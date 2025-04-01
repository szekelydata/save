---
title: 🏆 II. adatvizualizációs verseny
date: 2019-11-04 15:57:30
---


Az eredményekről szóló bejegyzést itt találod.

📣 Meghirdetjük az **II. székelydata adatvizualizációs versenyt****!** Akárcsak a **tavaly**, pályázat célja idén is az adatfeldolgozás és adatvizualizáció népszerűsítése **iskolások** és **friss egyetemista fiatalok** körében.

📤 Benyújtási határidő: **2019.12.31**

🏢 Az idei verseny újítása, hogy elindítunk egy **nyílt adatsor kategóriát** is: ide olyan **cégek** és **magánszemélyek** jelentkezését várjuk, akik úgy gondolják, hogy potenciálisan aranyat érő adatokon ülnek, de eddig még nem volt idejük/lehetőségük vizuálisan feldolgozni őket. Most **jelentkezhetnek** adatokkal egy **különdíj **díj felajánlása fejében!



🎨 A tavalyi verseny nagy sikernek örvendett, sőt, megszerveztük az első erdélyi adatvizualizációs mini-konferenciát is. 2020-ban meg szeretnénk ezt **ismételni**!



🧾 Szabályzat


    A pályázat célja az **adatfeldolgozás** és **adatvizualizáció népszerűsítése** **iskolások** és **friss egyetemista fiatalok** körében.
    A teljes pályázati kiírást, feltételeket, esetleges módosításokat, adatsort és bármilyen más ezzel kapcsolatos hírt a **székelydata** blogon nyilvánosságra hozunk. Fenntartjuk a szabályzat bármikori megváltoztatásának jogát.
    A pályázatra bárki jelentkezhet aki **1994.01.01** után született. Ezt az esetleges díjátvételkor igazolni kell.
    A pályázatra **NEM** jelentkezhetnek adatelemzői és/vagy adatvizualizációs tevékenységet **teljes idejű munkakörben** folytató fiatalok. Ezt az esetleges díjátvételkor igazolni kell.
    A pályamunkákat szakmai zsűri bírálja el. Ennek összetételét a **székelydata** blogon nyilvánosságra hozzuk.
    A pályamunkákat két kategóriában pontozzuk: adatanalízis minősége (**content**) és vizualizáció szépsége (**beauty**). A Kantar Information is Beautiful Awards szolgál útmutatóul minőségben.
    Nincsenek megkötések a beadott pályamunkát illetően: lehet statikus vagy interaktív adatvizualizáció, infografika, videó.
    Egy pályázó több pályamunkát is benyújthat.
    Pályázó lehet egy **személy** vagy több tagból álló **csapat**, de a díjak összege nem személyre, hanem pályamunkára vonatkozik.
    A pályázatra nyelv/állampolgárság, illetve bármilyennemű hovatartozástól függetlenül bárki jelentkezhet. Ellenben a benyújtott pályamunka nyelve **magyar** vagy **angol** lehet. A nyelvnek nincs jelentősége az elbírálás során.
    Abban az esetben ha a zsűri úgy ítéli meg, hogy egyetlen pályamunka sem éri el a minimális szakmai szintet, fenntartjuk a díj kiosztásának eltörlését bármely kategóriában.
    **A verseny két fordulóban zajlik**.

    Az **első fordulóban** a **jelentkezési űrlapot** kitöltve kell a pályamunkát benyújtani.
    A benyújtott pályamunkák közül a zsűri néhányat kiválaszt a **második fordulóra**. Itt egy **élő bemutató**ban kell majd a pályamunkát megvédeni .
    A második forduló helyszíne a **II. erdélyi adatvizualizációs mini-konferencia, Kolozsvár, 2020 január 11**.
    Ha egy második fordulóra kiválasztott pályázónak nem nyílik lehetősége a bemutatónapon való élő részvételre, **virtuális** megoldást biztosítunk.


    Bármilyen felmerülő kérdést a székelydata blogon kell feltenni a pályázatot meghirdető **bejegyzés** alatt, **komment** formában. Személyes kérdéseket a mail@csaladen.es email címre lehet küldeni, ellenben a komment a preferált mód.




