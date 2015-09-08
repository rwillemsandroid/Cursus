# 15 Retrofit

[http://square.github.io/retrofit/](http://square.github.io/retrofit/)

## JSON Server ##

Voor onze oefeningen, gebruiken we dezelfde JSON server als jullie voor iOS gedaan hebben.

[http://jsonplaceholder.typicode.com/](http://jsonplaceholder.typicode.com/)

Als de server goed is geinstalleerd, gebruik je de volgende command om de server te starten.

    json-server <FILE.DB>


waar `FILE.DB ` het bestand met je database data is



## About Retrofit 

### Retrofit 1 ###

- Owned by Square
- Opensource since 2010
- Originally a 'swiss knife' tool with misc stuff to help your android development
- Later focus op Rest webservices

### Retrofit 2 ###

- in beta
- officiele stabel release planned voor het einde van dit jaar

Voor deze opleiding doen we voorlopig niet te zot en gebruiken we een stabiele release van Retrofit, 1.9


    compile 'com.squareup.retrofit:retrofit:1.9.0'

## OkHttp ##

Retrofit uses OkHttp for the underlying networking library

    compile 'com.squareup.okhttp:okhttp:2.4.0'

## GSON ##

We gebruiken de Retrofit Library in combinatie met GSON.

[https://github.com/google/gson](https://github.com/google/gson)

"Gson is a Java library that can be used to convert Java Objects into their JSON representation. It can also be used to convert a JSON string to an equivalent Java object."

Dit will zeggen dat om Retrofit goed te gebruiken we ook best GSON importeren in ons project.
GSON zal er voor zorgen dat de JSON data die van de webservice komt geparsed wordt en omgezet naar een POJO (Plain Old Java Object)

    compile 'com.google.code.gson:gson:2.3'


## Retrofit Tutorial: ##

[https://github.com/codepath/android_guides/wiki/Consuming-APIs-with-Retrofit](https://github.com/codepath/android_guides/wiki/Consuming-APIs-with-Retrofit)


## Oefeningen ##

### Oefening 1

Gebruik Retrofit om een JSON webservice aan te spreken. 

Om te weten hoe je Retrofit gebruikt kan je de tutorial hierboven bekijken, devolgende stappen moeten doorlopen worden.

1. maak POJO's aan voor alle data die je wil afhalen van de webservices. (Tip:[http://www.jsonschema2pojo.org/](http://www.jsonschema2pojo.org/) )

![Hello World](/images/jsonschema2pojo.png)

2.  Maak een RestAdapter aan in je code
3.  Definieer een of meerdere endpoints in een interface
4.  Maak de access interface aan mbv je restadapter
5.  Vraag data op aan je webservice op mbv de gedefineerde endpoints 

Hiervoor kan je de JSON-testserver nemen die je ook tijdens de lessen iOS hebt gebruikt.

**Opgelet**: de Testserver gebruikt poort 3000, deze staat niet default open, om de JSON testserver te gebruiken zal je dus gebruik moeten maken van de **simulator**.

Geen data om te gebruiken?

Een voorbeeld JSON-database kan je hier terugvinden.
[https://raw.githubusercontent.com/typicode/jsonplaceholder/master/data.json](https://raw.githubusercontent.com/typicode/jsonplaceholder/master/data.json)


### Oefening 2

- Gebruik Retrofit om een nieuwe waarde te posten in je DB.

### Oefening 3

- Gebruik Retrofit om een lijst van objecten op te vragen.
- Geef deze objecten weer in een lijst (RecyclerView)

### Extra ###

Zoek een publieke REST service en probeer deze aan te spreken

bv.

- http://imdb.wemakesites.net/
- http://marsweather.ingenology.com/
- http://dev.socrata.com/consumers/getting-started.html
- http://developer.rottentomatoes.com/docs/read/JSON