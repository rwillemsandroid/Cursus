# 23 App signing

[https://developer.android.com/tools/publishing/app-signing.html](https://developer.android.com/tools/publishing/app-signing.html)


Voor je een .apk bestand kan installeren op een device, moet dit bestand gesigneerd zijn met een keystore.
Een keystore kan je dus zien als een soort van certificaat of handtekening bij wijze van security token.

## Apk statusses ##

### Debug ###

App gesigned met local debug-key.
Dit is wat er gebeurd als je app test op je telefoon via Android Studio

### Unsigned ###

Apk die helemaal niet gesigned is. Een app die niet gesigned is kan niet geinstalleerd worden. 

At install time zal het systeem kijken naar de signature en niet vinden dus error geven.

### Release ###

Apk gesigned met een release key.

Om een app te uploaden naar Google Play moet deze gesigned zijn met een release key.

Als je een app op je toestel wilt updaten zal Android steeds kijken of de vorige en nieuwe versie gesigneerd zijn met dezelfde key.

Bijgevolg moet je wanneer je een update pushed op Google play ook met dezelfde release key signen als vorige build.

Doe een Keystore dus niet kwijt!

## Hoe sign je een applicatie? ##

### Debug ###
Gebeurd automatisch door android studio wanneer je iets deployed naar de device of "AssembleRelease" Gradle actie uitvoert.

### Release ###
Om dit te doen moet je een Keystore + paswoord toeveogen aan je project en gradle release configuratie.

Dit ziet er zo uit:

```groovy
android {
    compileSdkVersion 23
    buildToolsVersion "23.0.0"

	...

    defaultConfig {
       ...
    }

    signingConfigs {
        release {
            storeFile file("FILENAME")
            storePassword "PASSWORD"
            keyAlias "KEYNAME"
            keyPassword "KEYPASSWORD"
        }
    }

    buildTypes {
        release {
            minifyEnabled false
            proguardFiles getDefaultProguardFile('proguard-android.txt'), 'proguard-rules.pro'
            signingConfig signingConfigs.release
        }
    }


    lintOptions{
      ...
    }
    packagingOptions {
		...
```

Vervolgens kan je via Android Studio aan je Gradle acties: 

![New Project](/images/gradleacties.png)


De geexporteerde apks kunnen teruggevonden worden in 

    PROJECTLOCATOIN/MODULENAME/generated/outputs/apk/

## Hoe maak je een keystore? ##

In command line mvb van keytool die deel uitmaakt van standaard java release
    
    keytool -genkey -v -keystore my-release-key.keystore -alias alias_name -keyalg RSA -keysize 2048 -validity 10000

[http://stackoverflow.com/questions/3997748/how-can-i-create-a-keystore](http://stackoverflow.com/questions/3997748/how-can-i-create-a-keystore)