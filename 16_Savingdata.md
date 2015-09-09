# 16 Saving Data

[http://developer.android.com/training/basics/data-storage/index.html](http://developer.android.com/training/basics/data-storage/index.html)


## Shared Preferences ##

[http://developer.android.com/training/basics/data-storage/shared-preferences.html](http://developer.android.com/training/basics/data-storage/shared-preferences.html)

### Tutorial: ###

[http://www.androidgreeve.com/2014/01/How-to-use-Shared-Preferences-and-manage-User-Sessions.html](http://www.androidgreeve.com/2014/01/How-to-use-Shared-Preferences-and-manage-User-Sessions.html)

### Oefening 1

Gebruik shared preferences om iets op te slagen

### Oefening 2 ###

- Bouw een scherm gelijkaardig aan onderstaande screenhot
- Voeg de bijhorende functionaliteit toe.

![](images/shared_prefs.jpg)

## Using the file system ##

[http://developer.android.com/training/basics/data-storage/files.html](http://developer.android.com/training/basics/data-storage/files.html)

    <uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" />

### creating Files & Folders ###
http://developer.android.com/reference/java/io/File.html

**Create a folder**

    File fileDirectory = new File(Environment.getExternalStorageDirectory() + "/DIRECTORY/");
    fileDirectory.mkdirs();
    
**Create a file**

    File mFile;
    mFile = new File(File fileDirectory ,String pictureName);
    
### Using the Camera ###

    // create Intent to take a picture and return control to the calling application
    Intent intent = new Intent(MediaStore.ACTION_IMAGE_CAPTURE);
    //Specify the URI of your file as output directory for the picture
    intent.putExtra(MediaStore.EXTRA_OUTPUT, fileUri); // set the image file name
    // start the image capture Intent
    startActivityForResult(intent, CAPTURE_IMAGE_ACTIVITY_REQUEST_CODE);

### Oefening: ###

Gebruik het fototoestel van je toestel in je applicatie om een foto te nemen. 

[http://developer.android.com/guide/topics/media/camera.html#intents](http://developer.android.com/guide/topics/media/camera.html#intents)

Slaag deze foto op in een sub directory van je toestels external storage.

Om dit te doen doorloop je devolgende stappen.

1. maak een nieuwe folder
2. maak een nieuwe file aan in deze folder
3. vraag aan je camera applicatie om een foto te nemen en op te slaan in de zojuist gemaakte file via een Intent


**Extra:**
Geef je foto weer in je activiteit nadat deze genomen is (Gebruik hiervoor Picasso)


## Databases ##
[http://developer.android.com/training/basics/data-storage/databases.html](http://developer.android.com/training/basics/data-storage/databases.html)

### Accessing the DB on your filesystem ###

De database van de applicatie wordt opgeslagen in de private storage van je applicatie.
Hierdoor is het moeilijk toegang tot deze te krijgen zonder root access.

Gelukkig zijn de Genymotion Simulators geroot!


Om een database te raadplegen

1. In settings, enable installs from unknown sources
2. Download SQLite debugger op je Genymotion Simulator. APK vind je hier terug: [http://vdab.raf-willems.be](http://vdab.raf-willems.be)
3. Het kan zijn dat om veiligheidsredenen het bestand automatisch gerenamed word naar `donwnload.dn`, als dit het geval is, verander de extensie van dit bestand terug naar .apk
4. Install SQLite Debugger
5. Hoera




### Tutorials ###

[http://hmkcode.com/android-simple-sqlite-database-tutorial/](http://hmkcode.com/android-simple-sqlite-database-tutorial/)


Alternatief:

[http://www.techotopia.com/index.php/An_Android_SQLite_Database_Tutorial](http://www.techotopia.com/index.php/An_Android_SQLite_Database_Tutorial)


#### Oefening 1 ####

Tutorial 1

#### Oefening 2 ####

1. Maak een Database Table voor een nieuw object (Verzin zelf iets dat niet boek is)
2. Maak een layout met devolgende elementen:
	- Een manier om elementen toe te voegen aan de database
	- Een lijst die weergeeft wat er allemaal in je tabel zit