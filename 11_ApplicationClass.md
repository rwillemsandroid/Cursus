# 11 Application Class #

[http://developer.android.com/reference/android/app/Application.html](http://developer.android.com/reference/android/app/Application.html)

Base class for those who need to maintain global application state. 

## Lifecycle ##


There is a Life-cycle for the android application BUT the applications have limited control over their own life-cycle, instead the components must listen for changes in the application state and react accordingly, the changes are as the following

- onCreate
- onLowMemory
- onTrimMemory
- onConfigurationChanged


## Hoe gebruiken? ##

### Extend Application class ###

    public class VDABApplication extends Application {
    	...
	    @Override
	    public void onCreate() {
	        super.onCreate();
	        ...
	    }
		...
    }

### Defineer in manifest dat dit de Application class is voor je activiteit ###

    <?xml version="1.0" encoding="utf-8"?>
    <manifest xmlns:android="http://schemas.android.com/apk/res/android"
    	package="be.vdab.simplelayout" >
    <application
	    android:allowBackup="true"
	    android:icon="@mipmap/ic_launcher"
	    android:label="@string/app_name"
	    android:theme="@style/AppTheme"
	    android:name=".VDABApplication">
    
		    <activity
		       ...
		    </activity>
    </application>
    
    </manifest>


## Use cases ##

- Initialiseer delen van je app (DB, Synchronisaties, Plant Log tree)
- Subscribe to services
- Register to Push server
- ....


## Oefening ##

Extend de Application class voor je project.

Zorg ervoor dat de Timber tree (Zie Jakewharton TImber logging library) geplaatst wordt in de OnCreate van je applicatie.


**Extra:**

Zorg ervoor dat de tree enkel geplant wordt in debug mode van je applicatie.