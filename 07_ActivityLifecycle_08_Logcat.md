# 07 Activity Lifecycle #



![New Project](/images/lifecycle.png)


Google training documents/Examples:

[http://developer.android.com/training/basics/activity-lifecycle/index.html](http://developer.android.com/training/basics/activity-lifecycle/index.html)


### onCreate() ###
Eerste stap in de Activity lifecyle


### onStart() ###

### onResume() ###
Executed na onStart() of wanneer de applictie terug in de voorgrond komt.

bv.:
- Heropenen van een geminimaliseerde applicatie
- Sluiten van overliggende activiteit


### onPause() ###

Deze functie wordt opgeroepen wanneer de activiteit niet langer zichtbaar is

### onStop() ###

Wanneer de activiteit helemaal gestopt wordt.

### onDestroy() ###

Executed vlak voor de activiteit volledig is afgesloten.

# 08 Logcat (Android Logging System)#

[http://developer.android.com/tools/help/logcat.html](http://developer.android.com/tools/help/logcat.html)

The Android logging system provides a mechanism for collecting and viewing system debug output. Logs from various applications and portions of the system are collected in a series of circular buffers, which then can be viewed and filtered by the logcat command. You can use logcat from an ADB shell to view the log messages.

### Log Utility

[http://developer.android.com/reference/android/util/Log.html ](http://developer.android.com/reference/android/util/Log.html)

![New Project](/images/logcat.png)

### Best practice ###

Pas op met Log messages!
Wanneer je gebruik maakt van Log Messages, hou er dan rekening mee dat deze ook zichtbaar zullen zijn voor Applicaties die in productie draaien. 

Het is aan te raden om ervoor te zorgen dat er Productie applicaties geen Log messages verschijnen. Het zou niet de eerste keer zijn dat er op deze manier gevoelige informatie lekt.

Twee manieren om het gebruik van de log messages te voorkomen:

- Maak een statische Logger-Class aan die eerste de Appconfiguratie nakijkt alvorens iets te printen.
- Maak gebruik van een gespecialiseerde Logger-Library (Meer hierover in het hoofdstuk over Gradle)


## Oefening  ##

**Oefening: Activity lifecycle**

In deze oefening gaan we de activity lifecyle testen.

1. maak een App met 2 Activiteiten.
2. Voeg een knop toe in Activity 1 die Activity 2 zal openen.
3. Voeg een knop toe in Activity 1 die Activity 2 zal openen en Activity 1 sluit. (`finish()`)
4. Overschrijf alle stappen in de activity lifecyle en voeg een Log message toe. Gebruik als TAG de naam van elke activiteit
4. Open de applicatie en navigeer tussen je Activiteiten, probeer je Applicatie te sluiten of te minimaliseren en opniuw te openen, hou ondertussen de prints in logcat in de gaten, welke stappen in de Lifecycle worden opgeroepen? Is dit wat je verwacht?
5. In Android Studio, voeg een Logcat filter toe, zorg dat enkel de Logcat messages van Activity 1 verschijnen in de console.


**Extra:**

- Maak gebruik van verschillende levels van Logging (Verbose, debug, warn, error)
- Stel de Android Studio Logcat console filters in op bepaalde log niveaus. 