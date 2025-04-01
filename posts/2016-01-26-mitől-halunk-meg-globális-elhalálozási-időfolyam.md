---
title: Mitől halunk meg? - Globális Elhalálozási Időfolyam
date: 2016-01-26 00:24:22
---


Olvasd el a globális, bővített bejegyzést is (angolul). 
There is also an English version of this post, for the world.
A tavalyelőtt megvizsgáltuk székelyföldi lakosság összetételét kor, vallás és gazdaság szempontjából. 2015-ben megszámoltuk, hogy hányan jöttek el a csíksomlyói búcsúra és azt is elkezdtük feltérképezni, hogy honnan - azaz pontosabban, hogy hol élnek az elszármazottak a nagyvilágban. Tudjuk már, hogy hányan élünk, hol, és (hamarosan) azt is hogy hogyan. Csak azt nem tudjuk, hogy hogyan halunk meg. Ezidáig.


Ebben a bejegyzésben nem egy kifejeztten vidám, de annál fontosabb adatsort tanulmányozunk:  Székelyföld (valamint Románia és Magyarország) elhalálozási okainak és betegségeinek statisztikáit hasonlítjuk össze a világ több országáéval. In medias res, rögtön az elejére be is illesztettem az erről készült adatvizualizációt (**interaktív - teljes képernyő, statikus**). Ez egy meglehetősen komplex vizualizáció, sok opcióval és gombbal, temérdek adattal és gyönyörű animációkkal - a d3plus csomagban, a d3 adavizualizációs nyelv Alex Simoes által továbbfejlesztett változatában készült, magyarosítás után.


[iframe src="http://szekelydata.csaladen.es/egeszseg/" width=760 height=650 style="overflow:hidden;"]


*In this post I am bringing you a causes of death (COD) visualization, depicting the evolution of causes of death in Székelyland, Romania and Hungary throughout the years, for different age groups. The visualization has two parts a stacked timeline chart and a time-keyed treemap (both beautifully crafted in d3plus), and it contains data for most of the countries of the world (WHO database).*





A vizualizáción az elhalálozások okait tűntettük fel, valamint ezek változását egy emberöltő során. Az alábbi színkód rendszert használjuk a betegségek és más okok megjelölésére, amit az Egészségügyi Világszervezet (WHO) által meghatározott standardok szerint (BNO-10) alakítottunk ki. A nyílt adatok forrása a WHO elhalálozási adatbázisa volt, amit a Washingtoni Egyetem GHDx programja támogat. A székelyföldi adatokat a romániai adatokból a Nemzeti Statisztikai Hivatal részadatai alapján extrapoláltuk.







Daganatok



A szem es függelékeinek betegségei



A csont-izom rendszer és kötőszövet betegségei



Az emésztőrendszer betegségei



A bőr és a bőr alatti szövet betegségei



Endokrin, táplálkozási és anyagcserebetegségek



Az idegrendszer betegségei



A perinatális szakban keletkező bizonyos állapotok



Veleszületett rendellenességek, deformitások és kromoszómaabnormitások



Mentális és viselkedészavarok



A légzőrendszer betegségei



Terhesség, szülés és a gyermekágy



A morbiditás és mortalitás külső okai



Máshova nem osztályozott panaszok, tünetek és kóros klinikai és laboratóriumi leletek



Fertőző és parazitás betegségek



A vér és a vérképző szervek betegségei és az immunrendszert érintő rendellenességek



Az urogenitális rendszer megbetegedései



A keringési rendszer betegségei



A fül és a csecsnyúlvány megbetegedései



[caption id="attachment_819" align="alignnone" width="783"] Székelyföld elhalálozási időfolyama[/caption]
Halálokok eloszlása
Időfolyam vizualizációk
A vizualizáció főábrája azt mutatja meg, hogy 20, 25 vagy akár 85 évesen milyen betegségben (vagy más okban) van esélyünk elhunyni - ponstosabban, **mekkora esélye van az egyes betegségeknek ****halált okozni**, valamint hogyan változnak ezek arányok az életünk során. Ezt a típusú megjelenítést **időfolyam**nak (sávozott grafikon, stacked plot) hívják, mivel az adatsávok olyanok, akár egy-egy kanyargó folyó. Az adatok a világ legtöbb országát és az utóbbi 15-20 évet ölelik fel, a megjelenített adatsor **Székelyföld 2012**-es értékeit rajzolja ki. Ez több szempontból is fontos, egyrészt segít tudatosítani az egyes betegségek súlyosságát, másrészt rávilágít arra, hogy a testünk melyik részére az életünk melyik szakaszában kell jobban odafigyeljünk. Először csak a halálokok eloszlásának statsztikáit tanulmányzzuk, majd később megnézzük magukat az értékeket is. De még ezelőtt fontos aláhúzni hogy ez a rész az adott korcsoporton belül eső elhunytak számára vonatkozik és az ezen belüli *eloszlást* mutatja - természesetesen *nominális érték*ben (esetek számában) mérve sokkal több ember hal meg 85 éves korában, mint 15 évesen, erre majd később visszatérünk.


