# Other device functionalities

## Camera ##

In a previous chapter we learned to use existing camera apps to provide us with a video or picture via **intents**.

It is also possible to directly access the device hardware and to use the camera.

For this we need the Camera permission from the manifest.

Tutorial:

http://developer.android.com/guide/topics/media/camera.html

Detecting camera hardware
Accessing cameras

## Location services ##

Makelijkste manier om Location te accessen is gebruik makend van de Google Play Services.

Google play services zullen achterliggend kijken welke hardware er beschikbaar is op je toestel en welke dingen aanstaan. Op basis daarvan zullen de play services een locatie doorgeven.

**Opgepast:**
Google play services zijn normaal beschikbaar op alle fysieke devices die verkocht worden.

**Maar!** De genymotion emulator heeft deze play services niet by default. Tenzij op een fysiek toestel kan niet iedereen deze oefening uitvoeren.

### Tutorial: ###

[http://www.androidhive.info/2015/02/android-location-api-using-google-play-services/](http://www.androidhive.info/2015/02/android-location-api-using-google-play-services/)


