# 02 Simple User interface 

## Hello World ##

Om te starten bekijken we het automatisch gegenereerde voorbeeldproject van *Les 01 - Getting Started with Android studio*


![Hello World](/images/02_helloworld.png)


## Project Structure ##

Bekijken we de automatisch gegenereerde bestanden voor dit voorbeeldproject nemen we devolgende structuur waar:

![Hello World](/images/02_projectstructure.png)

De bestanden die belangrijk zijn voor dit hoofdstuk werden uitgeklapt, namelijk:

- MainActivity.java
- activity_main.xml

### MainActivity.java ###

Wanneer de applicatie start, zal `MainActivity.java` de eerste activiteit zijn die wordt opgestart.

Een Activiteit zoals ze deze voorlopig zullen zien in deze lessen, kan beschouwd worden als een scherm.

Het iOS equivalent van een Android Activiteit is een `UI Viewcontroller`.


Net zoals op iOS, zal ook op bij Android elke scherm een zeker lifecycle doorlopen, deze lifecycle bestaat uit verschillende stappen, gaande van `OnCreate();` tot `OnDestroy();`.

Later in deze lessen zal de Activity lifecycle meer in detail besproken worden.

Openen we nu deze MainActivity zien we devolgende code terugkomen.

![Hello World](/images/02_setcontentview.png)

`activity_main.xml`, klinkt bekend?

### activity_main.xml

![Hello World](/images/02_layoutxml.png)

Openen we dit xml bestand, zien we een soort van **markup-taal** met een syntax die een beetje lijkt op die van html.

We zien een element `RelativeLayout` dat een element `TextView` omvat.

Deze elementen zijn de bouwstenen van onze layout.

Elke van deze elementen heeft enkele attributen, elke staande voor een andere eigenschap van dit element. Gaande van dimentie tot kleur.

### Applicatie ###

Kijken we nu terug naar de applicatie, zien we dat de TextView met attribuut `android:text = "Hello world!"` inderdaad terugkomt in onze app. 


## Layout elementen en Java Objecten linken. ##

In volgend voorbeeld gaan we een stapje verder. 

We voegen een Button toe aan onze layout.

![Hello World](/images/02_buttonxml.png)


![Hello World](/images/02_button.png)

Vervolgens linken we in de `OnCreate(..)` Functie van onze `MainActivity.java` class een Button-Object met de knop die we net toevoegden. 

Dit doen we doormiddel van onderstaande lijn code

        //Ken de Button met id my_button op activity_main toe aan object mMyButtn
        mMyButton = (Button) findViewById(R.id.my_button);

![Hello World](/images/02_buttonjava.png)

## Verschillende Types Bouwstenen ##

In bovenstaande voorbeeld hebben jullie reeds kennis kunnen nemen met de `TextView` en `Button`.

Hiernaast bestaan er nog vele andere UI bouwstenen. Hieronder worden enkele van de belangrijkste opgelijst.

Verschillende type elementen kunnen verschillende types parameters bezitten. 


### LinearLayout

Container voor andere UI elementen.
Elementen in deze layout worden op een lineaire manier naast elkaar in de layout geplaatst.
Dit kan horizontaal of verticaal gebeuren.

[http://developer.android.com/guide/topics/ui/layout/linear.html](http://developer.android.com/guide/topics/ui/layout/linear.html)

### RelativeLayout ###

Net als de LinearLayout is de RelativeLayout een container voor andere elementen.
 In plaats van dat de elementen linear naast elkaar gezet worden, kunnen ze nu relatief van elkaar geplaatst worden.

[http://developer.android.com/guide/topics/ui/layout/relative.html](http://developer.android.com/guide/topics/ui/layout/relative.html)

### TextView ###

Weergeven van text.

[https://developer.android.com/reference/android/widget/TextView.html](https://developer.android.com/reference/android/widget/TextView.html)

### EditText ###

Textinput user

[http://developer.android.com/reference/android/widget/EditText.html](http://developer.android.com/reference/android/widget/EditText.html)

### Button  

Knop 

[http://developer.android.com/reference/android/widget/Button.html](http://developer.android.com/reference/android/widget/Button.html)

### Switch ###

Toggle button

[http://developer.android.com/reference/android/widget/Switch.html](http://developer.android.com/reference/android/widget/Switch.html)

### Spinner ###

Dropdown selectie

[http://developer.android.com/guide/topics/ui/controls/spinner.html](http://developer.android.com/guide/topics/ui/controls/spinner.html)

### ImageView ###

Weergeven van een afbeelding

[https://developer.android.com/reference/android/widget/ImageView.html](https://developer.android.com/reference/android/widget/ImageView.html)

### ScrollView ###

View container voor scrollable content.

[https://developer.android.com/reference/android/widget/ScrollView.html](https://developer.android.com/reference/android/widget/ScrollView.html)

### WebView ###

Weergeven van een website.

[http://developer.android.com/reference/android/webkit/WebView.html](http://developer.android.com/reference/android/webkit/WebView.html)

# Opdrachten  

#### Oef 1: Click teller ####
Herneem je Hello world project van vorig hoofdstuk of maak een nieuw leeg project aan.

- Plaats een button in het midden van je activiteit.
- Plaats een textveld naast of boven je knop met het cijfer 0
- Zorg ervoor dat elke keer de user op de knop klikt, het cijfer in je textveld met 1 toeneemt.


### Oef 2: Click teller + ###

Deze oefening bouwt voort op oefening 1

Voeg een inputveld toe aan je View. In dit veld kan de gebruiker een nummer invoegen. 

Zorg ervoor dat wanneer de gebruiker op de knop duwt, het ingegeven cijfer genomen wordt. 


### Oef 3: Spelen met layouts ###

probeer hetvolgende scherm na te bouwen:

![Hello World](/images/02_oefBtns1.png)


### Extra ###

- verander de textkleur van je teller uit oef 1 en 2
- verander de achtergrondkleur van je scherm `"@android:color/"`


- probeer hetvolgende scherm na te bouwen:

![Hello World](/images/02_oefBtns2.png)