A főábráról leolvashatjuk , hogy a székelyföldi mortalitásnak **három fő oka** van: eleinte **külső okok** miatt, majd később **daganatok**ban és a **keringési rendszer** **betegségei**ben van a legnagyobb esélyünk elhunyni. Talán meglepő, de a rettegett rák maximum az elhalálozások egyharmadáért felelős, főként a a középkorúaknál - ebben persze az az ijesztő vetület is benne van, hogy a rákos betegség nem nyúlik túlságosan hosszúra. Ami a leginkább szembeötlő, az a keringési rendszer betegségeinek elsöprő részaránya idős korban: 80 év fölött majdnem mindenki valamilyen szív- vagy érrendszeri betegségben hal meg. Ezt úgy is értelmezhetjük, hogy a szervezet e rendszere öregedik el a leghamarabb, vagy - egy morbidabb, de talán annál helyénvalóbb megközelítésben - a középkorúaknál még a keringési rendszer megbetegedéseivel részarányosan jelentkező, hasonlóan potens rákos betegségek gyorsabban fatális kimenetelűek (vagy gyorsabban gyógyulandóak, és idősebb korban nem, vagy csak ritkábban alakulnak ki) és idős korra már nem "maradnak" csak a tartósabb szív és érrendszeri betegségek.


A fiatalokkal (10 és 40 év között) főként **külső okok** végeznek, és a fiatal férifak elhalálozási aránya messzemenően nagyobb a nőkénél. Az interatív térképen az egyes elmekre kattinva betekintést nyerhetünk a betegségcsoportok felépítésébe.




[caption id="attachment_856" align="aligncenter" width="785"] Székelyföldi férfiak elhalálozásának külső okai[/caption]
A székelyföldi férfiak tetemes része **közlekedési balesetek**ben huny el, illetve 15-18 éves kortól az **öngyilkosság** sem ritka. De az már meglepő, hogy az öngyilkosság nem csak a fiatalokat érinti, hanem a teljes társadalmi réteget athatja és 80 év fölött is előfordul. Ugyanakkor, bár a székely virtus méltán híres, az összetűzések ritkán fatálisak - **ezer halálból** csak **egy testi sértés** következménye, sokszor gyakoribb az esés, illetve vízbefulladás általi halál.



Hierarchiatérképek
A többi betegség- és okcsoport felépítése nem ennyire sokszínű és dinamikus. Ezért ezeket elgéséges a lakosságra teljese egészére nézve vizsgálni, egy **hierarchiatérképpel**. A vizualizáció jobb felső sarkában a betegségek és halálokok hierarchikus térképét hívhatjuk elő, amely a teljes lakosságra eső betegséglebontást mutatja meg. Ez egy egyszerűbb reprezentációja az adatoknak, mint az időfolyam,  mellőzi a kor-specifikusságot, de az adatokat két dimenzióban, területekként jeleníti meg, így felhasználóbarátabb és szembeötlőbb, mint egy egyszerű vonalgrafikon (ennél a bejegyzésnél már használtunk ilyen típusú adatmegjelenítést). A lenti menüben válasszuk ki a *betegségek* szerinti felbontást.




