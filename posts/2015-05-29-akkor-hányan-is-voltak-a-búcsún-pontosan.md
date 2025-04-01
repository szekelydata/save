---
title: Akkor hányan is voltak a búcsún? Pontosan?
date: 2015-05-29 02:21:04
---


Újabban nagy divat a nagy tömegeket megmozgató eseményeken résztvevők számát alul/felüllicitálni, a propagandaszekér rúdjának irányától függően. A teljesség igénye nélkül, elég csak a januári, párizsi eseményekre vagy az őszi, magyar kormányellenes tüntetésekre gondolni. Vagy közelebb hozzánk, a tavalyi, Székelyek Nagy Menetelésére. Az ott résztvevők száma 15000-től 120.000-ig a teljes skálát átölelte.  És ez alól persze a Csíksomlyói zarándoklat sem kivétel. De pontosan hogy is jutnak az ujságírók/statisztikusok ezekhez a számokhoz? - Nem, azt valójában nem tudom. De bemutatok nehány módszert az adatok szemszögéből.



A szombati zarándoklat médiavisszhangja "százezres" tömegről beszélt, ám az nem teljesen egyértelmű, hogy hány százezer. A hazai és anyaországi média orgánumok több száz, százötven- és százharminc ezerre teszik ezt a számot. Nézzük hát hogyan pontosíthatóak ezek az adatok. Három, egymástól teljesen eltérő modszert fogunk alkalmazni és végül összehasonlítani az eredményeket.




    Jacobs eljárás
    Folyamat-alapú eljárás
    Képfelismerő szoftveres eljárás


Ott van még természetesen negyediknek a direkt számlálás két módszere is: Ha a zarándokoknak egy bejárató-kapun kellene áthaladniuk, vagy valaki mondjuk manuálisan megszámolná egy nagy felbontású fényképen a résztvevőket, akkor nagyon pontos adatokat kapnánk. Ezeket a megközelítéseket egyelőre mellőzzük :)







A tömegek számlálására az újságírásban és hivatalos statisztikákban bevett módszer a múlt század elején kidolgzott és az  amerikai Million Man March után új lendületet kapó Jacobs eljárás (erről kiváló részletes leírások találhatóak angolul itt és itt). Jacobs szerint a tömegeknek az a fő karakterisztikája, hogy egy tetszőlegesen kiválasztott személy hány négyzetmétert (eredetileg négyzetlábot) foglal el az esemény felületéből. Így a tömegeket a következő három kategóriába sorolhatjuk:




    0.23 négyzetméter / személy: Sűrű tömeg, válltól vállig, koncert első sorai.
    0.42 négyzetméter / személy: Kezelhető tömeg, néhányan ülnek, koncert hátsó sorai.
    0.93 négyzetméter / személy: Laza tömeg, majdnem mindenki ül.


A kérdéses területet ezután kisebb cellákra osztjuk, annyira kicsikre, hogy az egyes cellákban elhelyezkedő emberek eloszlása homogénnek tekinthető legyen. A terület feloszátsát számos szabad forráskódú GIS eszközzel végrehajthatjuk, én ezt használtam. Persze a felosztáshoz szükségünk lesz egy fotóra/videóra, ami körbeüleli lehetőleg az egész eseményt - én ezt használtam. A szélső pontok pozícionálásában nagyban segített az erdő "szöge" :)



[caption id="attachment_646" align="aligncenter" width="633"] 2015-ös csíksomlyói búcsún résztvevők teljes kiterjedése[/caption]

Az így kapott terület nagysága 17.14 hektár, azaz 171400 négyzetméter. Ezen a területen vannak sűrű és kevésbé sűrű részek. A tömeg sűrűségének pontos meghatárzosához nagy segítséget nyújt, ha van egy műholddal vagy drónnal készített merőleges felvételünk, vagy legalább egy olyan, ami egy magaslatról készült. Ellenkező esetben lehet egy távolról készült fotót vagy videót alkalmaznunk - ahogy most is tettem - észben tartva, hogy perspektíva szabályai miatt az egységnyi területen elhelyezkedő emberek száma így többnek látszik, mint az valójában.



