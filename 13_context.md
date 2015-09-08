# 13 Application Context #

[http://stackoverflow.com/a/3572553/3708094](http://stackoverflow.com/a/3572553/3708094)

**Uitleg:**

As the name suggests, its the context of current state of the application/object. It lets newly created objects understand what has been going on. Typically you call it to get information regarding another part of your program (activity, package/application)

You can get the context by invoking` getApplicationContext()`, `getContext()`, `getBaseContext(`) or `this` (when in the activity class).

**Use cases**

- **Creating New objects**: Creating new views, adapters, listeners:

    TextView tv = new TextView(getContext());
    ListAdapter adapter = new SimpleCursorAdapter(getApplicationContext(), ...);


- **Accessing Standard Common Resources**: Services like LAYOUT_INFLATER_SERVICE, SharedPreferences:

    context.getSystemService(LAYOUT_INFLATER_SERVICE)   
    getApplicationContext().getSharedPreferences(*name*, *mode*);

- **Accessing Components Implicitly:** Regarding content providers, broadcasts, intent


    getApplicationContext().getContentResolver().query(uri, ...);