[caption id="attachment_841" align="aligncenter" width="783"] Székelyföld elhalálozási hierarchiatérképe[/caption]
A hierarchitérképről jól kivehető, hogy a teljes lakosság körében a **keringési rendszer betegségeibe a lakosság 55%-a hal bele**, míg **rákba 21%**. Azaz Székelyföldön több mint **minden második** halál egy szív- és érrendszeri betegség folytán történik: szívinfarktus, szélütés (stroke), szívelégtelenség, szívizomelhalás érelmeszesedés és különböző vérzések a leggyakoribb halálokozók, ezeket követi a **tüdőrák**, valamint a **máj** és a **légzőrendszer** más betegségei. A légzőrendszeri betegségek (nagyrészt tüdőgyulladás illetve a javarészt **dohányzás** miatt kialakuló krónikus (idült) légúti betegségek, mint az asthma vagy a bronchitis) az elhalálozások **6,8%**, a **külső okok** **6%** (autóbalesetek és öngyilkosság), míg az emésztőrendszer betegségei (szinte kizárólag májcirózis - májzsugorodás, krónikus **alkoholfogyasztás **következményeként) **4,3%**-ért felelősek.




[caption id="attachment_842" align="aligncenter" width="760"] Székelyföldi rákos megbetegedések válfajai nemek szerint[/caption]
A keringési rendszer esetén a szívinfarktus, stroke, illeve magas vérnyomás majdnem egyenlő arányban van jelen úgy a nőknél, mint a férfiaknál. De megéri közelebbről megvizsgálni a különbüző ráktípusok előfordulását, nemek szerint. A nőknél a mellrák a esetek 16%-ért felelős, a tüdőrák 11%. A férfiak esetében a **tüdőrák** aránya a daganttípusok között **27%, négyből egy**. A vastagbél és a végbél rosszindulatú daganatai a rákos megbetegedések folytán bekövetkezett elhalálozások 11-12%-ért felelősek, mindkét nemre nézve. Igen, ez egy tökéletes nap felhagyni a dohányzással...



Országos és globális összehasonlítás
Halálokok eloszlásai egyes országokban
De hogyan festenek ezek az adatok **Románia**-szinten, illetve a világ többi országaiban?




[caption id="attachment_844" align="aligncenter" width="760"] Románia, illetve Magyarország elhalálozási időfolyama[/caption]
Az országos statisztikák természetesen nem merőben eltérőek a székelyföldiétől, de érdemes megemlíteni, hogy míg a mortalitás **külső okai** országos szinten **2%**-ot tesznek ki, regionálisan ez az arány már **8,3%**, jórészt a több öngyilkosság és halálos baleset miatt. Ez a trend sajnos évekre visszamenőleg is igaz. Ugyanakkor a **légzőrendszer** betegségei országosan **4,1%**-ot, míg a hidegebb Székelyföldön **7,7%**-ot jelentenek. Az idegrendszeri és keringési betegségek aránya viszont országos viszonylatban nagyobb a székelyföldinél.


A tüdőgyulladás **Romániában** az egyik legfőbb oka a csecsemőhalandóságnak, míg ez **Magyarországon** mára már majdnem teljesen vissza lett szorítva. Bár a magyarországiak esetében is (ahogy amúgy a világ legtöbb országában) a halál legfőbb oka a keringési rendszer megbetegedése, az öregek esetében ez az arány kisebb, mint a Romániai lakosoknál. Magyarországon a fertőző betegségek sokkal jobban vissza vannak szorítva (kb. 10-szer kevesebb eset a feleakkora lakosság ellenére) , mint Romániában, illetve a "Máshova nem osztályozott panaszok" kategória is sokkal kisebb. **HIV**-betegségben Magyarországon 2012-ben 15-en hunytak el, míg Romániában 175-en. Tüdőgümőkórban  (**TBC**) 156-on, illetve 1220-an. (Fun fact: 1900-ban a Magyar Királyságban 63 632 áldozata volt a "tüdővész"-nek).




[caption id="attachment_845" align="alignnone" width="760"] Románia, illetve Svédország elhalálozási időfolyama[/caption]
A hosszú életű Skandináv államok esetében a keringési rendszer betegségei az elhalálozások feléért sem felelősek, még 95 éves korban sem! Csak összehasonlításképpen nézzük **Svédországot, **ahol a szív- és érrendszeri megbetegedések az elhalálozások 38%-ért felelősek, szemben Románia 60%-val. A derék svédek **6,4%**-át viszont a "**Mentális és viselkedészavarok**" kategóriába nagyvonalúan besorolt **drogtúladagolások** viszik el. Ez az arány **Amerikában 5,8%, Magyarországon 2,3%, Romániában 0,07%** valamint a könnyűdrogokat megengedő **Hollandiában 6,1%**.