[caption id="attachment_647" align="aligncenter" width="507"] 2015-ös csíksomlyói búcsún résztvevők felosztása[/caption]

A teljes területet a képen látható 7, nagyjából egyenletes tömegsűrűségű részre osztottuk, a következő méretekkel:
**1.** 56700 négyzetméter - sűrű tömeg, 0.3 négyzetméter/személy : 189000 fő
**2.** 8941nm - közepesen sűrű tömeg, 0.5 nm/személy: 17882 fő
**3.** 15300 nm - laza tömeg, 0.9 nm/személy: 17000 fő
**4.** 5617 nm - közepesen sűrű tömeg, 0.5 nm/személy: 11234 fő
**5.** 7728 nm - laza tömeg, 0.9 nm/személy: 8587 fő
**6.** 5519 nm - közepesen laza tömeg, 0.7 nm/személy: 7885 fő
**7.** 70500 nm - néhány ember, 3 nm/személy: 23500 fő



Figyelembe véve, hogy a TV-stáb, valamint a mentős részleg kb. 40 autónyi (15 nm) helyet foglalt el az 1-es régióban, valamint azt, hogy a színpad és a mögötte levő terület 650 nm a 2-es régióban, az így kapott résztvevők száma 275088 - 40*15/0.3 - 650/0.5 = **271788**.



Egy másik számítási módszer a **folyamatkövetés**. Képzeljünk el egy medencét, amibe vizet engedünk, de az csakis egyetlen csapból folyik. Tudjuk a csap átmérőjét és egy gumikacsával azt is meg tudjuk mérni, hogy milyen gyorsan áramlik be a víz a medencébe. Így egy egyszerű számítással meg tudjuk határozni, hogy egy adott időtartamon belül mennyi víz került a medencébe. Egy videó segítségével (mint ez a timelapse) ugyanígy tömegeket is mérhetünk. **Timelapse** (gyorsított idejű videó) esetén persze ez egy kicsit trükkösebb, hiszen pontosan nem tudjuk a valós idő telésének sebességét, ami ebben az esetben több, mint 1másodperc/másodperc. Viszont azt majdnem pontosan tudjuk, hogy mettől meddig tartott az esemény, mikor volt a szentmise, és mikor kezdtek el hazaszállíngózni az emberek. Feltételezve, hogy a videó készítője egyenletesen gyorsította fel a timelapse videót (vagy egyenletes eloszlásban vágta össze az állóképeket), meghatározhatjuk a gyorsítás sebességét és azután kiszámolhatjuk a valós folyamatértékeket.



A videó még a reggeli, felhős órákban kezdődik, amikor még nagyon kevesen tartózkodnak a nyeregben. Ez az időpont 8-9 óra körülre tehető. Az emberfolyamot figyelve a felvétel közepén, a szentmise kezdete 40-45 másodperc körülre tehető a videóban, és kb. 55-ig tart. Ez valós időben 12:30-tól kb. 14:00-ig tart. 1:15-re majdnem mindenki elhagyta a nyerget, és valószínüleg délután 4-5 óra fele járhat. Ezeket a számokat figyelembe véve bátran kijelenthetjük, hogy a videóban **egy másodperc 6-7 perc**nek felel meg a valóságban. 6 és fél perccel számolva 390-szeres gyorsítást kapunk, ami nagyon közel van a standard 400-szoroshoz. További számításainkban ezt az értéket fogjuk használni.



