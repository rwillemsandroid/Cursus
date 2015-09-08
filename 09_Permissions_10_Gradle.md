# 09 Permissions

Permissies worden gedefineerd in het Android manifest

Volledige uitleg/Source: [http://www.hongkiat.com/blog/android-app-permissions/](http://www.hongkiat.com/blog/android-app-permissions/)

First things first, Android app permissions aren’t requests, they’re declarations. Unless you’re rooted, you have no say – short of choosing to not install the app – in whether the app will receive all the permissions it requires.

When you install an app from the Play Store, you’ll get a pop up listing all the permissions that the app requires, things like access to your storage, phone calls, network communciation etc. 

### Common permissions ###

- Location
- External storage
- Internal storage
- Internet
- Bluetooth
- Vibratie
- Sychronisatie beheren
- Audioinstellngen aanpassen
- Achtergrond veranderen
- Phone Status And Identity
- Read/Modify Contacts
- SMS and MMS
- Account Related Permissions
	- Find Accounts
	- Use Accounts
- ...

![Hello World](/images/permissions.png)


### in Android M ###

[https://developer.android.com/preview/features/runtime-permissions.html](https://developer.android.com/preview/features/runtime-permissions.html)

#### Declaring permissions 
The app declares all the permissions it needs in the manifest, as in earlier Android platforms.
#### Permission Groups 
 Permissions are divided into permission groups, based on their functionality. For example, the CONTACTS permission group contains permissions to read and write the user's contacts and profile information.
#### Limited Permissions Granted at install time 
When the user installs or updates the app, the system grants the app all permissions listed in the manifest that fall under PROTECTION_NORMAL. For example, alarm clock and internet permissions fall under PROTECTION_NORMAL, so they are automatically granted at install time. For more information about how normal permissions are handled, see Normal Permissions.
The system may also grant the app signature permissions, as described in System components and signature permissions. The user is not prompted to grant any permissions at install time.
#### User grants permissions at runtime 
When the app requests a permission, the system shows a dialog to the user, then calls the app's callback function to notify it whether the user granted the permission.
### Develop for M ###

#### Always check for permissions ####
When the app needs to perform any action that requires a permission, it should first check whether it has that permission already. If it does not, it requests to be granted that permission. You do not need to check for permissions that fall under PROTECTION_NORMAL.
#### Handle lack of permissions gracefully ####
If the app is not granted an appropriate permission, it should handle the failure cleanly. For example, if the permission is just needed for an added feature, the app can disable that feature. If the permission is essential for the app to function, the app might disable all its functionality and inform the user that they need to grant that permission.

#### Permissions are revocable ####
Users can revoke an app's permissions at any time. If a user turns off an app's permissions, the app is not notified. Once again, your app should verify that it has needed permissions before performing any restricted actions.


## Voorbeeld manifest met permissies ##


    <?xml version="1.0" encoding="utf-8"?>
    <manifest xmlns:android="http://schemas.android.com/apk/res/android"
    	package="be.vdab.simplelayout" >
    
	    <uses-permission android:name="android.permission.READ_CONTACTS"/>
	    <uses-permission android:name="android.permission.INTERNET"/>
	    <uses-permission android:name="android.permission.READ_CONTACTS"/>
	    <uses-permission android:name="android.permission.BLUETOOTH"/>
	    <uses-permission android:name="android.permission.CALL_PHONE"/>
	    <uses-permission android:name="android.permission.READ_CALL_LOG"/>
	    <uses-permission android:name="android.permission.CAPTURE_VIDEO_OUTPUT"/>
    
	    <application
		    android:allowBackup="true"
		    android:icon="@mipmap/ic_launcher"
		    android:label="@string/app_name"
		    android:theme="@style/AppTheme" >
			    <activity
				    android:name=".MainActivity"
				    android:label="@string/app_name" >
				    <intent-filter>
				    	<action android:name="android.intent.action.MAIN" />
				    
				    	<category android:name="android.intent.category.LAUNCHER" />
				    </intent-filter>
			    </activity>
	    </application>
    
    </manifest>



# 10 Gradle

![Hello World](/images/gradlesync.jpg)

## Korte uitleg: ##

Gradle is een Buildsystem

Buidsysteem -> compileert de source code van je programma

### Groovy ###

Gradle build systeem laat ook to om scripts toe te voegen aan je gradle files om bepaalde taken te autmatiseren.
bv. het toevoegen van versienaam aan de output apk.

Deze scripts worden geschreven in Groovy.


![Hello World](/images/gradlefile.png)

#### Dependencies

Aangezien Gradle alles moet compileren, moet Gradle ook weten waar alle dependencies terug te vinden zijn. 

Net zoals bij Maven, zijn de meeste Android Libraries online beschikbaar en rechtstreeks te importeren in Gradle.

Dit kan je doen door slechts 1 regel toe te voegen aan de Gradle file van je Applicatie Module.

    
    apply plugin: 'com.android.application'
    
    android {
    	compileSdkVersion 21
    	buildToolsVersion "21.1.2"
    
    	defaultConfig {
    		applicationId "com.ebookfrenzy.buildexample"
    		minSdkVersion 19
    		targetSdkVersion 21
    		versionCode 1
    		versionName "1.0"
    	}
    buildTypes {
    release {
    	minifyEnabled false
    	proguardFiles getDefaultProguardFile('proguard-android.txt'), 'proguard-rules.pro'
    	}
    }
    }
    
    dependencies {
    	compile fileTree(dir: 'libs', include: ['*.jar'])
    	compile 'com.android.support:appcompat-v7:21.0.3'
    }

# Oefeningen #

#### Oefening 1: Timber ####

In het hoofdstuk over Logcat werd aangehaald dat er libraries bestaan die het gebruik van Log messages makkelijker maakt en ervoorzorgt dat er in productie geen Log messages verschijnen.

Een van deze libraries is Timber.

Je vind Timber hier terug:

[https://github.com/JakeWharton/timber](https://github.com/JakeWharton/timber)

Importeer Timber in je project.

#### Oefening 2: Picasso ####

Het correct afhalen, gebruik en cashing van afbeeldingen van het internet op Android is niet zo evident.

Gelukkig zijn er libraries die dit voor ons kunnen. De populairste image cashing library is **Picasso**.

Je vind deze hier terug:

[http://square.github.io/picasso/](http://square.github.io/picasso/)

- Gebruik Picasso om de Profile picture uit je Fanpagina app dynamisch af te halen van het web.
- Schakel de netwerkverbinding uit en open de applicatie opnieuw. Zie je de afbeelding nog?
 
#### Oefening 3: You choose! ####

Bekijk onderstaande lijst met Android Material design libraries. Kies er eentje uit en gebruik deze om een element van je Fan app te verbeteren of om een element toe te voegen.

[https://github.com/wasabeef/awesome-android-ui](https://github.com/wasabeef/awesome-android-ui)

Alternatief kan je ook de Google Android Design Library gebruiken en een nieuw element hiervan gebruiken.