[caption id="attachment_849" align="aligncenter" width="760"] Székelyföld, illetve Amerika elhalálozási időfolyama[/caption]
Bár **Amerika** elhalálozási arányai még kiegyensúlyozotabbak, mint Svédországé az idősek esetében és a rákos megbetegedések ritkábban fatális kimenetelűek, a gyorskaja hazájában a **cukorbetegség** a halálok **4%**-ért felelős. **Székelyföldön** ez az arány **2%** alatt van, **Mexikóban 15%**. A vastág sárga csík az **Alzheimer-kór**, ami az összes halál **5,7%**-ért felelős.



Halálesetek száma és várható élettartam
Az adatvizualizáción eddig a betegségek és okok eloszlását vizsgáltuk, főként a teljes lakosságra tekintve (hierarchikus térképek), illetve egy adott korosztályon belül előforduló halálesetek arányában (időfolyamok). Ugyanakkor a menüben az *Értékek*-re kattintva megtekinthetjük a konkrét **esetek számát**, így vizuális betekintést nyerve a **várható élettartam** foglamába.




[caption id="attachment_846" align="aligncenter" width="783"] Székelyföld elhalálozási időfolyama - értékek[/caption]
Ezen az ábrán a 2012-ben előfordult székelyföldi haláleseteket tűntettük fel, a halálokok szerint. Az így keletkezett valószínüséggörbe (ez egy egéséges lakosság esetében béta vagy log-normális eloszlást követ) középarányosa - *i.e tömegközéppont:* azaz *ha az ábrát fémből elkészítjük és megtaláljuk azt a pontot az életkor vízszintes tengelye mentén, ahol az öntvényünk pontosan egyensúlyban áll és nem dől el sem balra, sem jobbra, ez a pont fogja jelölni a valószínüségközepet* - jelöli a várható élettartamot. Ez az érték **Románia-szinten** jelenleg **74 év**, **Székelyföldön** egy** picivel magasabb**. Az halálesetek számát tekintve 80 éves kor körül tetőznek és a 95 évet csak nagyon kevesen érik el - és akik igen, azokról a fenti vizualizációk alapján tudjuk, hogy 90%-os eséllyel egy keringési rendszeri betegségben fognak elhunyni. Hosszab életű országok esetében a fenti ábra merőben másként fest.




[caption id="attachment_852" align="aligncenter" width="760"] Kolumbia, illetve Japán elhalálozási időfolyama - értékek[/caption]
**Japánban** a 95 évesek csak felannyian hunynank el (az esetek számát tekintve), mint a 80 évesek - és ezeknek az elhalálozásoknak okai (bár viszonylag sok a meghatározatlan ok) majdnem egyenletesen oszlanak el a betegségcsoportok között! A "görbecsúcs jobb oldala "vastagabb" Japán esetében, így a tömegközéppontja majdnem a csúccsal esik egybe! - így az ország várható élettartama **84 év**.


Kolumbia esetében az elhalálozási görbe nem követi a megszokott formát (béta vagy log-normális eloszlás). Ennek az oka a nagy számú fiatal férfi életét követelő (javarészt a drogcsempészethez köthető) belső konfliktusok, erről írtunk már itt. 2010 és 2012 között **több** Kolumbiai fiatal srác vált **testi sértés** áldozatává, mint a teljes lakosság körében **rák** által szedett áldozatok száma. Hogy jobban betekinthessünk ebbe a jelenségbe, meg kell vizsgálnunk a halálokok dinamikáját, azaz hogy hogyan változik az ehalálozási időfolyam összetétele **évről évre**.



Halálokok dinamikája
[caption id="attachment_850" align="aligncenter" width="783"] Kolumbiai férfiak dinamikus elhalálozási időfolyama 1997 és 2012 között[/caption]
Láthatjuk, hogy a kolumbiai helyzet valójában a 2010-es évek végére valamelyest mérséklődőtt, hiszen 1997 és 1999 között a gyilkosságok és a halál egyéb külső okai többet számláltak, mint a keringési rendszer betegségei és a daganatok **együttvéve**. Ez azt jelenti, hogy 1997-ben egy **25-éves srác**nak pontosan ugyankkora esélye volt meghalni, mint egy** 75 éves úr**nak, és ez a halál több mint **90%**-os eséllyel** testi sértés** által következik be! A trend csökkenést mutat, de még 2012-ben is többen lettek 20-30 évesen testi sértés áldozatai, mint a 70-80 évesen bármilyen keringési rendszeri betegségben elhunytak.