Mivel a csíksomlyói nyeregbe nem csak egy úton lehet eljutni, ez megnehezíti egy picit a számításainkat. A videón figyelemmel követhetjük, hogy egy központi artéria kivételével, szétszórtan történik az emberáramlás. A videó szuperlassításával megfigyelhetjük, hogy a középső artérián haladó embereknek **0.7-0.9** videómásodpercbe telik eljutni az oltártól az erdő aljába. Ez valós időben 5 perc 20 másodpercet jelent a 210 méteres táv megtételére, azaz **2.36 km/h**-ás átlagsebességet. A közéspső, 8 m széles artérián közlekedő emberek sűrűsége persze nem konstans, hanem időben vátozó. A videó kezdetétől 15 mp-ig laza tömeg, utána 25 mp-ig közepesen laza, 35-ig közepesen sűrű, majd 42-ig sűrű, amikor ugyanis leáll a mozgás - és kezdetét veszi a szentmise. Az utóbbi két szegmensben a sebesség is csökken, **1**, majd **1.1** videómásodpercre.



[caption id="attachment_648" align="aligncenter" width="968"] 2015-ös csíksomlyói búcsú tömegdinamikája[/caption]

Ezeket a számokat figyelembe véve arra jutunk, hogy a középső artériát használva, reggeltől a szentmise kezdetéig **134232** személy jött a nyeregbe. Ezen adatok alapján a nem a viszgált ösvényt használók számát is meg tudjuk adni, hozzávetőlegesen. Figyelembe véve, hogy a nyereghez vezető út (Kissomlyó utca) keresztmetszete (a keresztutat és a Barátok feredője felől jövőt is beleértve) körülbelül kétszerese a vizsgált artériának, ezzel a módszerrel a búcsún a résztvevők számát **268464**-re becsülhetjük, ami meglehetősen közel van a Jacobs-eredményhez. A videó folytatásában a lejövetel folyamatsebességét vizsgálva az előbbi szám ugyancsak visszaigozolódik.



Az utolsó megoldás a direkt módszer, amikor mindenkit "név szerint" számba veszünk. Ha a kézi számlálás emberfeletti igénybevétellel jár, akkor használjunk egy softvert a "piszkos munkára". Ehhez szükségünk van egy gigászi felbontásu fényképre - akkorára, amelyen az arcok tisztán kivehetően látszanak. Bár lehetséges, hogy az idei zarándoklaton is készült ilyen felvétel, az alábbi elemzéshez a tavalyi búcsún készült felvételt fogom használni. Az eljárás hasonló a bejegyzés elején már bemutatott Jacobs-módszerhez, de a résztvevők sűrűségének kiszámítása automatikusan történik, arcfelismerő szoftver alkalmazásával. Ehhez természesen először fel kell darabolnunk a gigapixeles képet kisebb darabokra, ugyancsak a homogén eloszlás elvét követve. Ehhez írtam egy rövid algoritmust, ami letölti a gigapixeles képet (gigapan-t) és utána feldarabolja.



[caption id="attachment_650" align="aligncenter" width="1187"] Csíkszomlyó 2014 Gigapanoráma felosztás[/caption]

Az így kapott 512 x 256 = 131072 kép mindegyikén lefuttatunk egy automatikus arcfelismerő szoftvert. Én OpenCV-t és ezt az IPython munkafüzetet használtam.



[caption id="attachment_651" align="aligncenter" width="371"] Gigapanoráma arcfelismerés példa[/caption]

Rögtön kiderül, hogy a probléma ezzel a megközelítéssel az, hogy sok résztvevő esernyő alatt ül, egymás mögött áll vagy nem néz a kamera felé, így meglehetősen nehéz az arcukat felismerni. Más esetekben az arcok pontosan a nagy kép vágásvonalain fognak elhelyezkedni és a felszeletelt képeken csak félarcokat kapunk. Arról nem is beszélve, hogy az oltár mögött állók eleve háttal állnak a kamerának és sokkal közelebb hozzá. Ezért ez a módszer, bár jónak és elegánsnak ígérkezett az elején, sajnos nem vezetett értelmezhető eredményekhez, még hosszas beállítások után sem. Számos statisztikai szűrés után arra jutottam, hogy a képfelismerő szoftver a 2014-es búcsún 20 és 50 ezer arc között számolt. Figyelembe véve a fenti képen az arcfelismerés átlagos hatásfokát (a többi fotón is hasonló), a valós szám 4-6-szor nagyobbra tehető, azaz 150000-200000 fő. Ezután ehhez még hozzáadódnak a háttal állók, ami az idei adatok alapján kb. a teljes tömeg egyötöde, ami végül az előbbi két módszerhez közeli 180-250.000 résztvevőt eredményez.







