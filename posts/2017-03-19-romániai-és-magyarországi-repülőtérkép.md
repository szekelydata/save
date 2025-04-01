---
title: Romániai és Magyarországi repülőtérkép
date: 2017-03-19 20:14:13
---


Ebben a bejegyzésben **Románia** és **Magyarország** repülőtereinek heti járatszámait vizsgáljuk. Így közvetetten ez a bejegyzés a Székelyföldi diaszpóra elemzéshez kapcsolódik.



Interaktív adatvizualizációk

[iframe src="http://szekelydata.csaladen.es/repulok/ro/" height=423 style="overflow:hidden;"]

**Romániai repülőtérkép (teljes képernyő)**



[iframe src="http://szekelydata.csaladen.es/repulok/hu/" height=423 style="overflow:hidden;"]

**Magyarországi repülőtérkép (teljes képernyő)**



A fenti két adatvizualizáción az országok reptereit elhagyó repülőgépeket láthatjuk, színkódólva. A repülők relatív frekvenciája a heti járatsűrűséggel arányos. A célvárosokba Európa-szerte tortadiagrammokat helyeztünk el, amelyek az oda érkező járatok heti gyakoriságát mutatják, forrásrepterek szerint rangsorolva. A baloldali menü segítségével ki-be kapcsolhatók az adatvizualizáció különböző elemei: a repülők, hálozatvonalak és csomópontok (városok). Az országokra kattintva illetve az egérgörgő használatával közelíthetjük a térképet. A jobboldali információcsíkban az épp felszálló repülő célállomása jelenik meg, színkódja a kiindulási várost jelöli.



Minielemzés

A két ország repülőtérképe szembeötlően eltér egymástól: a romániai egy szivárvány, míg a magyarországi majdnem egyszínű. Ez azt jelenti, hogy Romániában sokkal (egy nagyságrenddel) több nemzetközi repülőtér található. Mi több, a Romániában felszálló repülők legnagyobb célországa ugyancsak Románia, azaz jelentős a belföldi piac - persze ez a két ország merőben eltérő földrajzának tudatában érthető. Nézzük csak a **romániai belföldi járatok** térképét:



[iframe src="http://szekelydata.csaladen.es/repulok/ro/dom.html" height=423 style="overflow:hidden;"]



Bukarestet hetente 176 belföldi járat hagyja el, 58 Kolozsvár, 44 Jászvásár, valamint 39.8 Temesvár irányába, de rendszeresen vannak járatok továbbá Nagyvárad, Szeben, Suceava és Szatmárnémeti reptereire is, illetve Kolozsvár, Temesvár és Jászvásár direkt összeköttettésben is áll egymással. A legnagyobb belföldi légitársaság a Tarom, heti 234 belföldi járattal, ezt követi a Blue Air 91-el, valamint a Ryanair és a Wizzair heti 28, illetve 10 járattal.



[iframe src="http://szekelydata.csaladen.es/repulok/d3ro/dom.html" height=423 style="overflow:hidden;"]



A bejegyzés hátralevő részében a d3plus könyvtár buborékdiagram típusú adatvizualizációkat fogunk használni. Ez a fatérképhez hasonló *területileg* arányos megjelenítési forma.



Célországok

Romániában hetente 1501,6 járat száll fel, míg ez a szám a magyar reptereken 789,3. A leggyakrabban elérhető külföldi desztináció Romániából Olaszország, heti 201 járattal. Ezt követi Németország 200-al, és az Egyesült Királyság 153-al. A magyarországi járatok legnagyobb célországa az Németország és az Egyesült Királyság, 147, illetve 110 heti járattal.Utána következik Olaszország és Hollandia 61 és 43,5 járattal. Az alábbi két buborékdiagramon Románia és Magyarország 8 legnagyobb célországaiba tartó járatokat tűntettük fel. A diagramok interaktívak, a buborékokra klikkelésre megmutatják a járatok kiindulási pontjait, illetve a működtető légitársaságokat.



**Románia**



[iframe src="http://szekelydata.csaladen.es/repulok/d3ro/countries.html" height=423 style="overflow:hidden;"]



**Magyarország**



