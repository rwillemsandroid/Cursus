# 20 Notifications


## Notificaties weergeven ##

[http://developer.android.com/training/notify-user/build-notification.html](http://developer.android.com/training/notify-user/build-notification.html)

### Notification builder ###

`NotificationCompat.Builder` object. At bare minimum, a Builder object must include the following:

- A small icon, set by setSmallIcon()
- A title, set by setContentTitle()
- Detail text, set by setContentText()

```java
    NotificationCompat.Builder mBuilder =
    new NotificationCompat.Builder(this)
    .setSmallIcon(R.drawable.notification_icon)
    .setContentTitle("My notification")
    .setContentText("Hello World!");
```

### Notification onClick action ###

= Intent maken dat uitgevoerd wordt wanneer de notification geclicked wordt.

bv. 

- Intent voor homepage van je app
- Intent voor een detailpagina van je app (bv article detail etc)


```java
    Intent resultIntent = new Intent(this, ResultActivity.class);
    ...
    // Because clicking the notification opens a new ("special") activity, there's
    // no need to create an artificial back stack.
    PendingIntent resultPendingIntent =
    PendingIntent.getActivity(
    	this,
    	0,
    	resultIntent,
    	PendingIntent.FLAG_UPDATE_CURRENT
    	);
```

Om bovenstaande pendingIntent effectief toe te voegen aan de notification gebruiken we opnieuw de notificationbuilder:


```java
	mBuilder.setContentIntent(resultPendingIntent);
```

### Display the notification ###

To issue the notification:

- Get an instance of NotificationManager.
- Use the notify() method to issue the notification. When you call notify(), specify a notification ID. You can use this ID to update the notification later on. This is described in more detail in Managing Notifications.
- Call build(), which returns a Notification object containing your specifications.

For example:

```java
	NotificationCompat.Builder mBuilder;
	...
	// Sets an ID for the notification
	int mNotificationId = 001;
	// Gets an instance of the NotificationManager service
	NotificationManager mNotifyMgr = 
     	   (NotificationManager) getSystemService(NOTIFICATION_SERVICE);
	// Builds the notification and issues it.
	mNotifyMgr.notify(mNotificationId, mBuilder.build());
```

## Notifications triggeren ##

### GCM -> Google Cloud Messaging (Out of scope) ###

[https://developers.google.com/cloud-messaging/](https://developers.google.com/cloud-messaging/)

Idee is alsvolgt

1. App registreert device bij de Google Cloud service
2. App stuurt App id naar de maker van de app (Target server)
3. Wanneer we een notification uit willen sturen, spreken we een google cloud webservice aan en geven als target de id mee die we kregen in stap 2
4. Google zorgt ervoor dat er een broadcast uitgestuurd wordt naar de applicatie die geregistreerd is

### Alternatieve service: Parse.com ###

Gratis online backend voor je applicatie.

- Push
- Database backend
- scripting
- Analytics and crash reporting
- ...