Az idei búcsún tehát - az adatelemzés alapján - körülbelül **270.000**-en vettek részt - és ez jóval eltér mind a magyar, mind pedig a román média becsléseitől. És ez a szám valószínüleg nem változik gyökeresen a többi években sem.





**UPDATE: **Többen jeleztétek kommentben, hogy a templomnál, kápolnánál maradó, erdőbe behúzódó tömeg kimaradt az elemzésből. Valóban, az erdőben résztvevőket azért mellőztem, mert ők kompenzálnák a hátrábbi sorokban levő kisebb sűrűséget az 1-es szektoron belül. Mert az itteni embersűrűség természetesen kisebb, mint mondjuk a színpad előtt állók.



Ugyanakkor, részben a cikk népszerűségének köszönhetően időközben nyilvánossá vált egy általam a fő cikkben is hőn áhított légi felvétel (nyugatról, és egy másik északról). Tapasztalt koncertszervezőktől azt is megtudtam, hogy az 1-es szektorra számolt embersűrűség csak az első sorokra igaz, a hátrébb már alacsonyabb értékekkel kell számolnom. Természetesen a folyamatmodell becslései nem változnak, de a Jacobs-módszer a következőképpen frissül:



**1.** 56700 négyzetméter - sűrű tömeg, 0.3 négyzetméter/személy : 189000 fő



**1a oltár környéke.** 25350 négyzetméter - sűrű tömeg, 0.3 négyzetméter/személy : 84500 fő
**1b középsáv.** 11175 négyzetméter - közepesen sűrű tömeg, 0.5 nm/sz : 22350 fő
**1c erdő alatt.** 11175 négyzetméter - laza tömeg, 0.9 nm/sz : 12417 fő
**1d északi oldal** 9000 négyzetméter - néhány ember, 3 nm/sz: 3000 fő



Összesen: 122267 fő. Ehhez még hozzáadódik:



A **kegytemplom** és környéke: 2500 nm - sűrű tömeg, 0.3 nm/sz: 7500 fő
Az **erdő** 50 méteres sávban, az 1-es szektor mentén: 19400 nm - nagyon laza tömeg, 1.8 nm/sz: 10778 fő
Az **erdő** 50-től 1 méterig fokozatosan elvékonyodó sávban a 4-es és 6-os szektorok mentén: 4590 nm  - nagyon laza tömeg, 1.8 nm/sz: 2550 fő
Az **erdő** a 2-es szektor északi részén, 50 méteres sávban: 4100 nm - laza tömeg, 0.9 nm/sz: 4556 fő



Azaz a kezdeti 189000-es becslés 147661-re módosul. Ez nettó -41339 személyt jelent, ami a Jacobs-módszer végső értékét **230449**-re módosítja. Figyelembe véve, hogy a folyamatáramlás-elemzést nem befolyásolják a fenti adatok jelentősen (kivétel a templomnál maradtak), a végső becslésérték e két módszer középarányosa: **249465**. Ez a szám már közel áll az arcfelismerő módszer durva becsléséhez is, ami arra enged következtetni, hogy a 2015-ös csíksomlyói búcsún **kb. 250 000 ember** vett részt.** **





**ADATOK + KÓD:** Az adatelemzés központi forrásai Incze András Lajos timelapse videója és a transilvanart.ro gigapanorámája voltak. Ha tetszett a bejegyzés, vagy bármilyen kérdésed, hozzáfűznivalód van, **Like-olj, Oszd meg, Kommentelj**, és **Iratkozz fel**!