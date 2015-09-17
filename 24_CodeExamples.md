# Code Examples

## Setting a color filter on a drawable ##

```java
    Drawable d = …;
    d.setColorFilter(getResources().getColor(R.color.theme_primary), PorterDuff.Mode.MULTIPLY);
```
## Creating a Timer ##

```java
     private static final String FORMAT = "%02d:%02d:%02d";
    	...
      new CountDownTimer(10000, 1000) { // adjust the milli seconds here
    
    public void onTick(long millisUntilFinished) {
	    
	    mCouterTV.setText(""+String.format(FORMAT,
		    TimeUnit.MILLISECONDS.toHours(millisUntilFinished),
		    TimeUnit.MILLISECONDS.toMinutes(millisUntilFinished) - TimeUnit.HOURS.toMinutes(
		    TimeUnit.MILLISECONDS.toHours(millisUntilFinished)),
		    TimeUnit.MILLISECONDS.toSeconds(millisUntilFinished) - TimeUnit.MINUTES.toSeconds(
		    TimeUnit.MILLISECONDS.toMinutes(millisUntilFinished))));
	    }
	    
	    public void onFinish() {
	    	mCouterTV.setText("done!");
	    }
    }.start();
```