**📊** Adatok

1. Közös adatsor kategória

A 2019-es év globálisan legmeghatározóbb témája a **klímaváltozás**. Nem titkolt inspiráció **Ed Hawkins #ShowYourStripes** vizualizációja, ami egy egész mozgalmat indított el világszerte a vizualizáció - ergo adatalapú diskurzus terén a klímaváltozás témában. Ezért a **II. székelydata adatvizualizációs verseny** közös adatsora **Románia és Magyarország időjárás-állomásai** által rögzített hosszútávú, nagyfelbontású klímaadatai.



Az **adatsor** a https://szekelydata.csaladen.es/verseny/2019/data címen érhető el. Akárcsak a tavalyi versenynél, idén is hamarosan részletes leírást közlünk az adatokról (**UPDATE**: itt).

A **székelydata** számára fontos szempont, hogy minden elemzés és munka amit végzünk, az ingyenesen és nyilvánosan elérhető legyen. A nagyfelbontású, hosszútávú időjárás-adatok általában mindig fizetősek. Kivételt képeznek a **NOAA** (Amerikai Éghajlat- és Óceántanulmányozási Ügynökség) **adatbázisában** világszerte regisztrált időjárás-állomások adatai. Ezért ezt az adatbázist (**NCDC**/**NCEI**) használtuk fel a verseny közös adatsorának elkészítéséhez. Az adatokat a következő lekérdezéssel nyertük: *Country → Romania/Hungary → Surface Data (Hourly Global) → SIMPLIFIED → I AGREE → Country: Romania/Hungary → Selected ROMANIA/HUNGARY stations → Mindent kiválaszt → 1931/01/01 - 2019/10/01 (Select Only Obs. on the Hour nincs kiválasztva!) → Inventory Review kipipálva, captcha, email cím → Submit Request*

Az adatokat több fájlban tároltuk, **ebben** a mappában, Romániára és Magyarországra lebontva. Ezek a mappák *zip*-pel összecsomagolt *txt* szövegfájlokat tartalmaznak. Mindegyik *zip* fájlban 3 *txt* fájl található:


    egy *dat* végződésű, ezek az adatsorok
    egy *stn* és egy *stn+* végződésű (tartalomra azonos), ezek a meta-adatok


Minden adatsor egy azonosító (*USAF* oszlop) alapján, időjárás-állomások szerint rendezett idősor (time series). A *stn* fájlok az azonosító szerint tartalmazzák az időjárás-állomások nevét, koordinátáit és földrajzi magasságát. Az adatsorok többi oszlopainak leírását *3505doc.txt* fájlban találhatod (angolul - ha segítséged van fordításra, kérlek kommentben jelezd).

A közös adatsor kategória témája a **klímaváltozás**, ellenben az adatok felhasználása ebben a témakörben **nem szűkített** az itt megadott adatokra! Felhasználhatsz például más országokat is a fenti adatbázisból (persze itt neked kell az új adatbázis-lekérdezést végrehajtani), vagy akár a romániai (**Nemzeti Statisztikai Hivatal**, **Országos Meteorológiai Hatóság**) vagy magyarországi (**Központi Statisztikai Hivatal**, **Országos Meteorológiai Szolgálat**) forrásokat. Budapesti viszonylatban az ÁTLÓ adatvizualizációs műhely egy szuper anyagot készített már erről, de Maarten Lambrechts időjárás-vizualizációját is megemlíteném inspirációnak. Egyetlen **kikötés**, hogy ha további adatokat használsz a pályamunkád elkészítéséhez, akkor ezek **nyilvánosan és ingyenesen elérhetőek kell legyenek**.

2. Nyílt adatsor kategória

Az idei verseny újítása, hogy elindítunk egy **nyílt adatsor kategóriát** is. Ide **olyan cégek és magánszemélyek jelentkezését várjuk, akik úgy gondolják, hogy potenciálisan aranyat érő adatokon ülnek**, de eddig még nem volt idejük/lehetőségük vizuálisan feldolgozni őket. Így most a **II. székelydata adatvizualizációs verseny** nyílt adatsor kategóriájába jelentkezhetnek adataikkal, adatsoronként egy **különdíj **díj felajánlása fejében. Ennek a mértéke természetesen a felajánlótól függ, de minimum **200 € **a javasolt érték. Ez a kategória ugyanúgy kétfordulós, az elbírálási kritériumok azonosak a főkategóriáéval, ellenben itt adatsoronként **egy** díj kerül kiosztásra - illetve a felajánló eldöntheti, ha több díjat is ki szeretne osztani.

**📝 Nyílt adasor ****űrlap**

📤 Benyújtási határidő: **2019.11.30**

Az adatsorok egyetlen kritériuma, hogy **legalább 1000 adatpont**ot tartalmazzanak és **legalább 4 dimenzióban** változzanak. Egy ilyen példa: egy cég munkapontjainak napi árbevétele. Minden munkapont tartalmaz egy azonosítót, helyszínt, illetve a különböző kereskedelmi tevékenységeket leíró címkéket és értékeket, napi időbélyeggel ellátva.

A díjak semmilyen jogi kötelezettséget nem vonnak maga után egyik fél részéről sem. Nyílt adatsorok javaslatára **egyének** és **cégek jelentkezését** **ennek az űrlapnak** a kitöltésével várjuk **2019.11.30**-ig. Bármilyen kérdést a mail@csaladen.es címen tehetnek fel.



📆 Fontos dátumok


    **ELSŐ FORDULÓ** benyújtási határidő: **2019.12.31**
    **NYÍLT ADATSOR **benyújtási határidő: **2019.11.30**
    **MÁSODIK FORDULÓ** élő bemutatók: **2020.01.11**


**EREDMÉNYHIRDETÉS**: **2020.01.11**

🏅 Díjak

**Fődíj: 500 €**
**Legjobb adatelemzés: 200 €
****Legszebb adatvizualizáció: 200 €
**

**Nyílt adatsor kategória: 200 € adatsoronként**

A díjak Csala Dénes és számos magánszemély, illetve cég adományai.

A díjak jogilag személyes, baráti ajándék formáját öltik.
A díjak semmilyen jogi kötelezettséget nem vonnak maga után egyik fél részéről sem. Esetleges **további díjak**, felajánlások, adományok javaslatára **egyének** és **cégek jelentkezését** várjuk a mail@csaladen.es címen.



🧮 Pályamunka

A pályamunkák a **székelydata** blogbejegyzéseinek szokásos formátumát követik: egy fő vizualizáció, esetleg több egyszerűbb infografika által kísérve, az adatfeldolgozáshoz és a vizualizációk elkészítéséhez használt kódrészletek, illetve egy rövid történetmesélés.

Így a pályázathoz is 3 benyújtási mező tartozik: **VIZ**, **KÓD** és **LEÍRÁS**. A pályamunka típusától függetlenül ajánlott a GitHub használata. Itt egy repository-ban csoportosíthatsz mindent. A **székelydata** blog GitHub csatornája útmutatóul szolgálhat e téren.

A **VIZ** mezőbe kérlek illeszd be a pályamunkád vizualizációs részéhez mutató hyperlinket. Ha nem sikerül a GitHub beállítása/használata, akkor a következő alternatívákat használd:


    Statikus vizualizáció/infografika esetén: Dropbox, Onedrive, GDrive vagy IMGUR
    Videó esetén: YouTube vagy Videa
    HTML vizualizáció esetén: GitHub, Heroku
    Tableau/PowerBI/Excel más eszközök esetén a beépített online megosztási linket használd


A **KÓD** mezőbe kérlek illeszd be az adatfeldolgozásra és a vizualizáció megvalósítására használt kód elérésez mutató hyperlinket. GitHub, JSBin, JSFiddle vagy más hasonló szolgáltatások használata ajánlott.

A **LEÍRÁS** mezőbe kérlek írd be a következőket, összesen maximum 300 szóban:


    Honnan jött az ötlet?
    Hogyan végezted az adatfeldolgozást?
    Miről szól a vizualizáció?
    Miért érdekes?
    Szeretnél-e ilyesmivel foglalkozni ezután is?




**📝 JELENTKEZÉSI ŰRLAP**



**🚀 SOK SIKERT!**