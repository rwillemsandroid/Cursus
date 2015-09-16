# 21 Sounds


    android.media.MediaPlayer;

## Example ##

```java
     MediaPlayer mp;
	 mp = MediaPlayer.create(NavDrawerActivity.this, R.raw.kzaluisietszeggense);
	 mp.setOnCompletionListener(new MediaPlayer.OnCompletionListener() {
	    
		    @Override
		    public void onCompletion(MediaPlayer mp) {
		    // TODO Auto-generated method stub
		    mp.reset();
		    mp.release();
		    mp=null;
		    }
	    
	    });
    mp.start();
```