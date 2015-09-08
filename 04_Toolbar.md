# 04 Toolbar #


## What is the action bar? ##

The action bar (ActionBar) is located at the top of the activity. It can display the activity title, icon, actions which can be triggered, additional views and other interactive items. It can also be used for navigation in your application.

The action bar is enabled for devices which specify a target SDK of API version 11 or higher. It is possible to disable the action bar via the used theme, but the default Android themes have it enabled.

Applications with a target SDK version less than API 11 use the options menu if such a button is present on the device. The option menu is displayed if the user presses the Option button. The action bar is superior to the options menu, as the action bar is clearly visible, while the options menu is only shown on request. In case of the options menu, the user may not recognize that options are available in the application.

![New Project](/images/05_toolbar01.png)


(Source: [http://www.vogella.com/tutorials/AndroidActionBar/article.html](http://www.vogella.com/tutorials/AndroidActionBar/article.html))


## History 

### API 11 (Honycomb)

Intoductie of Actionbar

**Wat met devices < API 11?**

Compatibility library `ActionbarSherlock`, geschreven door [Jake Wharton](https://github.com/JakeWharton)


### API 21 

- Introductie Toolbar
- Google brengt de `AppCompat` library uit, die net zoals Actionbarsherlock, de ActionBar backwards compatible maakt tot API 9 (Gingerbread)


## Toolbar versus Actionbar? ##

Zonder al te veel in details te treden, kan je de Toolbar kan je zien als een meer flexibele versie van de Actionbar. 

De Actionbar maakte standaard deel uit van je activiteit en werd in het Applicatie-thema gedefinieerd.
De Toolbar daarintegen, moet manueel in de view-hierarche van je layout.xml files worden toegevoegd en in je Java code gelinkt worden aan de werking van je activiteit.


## Oefeningen: 

### Oef 1: Tutorial: How to make a material design Toolbar

Herneem je Fan-Pagina applicatie.

Aan de hand van onderstaande tutorial voegen we samen een Toolbar toe aan deze app.

[http://techlovejump.com/android-toolbar-tutorial/](http://techlovejump.com/android-toolbar-tutorial/)

**OPGELET:** gebruik AppCompatAcitivity in plaats van ActionBarActivity!!

### Oef 2: Verplaats de Engels en Nederlands knop naar opties in de Actionbar

![New Project](/images/05_toolbar_ex2.png)

hint: gebruik de menu resource files


### Extra 

- Verander de toolbar van kleur
- Gebruik een achtergrond afbeelding
- probeer de Actionbar van plaats te veranderen (Bv de bodem van je scherm)
- Gebruik een icoon voor een actie in de Toolbar: [https://materialdesignicons.com/](https://materialdesignicons.com/)