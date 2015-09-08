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

    File fileDirectory = new File(Environment.getExternalStorageDirectory() + "/FILENAME/");
    photoDirectory.mkdirs();
    
**Create a file**

    File mFile;
    mFile = new File(File fileDirectory ,String pictureName);
    


### Oefening: ###

Gebruik het fototoestel van je toestel in je applicatie om een foto te nemen. 

[http://developer.android.com/guide/topics/media/camera.html#intents](http://developer.android.com/guide/topics/media/camera.html#intents)

Slaag deze foto op in een sub directory van je toestels external storage.

Om dit te doen doorloop je devolgende stappen.

1. maak een nieuwe folder
2. maak een nieuwe file aan in deze folder
3. vraag aan je camera applicatie om een foto te nemen en op te slaan in de zojuist gemaakte file via een Intent


**Extra:**
Slaag een thumbnail op van de foto die je getrokken hebt


## Databases ##
[http://developer.android.com/training/basics/data-storage/databases.html](http://developer.android.com/training/basics/data-storage/databases.html)

Tutorial:

[http://www.techotopia.com/index.php/An_Android_SQLite_Database_Tutorial](http://www.techotopia.com/index.php/An_Android_SQLite_Database_Tutorial)