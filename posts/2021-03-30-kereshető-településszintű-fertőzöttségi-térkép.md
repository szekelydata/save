---
title: 🌄 Kereshető településszintű fertőzöttségi-térkép
date: 2021-03-30 04:23:33
---


A legújabb járványügyi intézkedések Romániában a korlátozások mértékét a **település-szintű fertőzöttségi rátá**hoz kötik. Ez az utóbbi két hétben megjelent új esetek számát, ezer főre vetítve (‰) mutatja meg. A kormány a település-szintű adatokat csak idén (2021) március eleje óta publikálja (de nem a hivatalos COVID19 kommunikációs oldalon, hanem máshol), és **nincs egy hivatalos eszköz**, ahol a település-szintű adatokat meg lehetne jeleníteni. A többi járványtani és gazdasági mutatóval együtt ezeket az adatokat már át is vettük a **COVID-19 – Romanian Economic Impact Monitor**-ra.

Ugyanakkor elkészítettem **🌄 egy önálló oldalt** is, ahol csak a településszintű fertőzöttségi rátákra kereshetünk. Ez eredmény egy choropleth térkép, amelyen a székelydatás szokástól eltérően, most a települések nevei nem magyarul jelennek meg, mivel ezek a teljes ország szintjén léteznek. Ugyanakkor a **keresőben **magyar és román kifejezések egyaránt működnek (bizonyos mértékig). Közelítésre a térképen megjelennek a kisebb települések címkéi is.

**🕹 Interaktív **



A **COVID-19 – Romanian Economic Impact Monitor**-on mutatjuk az idősoros adatokat is, ezek márciusra így néznek ki 👇





**ADATOK + KÓD:** Az adatok forrása a **COVID-19 – Romanian Economic Impact Monitor**.  megjelenítéshez **kepler.gl**-t használtam. A térkép konfigurációs file-ja és az UAT-szintű fertőzőttségi adatok (a reprodukáláshoz) innen tölthetőek le. Helység, azaz *Unitate Administrativ Teritorială* (UAT)-szintű térképfile-okat nem könnyű találni, ez egy jó kezdeményezés, de itt sincsenek település-szintű térképek. A hivatalos adatoknak elméletileg itt vagy itt kellene lenniük, de ez még a múlt évtizedben ragadt, amikor csak a ESRI ArcGIS volt az egyetlen térkép-megjelenítési módszer, és shapefile formátumban vannak (nem találtam/nem tudtam letölteni - pedig még videó is készült róla). A data.gov.ro-n sem lehet semmi használhatót találni. Végül itt és az Eurostat-on sikerült találnom letölthető shapefile-okat, ezeket megpróbáltam áthozni a 21. századba. Ezért ebben a mappában talász majd **geojson**és**topojson**formátumot** Románia megyéi**ről és az** UAT**k-ről. Később megtaláltam a geo-spatial.org oldalt is, ahol a forráskódból kibányászható egy UAT-szintű topojson.