[iframe src="http://szekelydata.csaladen.es/repulok/d3hu/countries.html" height=423 style="overflow:hidden;"]



Ha visszaemlékezünk a Székelyföldi diaszpóra elemzésre, és Székelyföld lakosságát a romániai és magyarországi ötvözetének vesszük, akkor láthatjuk, hogy a repülőutak célországai majdnem egyenesen arányosan megegyeznek a diaszpóra országaival. Természetesen Magyarország és Románia kilóg a sorból (nagyobb diaszpóra, mint a járatszám által indokolt lenne), hiszen ezekre a területekre az utazás főként nem repülővel történik. Az **alábbi diagram** egy log-log plot, mivel a diaszpóra, akárcsak a népesség, a már említett hatványtörvény alapján szerveződik - ez a repülőjáratokra is igaz.



[iframe src="http://szekelydata.csaladen.es/repulok/diasp.html" height=523 style="overflow:hidden;"]



Városok

Ha a városok szerinti sorrendet vesszük figyelembe, Bukarest után (176), London toronymagasan vezet: Romániából naponta 18 járat száll az angol fővárosba (hetente 128). Ezt München és Milánó, 84, illetve 65 járattal hetente, majd Kolozsvár (65), Bécs (58,2) és Róma (57). Ezután újra két belföldi város következik Jászvásár (51) és Temesvár (46,8), majd Párizs (45,5), Isztambul (44,5), Brüsszel (41), Tel Aviv (35,8), Frankfurt és Madrid (mindkettő 35,5), Chisinau (27,5), Amszterdam (27) és Bologna (24).



Budapestről és Debrecenből ugyancsak messze az angol főváros a legkönnyebben megközelíthető légi úton, ide heti 87 repülő száll, több, mint kétszer annyi, mint az ezt követő Brüsszelbe (36,5) és Párizsba (37). Ezután jön Berlin (36), München (35), illetve Frankfurt és Varsó (mindkettő 30), majd Amszterdam (24) a rangsorban.



**Románia - városok szerint**



[iframe src="http://szekelydata.csaladen.es/repulok/d3ro/cities.html" height=423 style="overflow:hidden;"]



**Románia - légitársaságok szerint**



[iframe src="http://szekelydata.csaladen.es/repulok/d3ro/cities2.html" height=423 style="overflow:hidden;"]



**Magyarország - légitársaságok szerint**



[iframe src="http://szekelydata.csaladen.es/repulok/d3hu/cities2.html" height=423 style="overflow:hidden;"]



A diaszpóra arányait a **városok** is tartják, persze akárcsak az országok esetében, itt is a romániai és a magyarországi városok kivételével. A trendtől jelentős mértékben eltér egyetlen város, Tel Aviv, ahová sokkal több járat száll, mint azt a diaszpórája indokolná, illetve kisebb mértékben ugyanebben a helyzetben van Isztambul. Ellenben, hogyha figyelembe vesszük, hogy Izrael más városaiban is jelentős a diaszpóra (pl. Jeruzsálem), de ezek nem rendelkeznek önálló reptérrel, akkor visszaáll a rend. Verona a trend másik végén lóg ki a sorból, ide kevesebb járat száll, mint azt a diaszpórájának mérete indokolná.



[iframe src="http://szekelydata.csaladen.es/repulok/diasp_cities.html" height=523 style="overflow:hidden;"]



Társaságok

A Tarom Románia legnagyobb légitársasága, megelőzve a Wizzair-t. A nemzeti légitársaság hetente 446 járatot működtet, a Wizzair 336-ot. Őket követi a Blue Air és a Ryanair, 244 és 143 járattal hetente. A magyar piacot a Wizzair uralja, kissé több, mint a Romániai járatok felével, heti 181-el. Magyarországról hetente 112 Ryanair repülő száll föl, 59.8 Lufthansa és 47 easyjet.



**Románia**



[iframe src="http://szekelydata.csaladen.es/repulok/d3ro/airlines.html" height=423 style="overflow:hidden;"]



**Magyarország**



[iframe src="http://szekelydata.csaladen.es/repulok/d3hu/airlines.html" height=423 style="overflow:hidden;"]



Böngésző

