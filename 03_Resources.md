# 03 Resources 



Android apps maken gebruik van resource files.

Deze files bevinden wich in de `res/` folder van je applicatie module.

![Hello World](/images/03_res2.png)

In deze files kunnen allerhande dingen gedefinieerd zijn. Dit kan gaan van Afbeeldingen tot kleuren en vormen.

[http://developer.android.com/guide/topics/resources/providing-resources.html](http://developer.android.com/guide/topics/resources/providing-resources.html)

## Resource types ##

### Strings ###

Text

[http://developer.android.com/guide/topics/resources/string-resource.html](http://developer.android.com/guide/topics/resources/string-resource.html)

### Colors ###

Kleuren

[http://developer.android.com/guide/topics/resources/more-resources.html](http://developer.android.com/guide/topics/resources/more-resources.html)

### Dimens ###

Afmetingen

[http://developer.android.com/guide/topics/resources/more-resources.html](http://developer.android.com/guide/topics/resources/more-resources.html)
### Other 

[http://developer.android.com/guide/topics/resources/more-resources.html](http://developer.android.com/guide/topics/resources/more-resources.html)

### Drawables  ###
#### Images ####

Afbeeldingen

- png
- jpg
- ...

#### Shapes ####
Het is ook mogelijk om zelf vormen of figuren te definieren in XML


    <?xml version="1.0" encoding="utf-8"?>
    <shape
    	xmlns:android="http://schemas.android.com/apk/res/android"
    	android:shape="oval">
    
       <solid 
       	android:color="#666666"/>
    
       <size 
       	android:width="120dp"
    	android:height="120dp"/>
    </shape>

## Resource Selection/Alternative Resources ##
At runtime, Android detects the current device configuration and loads the appropriate resources for your application.

Different selection criteria can be:

- Language 
- Resolution 
- Screensize 
- Country 
 
## Oefeningen

Oefening 1: Fanpagina

Start van de applicatie die je hier terugvind:

//TODO
App heeft al language switch.


Maak in dit scherm een informatiepagina van een onderwerp van jou keuze.
Zorg ervoor dat je informatiepagina minstens devolgende items bevat

afbeeldingen
text in zowel nederlands als engels


extra:
gebruik een scrollview
maak gebruik van shapes



Huisdier, favoriete sjotter, Hobby, ....