[caption id="attachment_851" align="aligncenter" width="783"] Székelyföld dinamikus elhalálozási időfolyama 1999 és 2012 között[/caption]
A székelyföldi adatokra visszatérve azt vehetjük észre, hogy az elhalálozások száma évről évre növekedik, azaz stabil vagy csökkenő születések mellett a lakosságunk csökkenőben van (ahogy már itt is is említettük). Ugyanakkor a várható élettartam 70 év alól 75 év fölé emelkedik. Ahogy a kétezres évek elején negyvenéves generáció lassan öregedik, egyre vastagdik a daganatok, cukorbetegség, illetve emésztőrendszeri és idegrendszeri problémák kategóriája is.


Bár minden bizonnyal ebben az adatsorban és a hozzá tartozó interaktív adatvizualizációban még rengeteg lecke található, azt kétségkívül levonhatjuk következtetésnek, hogy Székelyföldön, Romániában, Magyarországon, de talán a világ bármely pontján nagyobb figyelmet kell fordítanunk a **keringési rendszerünk megbetegedéseire**. Bár sok fatális betegség az öregedési folyamat velejárója, egyes országok mégis viszonylag alacsonyan (50% alatt) tudják tartani az ebből fakadó elhalálozásokat. Bár orvosi tanácsot nem vagyok kvalifikált adni, ez természetesen ez összefügg a szalonnaországi diétánkkal - úgy a zsírgazdag ételek, mint a vöröshús, illetve feldolgozott hústermékek fogyasztásával - és életvitelünkkel. A **káros szenvedélyek** is rivaldafénybe kerültek, úgy a dohányzás, mint a krónikus alkoholfogyasztás jelentős számú elhalálozásért (10% fölött) felelős, rákhoz vezetve vagy egyéb betegségek formájában, de az is említésre méltő, hogy sok téren jobban állunk, mint más, sokszor jelentősen gazdagabb államok (testi sértések, cukorbetegség, drogfüggőség, idegrendszeri és mentális megbetegedések).





**UPDATE: **Platon Arnold barátom javaslatára, a romániai adatokat újrahasznosítva elkészítettem egy Erdélyt, illetve Havasalföldet és Moldvát összehasonlító vizualizációt is.


A férfiak statisztikáit vizsgálva észrevehetjük, hogy bár az élettartam-eloszlás csúcsában nincsen különbség, a várható élettartam Erdélyben jóval magasabb mint az ország másik két regiójában (Bukarest nélkül). Ez annak tudható be, hogy az elhalálozási arány az **5-35** évesek körében szembetűnően magasabb a Kárpátokon kívül. A különbség minden oknál megfigyelhető, de különösen magas a külső okok esetében - mégpedig a **közlekedési balesetek** miatt! Azaz Erdélyben nem csak az egészségügyi ellátás alapszínvonla magasabb, hanem (bár ez néha nehezen hihető) a fiatal férfiú sofőrök is (sokkal) biztonságosabban vezetnek! 


UPDATE 2: **Az intra-romániai adatok UPDATE-ben közölt térképeinek kivágásába hiba csúszott, így a erdélyi, illetve moldvai és havasalföldi balesetekre vonatkozó következtetés *nem áll fenn*. Az összes többi megállapítás és az interaktív vizualizáción feltűnteített adatok is *helyesek *(Erdély + Moldva és Havasalföld dupla vizualizáció). Erdély, Székelyföld illetve Havasalföld és Moldva elhalálozási időfolyamai így néznek ki 1999-re és 2012-re:




[caption id="attachment_900" align="aligncenter" width="775"] Erdély, Székelyföld illetve Havasalföld és Moldva elhalálozási időfolyama - 1999-es értékek[/caption]

[caption id="attachment_899" align="aligncenter" width="775"] Erdély, Székelyföld, illetve Havasalföld és Moldva elhalálozási időfolyama - 2012-es értékek[/caption]


