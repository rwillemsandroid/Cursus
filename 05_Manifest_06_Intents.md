# 05 Manifest #

## What is het Android Manifest?

AndroidManifest.xml is een bestand dat zich in de rootfolder van je project module bevind.

Dit bestand bevat informatie die crusiaal is voor het runnen van je applicatie op een Android toestel. 

De je Manifest definieert onder andere

- De java packagename voor je applicatie
- De componenten van je applicatie
	- activiteiten
	- services
	- broadcast receivers
	- ...
- de permissies die je applicatie nodig heeft
- welk applicatie thema er gebruikt wordt
- welke activiteit er gestart wordt bij het openen van je applicatie
- ....


Voor de volledige uitleg rond het Android Manifest verwijs ik naar de officiele documentatie:

[http://developer.android.com/guide/topics/manifest/manifest-intro.html](http://developer.android.com/guide/topics/manifest/manifest-intro.html)


![New Project](/images/05_manifest.png)


# 06 Intents #

Wat?

Een intent is een messaging-object dat je kan gebruiken om acties op te vragen van andere app componenten.

De drie main use cases zijn:

- Start een activity
- Start een service
- Deliver a broadcast

In praktijk zullen jullie intents gebruiken om

- andere activiteiten te starten
- berichten voor externe applicaties uitsturen


Sources:

[http://developer.android.com/guide/components/intents-filters.html](http://developer.android.com/guide/components/intents-filters.html)

[http://developer.android.com/reference/android/content/Intent.html](http://developer.android.com/reference/android/content/Intent.html)

[http://developer.android.com/training/basics/firstapp/starting-activity.html](http://developer.android.com/training/basics/firstapp/starting-activity.html)

## Oefeningen: 

### Oef 1: Voeg een tweede activiteit toe aan je Fan applicatie. ###

- Voeg een tweede activiteit toe
- Voeg een knop toe om naar activiteit 2 te gaan


### Oef 2 
- Intent voor Internet
- Intent voor Google Maps(Niet op emulator)
- Intent voor email
- Blokkeer landscape mode in je app