# 03 Resources 



Android apps maken gebruik van resource files.

Deze files bevinden wich in de `res/` folder van je applicatie module.

![Hello World](/images/03_res2.png)

In deze files kunnen allerhande dingen gedefinieerd zijn. Dit kan gaan van Afbeeldingen tot kleuren en vormen. Enkele van de belangrijkste resource types worden in dit hoofdstuk opgelijst.

[http://developer.android.com/guide/topics/resources/providing-resources.html](http://developer.android.com/guide/topics/resources/providing-resources.html)

## Resource types ##

### Strings ###

Text resources.

[http://developer.android.com/guide/topics/resources/string-resource.html](http://developer.android.com/guide/topics/resources/string-resource.html)

### Colors ###

Kleuren.

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

Het is mogelijk om verschillende resources te configuren voor verschillende type gebruikers.

Tijdens de runtime zal Android automatisch je toestel configuratie detecteren en de de juiste resources voor je 
applicatie inladen.

De verschillende criteria bevatten onder andere

- Language 
- Resolution 
- Screensize 
- Country 
- Android versie
- ...
 
In onderstaande afbeelding zie hoe een launcher icon werd gedefinieerd voor verschillende schermdensiteiten.

![Hello World](/images/03_dpi.png)


## Oefeningen

### Oefening: Fanpagina

Start van de applicatie die je hier terugvind:

[https://github.com/rwillemsandroid/Ex03_01_Fanpage/](https://github.com/rwillemsandroid/Ex03_01_Fanpage/)


Maak in de MainActivity een informatiepagina van een onderwerp van jou keuze.
Dit kan informatie zijn over je favorite voetbalspeler, sport, hobby, huisdier, ....


Zorg ervoor dat je informatiepagina minstens devolgende items bevat:

- een of meerdere afbeeldingen
- text komende uit de resources
- zorg voor een aangepaste layout voor tablet (w600dp)


**extra:**

- gebruik een scrollview
- maak gebruik van shapes
- gebruik /dimens voor padding, marges en afmetingen
- Maak een gradient achtergrond

