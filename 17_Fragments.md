# 17 Fragments

## Intro ##

http://www.tutorialspoint.com/android/android_fragments.htm

## Oefening

Maak een activiteit met 2 knoppen en een framelayout.
Zorg ervoor dat wanneer je op een knop drukt, bijbhorende frame wordt geladen.

### tutorial: ###

http://examples.javacodegeeks.com/android/core/app/fragment/android-fragments-example/

**Opgepast:** 

- In plaats van `android.app.Fragment;` gebruiken we `android.support.v4.app.Fragment`
- Ook voor FragmentManager, gebruiken we deze van appcompat.
- In de XML gebruiken we `<FrameLayout>`in plaats van `<Fragment>`

**Opdrachten**

- In elke fragment, voeg Log messages toe in elke stap van de lifecycle.
- Schrijf iets weg in je sharedpreferences in Fragment 1
- Lees deze waarde terug uit in Fragment 2

### Extra: ###

- Switch fragments with animation 

[http://stackoverflow.com/a/9856449/3708094](http://stackoverflow.com/a/9856449/3708094)

## Viewpager ##

Werkt net zoals een recyclerview met een adapter

In plaats van kaartjes, fragments.


Tutorial

[https://github.com/codepath/android_guides/wiki/ViewPager-with-FragmentPagerAdapter](https://github.com/codepath/android_guides/wiki/ViewPager-with-FragmentPagerAdapter)