**ADATOK + KÓD:** A bejegyzést Nathan Yau, az egyik legnagyobb adatvizualizációs portál, a FlowingData szerkesztőjének ez a posztja inspirálta. Egy ehhez hasonló, részletesebb vizualizáció-csoportot tart fent a Washingtoni Egyetem által működtetett Institute for Health Metrics and Evaluation intézet is. A felhasznált nyílt adatokat az Egészségügyi Világszervezet (WHO) mortalitás-adatbázisából gyűjtöttük és a szervezet által meghatározott és globálisan elismert és alkalmazott standardok szerint (BNO-10, angolul ICD-10) alakítottunk ki. Az így bányászott adatokat JSON formátumba dolgoztuk fel ezzel a Jupyter munkafüzettel, pandas használatával. Minden ország JSON-ját egy zip-fájlba tömörítettük, amit később JSZip-pel csomagoltunk ki. Az ICD-10 adatbázis magyarosítását a magyar Wikipédia BNO-10 oldaláról ezzel a Jupyter munkafüzet segítségével végeztük, Csala Hunor-ral. A székelyföldi adatok kialakítása a romániai WHO-adatok, valamint a Nemzeti Statisztikai Hivatal romániai megyékre vonatkozó okok szerinti elhalálozási részadatai alapján ezzel a Jupyter munkafüzettel készült el. A bejegyzésben a *Székelyföld* megnevezés most kivételesen Hargita és Kovászna megyéken kívül a *teljes* Maros megyét magában foglalja.


Ebben a bejegyzésben a nagy újítás a **d3plus** csomag használata. Erre az MIT Observatory of Economic Complexity adatvizualizációja inspirált. A komplex adatvizualizáció a natívan gyönyörű animációkat és felhasználófelületi elemeket tartalmazó d3plus csomagban készült, ami az eddigi bejegyzéseknél használt d3 adavizualizációs nyelv az MIT-n, Alex Simoes által továbbfejlesztett változata. A kódot magyarosítottuk. Az adatok tisztogatása és normalizálása 60 órát vett igénybe. Ezután az interaktív vizualizációkat magába fogaló weboldalt, 48 óra alatt készítettük el. Az oldalon a blogra jellegzetes Righteous betűtípust használtuk. A háttérkutatás és a bejegyzés szerkesztése 16 órát tartott. Az végső eredmények:




 	**Globális Elhalálozási Időfolyam** interaktív adatvizualizáció (**interaktív - teljes képernyő, statikus**). Az összes bejegyzésben található statikus képet ebben az interkatív adatvizualizációban generáltuk. Ezek a következők:

 	Székelyföld Elhalálozási Időfolyama (**interaktív, ****statikus**)
 	Székelyföldi Férfiak Elhalálozásának Külső Okai (**statikus**)
 	Székelyföld Elhalálozási Hierarchitérképe (**interaktív, ****statikus**)
 	Székelyföldi rákos megbetegedések válfajai nemek szerint (**statikus**)
 	Románia és Magyarország Elhalálozási Időfolyama (**interaktív, ****statikus**)
 	Románia és Svédország Elhalálozási Időfolyama (**interaktív, ****statikus**)
 	Székelyföld és Amerika Elhalálozási Időfolyama (**interaktív, ****statikus**)
 	Székelyföld Elhalálozási Időfolyama - értékek (**interaktív, ****statikus**)
 	Kolumbia és Japán Elhalálozási Időfolyama - értékek (**interaktív, ****statikus**)
 	Székelyföld Dinamikus Elhalálozási Időfolyama 1999 és 2012 között (**gif**)
 	Kolumbia Dinamikus Elhalálozási Időfolyama 1997 és 2012 között (**gif**)


 	**UPDATE**

 	Erdély, illetve Havasalföld és Moldva elhalálozási időfolyama – 2012-es értékek (**interaktív**)


 	**UPDATE 2**

 	Erdély, Székelyföld illetve Havasalföld és Moldva elhalálozási időfolyama - 1999-es értékek (**gif**)
 	Erdély, Székelyföld illetve Havasalföld és Moldva elhalálozási időfolyama - 2012-es értékek (**gif**)



A fenti adatvizualizációban **a világ legtöbb országáról** fellelhetőek az elhalálozási adatok időfolyam, illetve hierarchiatérkép megjelenítésben, általában az utóbbi **15-20 évre visszamenőleg**. Angolul is elérhető **itt**.


A fő adatvizualizáció mellett elérhető egy **nagy felbontású verzió** is, ami az ICD (BNO) 10 kódrenszer főcsoportjai és betegségei (négyszámjegyű, 1-el kezdődő kódok) melett az egyes betegségek típusait illetve válfajait is tartalmazza (egy betű és utána két- vagy háromszámjegyű számkódok). Ez **nagyon memóriaéhes**, egy ország betöltése több percet is igénybe vehet.


Ugyanakkor elkészítettünk továbbá egy **összehasonlító felület**et, ahol két adatvizualizáció egyszerre, egymás melett jelenik meg.