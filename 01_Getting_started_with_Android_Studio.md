# 01 Getting started with Android Studio #

Aan het einde van deze les heeft iedereen de juiste software geinstalleerd en is iedereen in staat om een project op een toestel of simulator te deployen.

## Android Studio ##

- Officially supported IDE
- **IntelliJ** based

#### Download ####

[https://developer.android.com/sdk/index.html](https://developer.android.com/sdk/index.html)

### Installeren SDK en build tools

Bij het eerste maal runnen van Android Studio, zal een wizard starten om de nodige dependencies, build tools en SDK te downloaden.

De benodigde items worden hier automatisch ingevuld.

## Creating your first App

Om je eerste applicatie te maken, selecteer je devolgende optie in je menu:


    File > New project 

Vervolgens doorloop je de wizard om je project to configureren.

![New Project](/images/01_newproject.png)


Voor dit voorbeeld gebruiken we devolgende instellingen:

- Target Androi Devices:

Phone and Tablet: **API 15**

- Add an Activity:

Blank Activity 

- Customize Activity 

Keep default values



## Running your Application

Press play button 

![New Project](/images/01_run.png)

### Target devices

#### Android toestel (GSM/Telefoon)
De meest voor de hand liggende optie is om je applicatie rechtstreeks op je Telefoon te uploaden.

Voor we dit kunnen doen moeten we eerst de USB Debugging van de telefoon opzetten. Dit kan je doen door volgende stappen te doorlopen.

1. Enable developer settings 

Op je Android toestel, ga naar 

    Instellingen > Over de telefoon

Vervolgens, ga je op zoek naar de **Build-nummer**.
Klik vervolgens 7 keer op dit nummer.

Proficiat! Je bent nu een developer.

2. Enable USB-Debugging

Op je Android toestel, is er nu bij instellingen een nieuw menu verschenen:

    Instellingen > Opties voor ontwikkelaars.
    
Ga in dit menu opzoek naar de optie **'Android-foutopsporing'** en vink deze optie aan


[![Youtube enable developer settings](http://img.youtube.com/vi/PLQ7CZeMEVA/0.jpg)](https://www.youtube.com/watch?v=PLQ7CZeMEVA)


Vind je de juiste opties niet terug? Vraag google om raad om te kijken hoe je de opties voor jouw specifiek toestel unlocked.

#### Android Emulator 

De **Android Virtual Device (AVD) Manager** , is een tool ingebouwd in Android Studio. 

![New Project](/images/01_avd.png)

Met deze tool is het mogelijk om een Android Virtual Device **Emulator** op te zetten.

Emulator = nabouwen van gedrag.

Nadeel: Traag

Meer info: [http://developer.android.com/tools/help/avd-manager.html
](http://developer.android.com/tools/help/avd-manager.html)

#### Android Simulator

Veel developers kiezen ervoor om in de plaats van de tragere officiele Android emulator te gebruiken, voor het gebruik van een third party Android Simulator, namelijk Genymotion.

[https://www.genymotion.com/#!/](https://www.genymotion.com/#!/)

Simuleren = nabootsen van gedrag.

Het voordeel van Genymotion is dat de simulators sneller werken dan de default AVD's en dat het makkelijker is om de externe sensoren en dergelijke te controleren.

Nadeel is dat Genymotion betalende software is, er is gelukkig wel een gratis versie met beperkte functionaliteit.

![Genymotion](/images/01_genymotion.png)

# Opdrachten #

- Installeer Android Studio 
- Zorg dat de nodige dependencies geinstalleerd zijn. 
- Genereer een nieuw, leeg Android Studio project zoals beschreven in dit document.
- Deploy je eerste "Hello world" applicatie


- (Optioneel) Setup emulator