Az eddigi buborékdiagramokon az adatokat szűrtük az első 8-12 találatra, ezért nem jelent meg az összes regisztrált járat információja. Az alábbi böngésző diagramokon a teljes adatsor helyet kapott, így egyes országokra, illetve városokra kattintva a teljes összeköttettési információ megjeleníthető, **Romániából** vagy **Magyarországról, **illetve egy **univerzális app**-on.



[iframe src="http://szekelydata.csaladen.es/repulok/" height=630 style="overflow:hidden;"]





**UPDATE**: Több kommentet is kaptam arról, hogy a magyarországi járatok száma alacsonyabb, mint kellene legyen. Ezért újra lefuttattam az adatbányászatot, ezúttal csak az utóbbi két hét (március 11-24) járatait véve figyelembe. A bejegyzést ennek megfelelően módosítottam. A megfigyelt kis változások oka kétrétű: vannak társaságok, akik az utóbbi egy-két hónapban növelték a járatszámuk egyes útvonalakon, de főként azt fedeztem fel, hogy az airportia nem tartja meg a repülési logokat minden légitársaságtől egyforma arányban. Például a Lufthansa járatok csak utóbbi hónapra maradnak meg, míg a Wizzair járatok három hónapra visszamenőleg. Ezúton is köszönet a kommentelőknek, hogy rájöhettem erre a turpisságra. Mégegyszer tehát: a bejegyzés mostmár a friss számokat tartalmazza.





**ADATOK + KÓD:** Ebben a bejegyzésben Románia és Magyarország repülőtérképét készítettük el és vizsgáltuk. Az eredmények:


    Románia interaktív repülőtérképe adatvizualizáció (interaktív | statikus)
    Magyarország interaktív repülőtérképe adatvizualizáció (interaktív | statikus)
    Románia belföldi járatainak interaktív repülőtérképe adatvizualizáció (interaktív | statikus)
    Romániai járatok célországai buborékdiagram (interaktív | statikus)
    Magyarországi járatok célországai buborékdiagram (interaktív | statikus)
    Országos járatszám - diaszpóra log-log plot (interaktív | statikus)
    Romániai járatok célvárosai buborékdiagram, városok szerint (interaktív | statikus)
    Magyarországi járatok célvárosai buborékdiagram, városok szerint (interaktív | statikus)
    Romániai járatok célvárosai buborékdiagram, légitársaságok szerint (interaktív | statikus)
    Magyarországi járatok célvárosai buborékdiagram, légitársaságok szerint (interaktív | statikus)
    Városi járatszám - diaszpóra log-log plot (interaktív | statikus)
    Romániai légitársaságok buborékdiagram (interaktív | statikus)
    Magyarországi légitársaságok buborékdiagram (interaktív | statikus)
    Romániai járatböngésző buborékdiagram (interaktív | statikus)
    Magyarországi járatböngésző buborékdiagram (interaktív | statikus)
    Univerzális járatböngésző buborékdiagram (interaktív)


A bejegyzéshez az airportia adatbázis adatait használtuk fel. Első lépésként Jupyter Python munkafüzetekkel, requests és pandas segítségével letöltöttük az utóbbi 10 hét érkezéseit és indulásait az összes romániai illetve magyarországi repterekre (érkezés, indulás). Ezután az érkezés és indulástáblákat ezekkel (HU, RO) a munkafüzetekkel normalizáltuk, illetve a célreptereket és városokat geolokalizáltuk. A geolokalizációt a Google Maps Geocoding API és pyegocoder Python bővítőcsomag segítségével hajtottuk végre. Az így kapott adatokat JSON formátumba dolgoztuk fel ezekkel (HU, RO) a munkafüzetekkel. A repülőtérképeken tortadiagramok d3.js és SVG nyelvben vannak rajzolva, ebben ez a blogbejegyzés is segített. A színeket colorbrewer segítségével választottuk és a Righteous betűtípust használtuk. A buborékdiagramokat d3plus nyelvben rajzoltuk. Ehhez a bemeneti fájlokat ezzel és ezzel a Jupyter munkafüzettel formáztuk meg. A teljes adatbányászat, formázás, illetve a bejegyzés megírása és szerkesztése 48 munkaórát vett igénybe.