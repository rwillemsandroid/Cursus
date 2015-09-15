# Navigation Drawer


**Android developer guide:**

[https://developer.android.com/training/implementing-navigation/nav-drawer.html](https://developer.android.com/training/implementing-navigation/nav-drawer.html)

## Drawer Layout ##

Available in de support library

### Creating a Drawer Layout ###

In je `layout/activity_main.xml` definieer je hetvolgende


```XML
    <android.support.v4.widget.DrawerLayout
	    xmlns:android="http://schemas.android.com/apk/res/android"
	    android:id="@+id/drawer_layout"
	    android:layout_width="match_parent"
	    android:layout_height="match_parent" >
	
	    <!-- The main content view -->
	    <LinearLayout
	        android:layout_width="match_parent"
	        android:layout_height="match_parent"
	        android:orientation="vertical">
	        <TextView
	            android:layout_width="match_parent"
	            android:layout_height="wrap_content"
	            android:text="HALLO, IK BEN DE CONTENT"/>
	    </LinearLayout>
	
	    <!-- The navigation drawer list-->
	    <LinearLayout
	        android:layout_gravity="start"
	        android:layout_width="240dp"
	        android:layout_height="match_parent"
	        android:orientation="vertical"
	        android:background="@color/theme_primary">
	        <TextView
	            android:layout_width="match_parent"
	            android:layout_height="wrap_content"
	            android:text="HALLO, IK BEN DE DRAWER"/>
    	</LinearLayout>

	</android.support.v4.widget.DrawerLayout>
```

Dit gaat ervoor zorgen dat er een navigation drawer gecreeerd wordt in je layout

## Opdracht ##

1. Voeg bovenstaande DrawerLayout toe aan je applicatie.
2. Volg onderstaande tutorial die een stapje verder gaat en de Drawer zal vullen met een lijst etc.

[http://javatechig.com/android/navigation-drawer-android-example](http://javatechig.com/android/navigation-drawer-android-example)