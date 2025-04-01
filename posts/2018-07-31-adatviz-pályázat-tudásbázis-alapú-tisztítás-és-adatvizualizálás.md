---
title: Adatviz pályázat: Tudásbázis alapú tisztítás és adatvizualizálás
date: 2018-07-31 20:22:02
---


Adatviz pályázat fődíj vendégbejegyzés: Salamon Evelin és Rapa Erik



Adattisztítás

Az adattisztítással foglalkoztunk a legtöbbet a projekt során. Ehhez C#-ban építettünk egy **tool**-t, amit könnyen tudtunk továbbfejleszteni és párhuzamosan is tudtunk vele dolgozni.



https://github.com/RapaErik/SzekelyData/

Első lépésben meg kellett határozni az attribútumok számát és azok nevét. Ezt az akadályt könnyen vettük, mivel Newtonsoft Json-t alkalmaztunk a json beolvasásánál és ez egyből *deszerializálta* nekünk az adatokat. Ezután eltároltuk az összes adatot egy MS-SQL adatbázisba Entity Framework segítségével, ahol Code First technikát alkalmaztunk (azaz létrehoztunk egy osztályt, aminek az attribútumai meg fognak egyezni az adatbázis táblájának oszlopaival). Mikor eltároltuk az adatokat, figyeltünk arra, hogy duplikáljuk a tisztítandó oszlopokat és a felesleges oszlopokat, amiben semmi nincs, ne tároljuk. Másrészt minden ékezetet eltávolítottunk, azaz normalizáltuk az adatokat.



Második részben az *livesin* (jelenlegi lakhely) oszlopot próbáltuk megtisztítani. Itt az adatok fele más nyelven és sokféleképpen van jelen. Nagyon sokat böngésztük az adatokat és egy **érdekes támpontot** találtunk: Az, aki külföldön él és nem világhírű településen, (mint Hollywood) az írja az országot is mellette. Ha belföldön él, akkor vagy csak a település, vagy a település, a megye és Románia. Ha a Románia szóra keresünk rá, megkapjuk azokat az adatokat, ahol a település, a megye és Románia szerepel. Ezek mind vesszővel vannak elválasztva. **Felbontottuk **(splitteltük / tokenizáltuk) az adatot vessző szerint és megtartva az első elemet, megkaptuk a települést. Ezután az adataink ugy néztek ki, hogy ahol többminden volt felsorolva az külföldi és ahol nem volt felsorolás az belföldi. Egyszerűbben, ahol van “,” az külföldi ahol nincs az belföldi.



A belföldi adatok **többnyelvűsége** okozott még problémát. Szerencsére Románia településeinek adatbázisát megtaláltuk az interneten, ahol románul írja az összes települést. Normalizálva ezeket is, már tudtunk keresést írni és ahol egyezés volt, kiírtuk egy CSV file-ba. Ezeket kézzel (azaz nem API segítségével) lefordítottuk magyarra (már aminek volt magyar megfelelője) és vissza írtuk őket az adatbázisba.



A következő lépésben a legidőigényesebb rész következett: a **tudásbázis alapú tisztítás**. Itt a tudásbázis alatt **ontológiát** értünk, egy adott fogalomhoz kapcsolódó szavakat. Ezekből az adatokból így érdemes statisztikát kivonni. A foglalkozás helyet szakmai irányzatott írunk: sebész, ápoló, orvos, medic, stb., ezek az emberek mind az egészségügyben dolgoznak. Ez rengeteg munkát igényelt, mivel itt nem csak az elírásokat kellett kiküszöbölni, hanem kicsit jobban össze kellett vonni az adatokat, viszont működő út volt.



Ezt megcsináltuk iskolákra és egyetemekre is. Arra lettünk figyelmesek, hogy össze tudunk vonni két oszlopot a *school* és az *other1*-et. Három helyen volt csak ütközés, de valójában csak kiegészítő információ volt, nem ütközés.



[caption id="attachment_1265" align="alignnone" width="817"] Salamon Evelin és Rapa Erik - Tudásbázis alapú tisztítás és adatvizualizálás[/caption]

Egyéb próbálkozások tisztításra:

Mikor megláttuk, milyen sok munkát igényel a tudásbázisos tisztítás, kipróbáltunk egyéb módszereket is.



Az első ilyen volt az OpenRefine, ami nagyon ügyes kis software és mindenki figyelmébe csak ajánlani tudjuk. De nem elég gyors: a mi módszerünkkel egy óra alatt meg lehetett csinálni azt, amit ezzel három óra alatt sikerült elérni.



Szavak közötti távolság mérő függvényekkel (Jaro-Winkler, Levenshtein, stb.) kísérleteztünk még, de ezek csak szintaktikailag képesek értelmezni a szavakat. Ha csak elírások lettek volna a mi problémáink, ez egy jó irány lett volna.



Kohonen hálókkal is csak ennyit tudtunk volna elérni, ezeknek is jól utánanéztünk. Bár a Kohonen hálókat klaszterezésre használják, ugyanúgy távolságmérő függvényeken alapul.



Született még egy ötlet, ami tudásbázis alapú szemantikai értelmező lenne, de ezt sajnos még nem próbáltuk ki. Az ötlet a k-means klaszterezőre épül. A centroidok a mi esetünkben nem pontok lennének, hanem halmazok, amikben egy fogalommal kapcsolatos szavak lennének: {sapi, sapientia, emte, erdélyi magyar tudományegyetem}. A következő lépésben az összes centroid összes szavától távolságot mérnénk az összes input szóra  és a centroidok újraszámítása abból állna, hogy ahol a legkisebb a távolság, azt a centroidot bővítenénk. Elméletileg működőképes lenne, gyakorlatilag még nem lett kipróbálva. Ezzel azt érnénk el, hogy a tudásbázisunk magától bővülne.



Statisztikák kinyerése

Ez nem volt egy nagyon bonyolult feladat. Pár lekérdezéssel már készen is voltunk. Ezután az eredményeket átalakítottuk százalékokba és már vizualizáltunk is.



[gallery type="slideshow" ids="1282,1283,1281,1280" orderby="rand"]

Vizualizáció

Számos software-t néztünk meg, ami vizualizációra alkalmas, köztük az Excel-t és a Tableau-t is. Ezek nagyon ügyesen felismerik a településeket, koordináta megadása nélkül is.



Megnéztünk adatvizualizációs templateket is, köztük a D3, D3plus, chartist, amcharts és még sok hasonlót. Ekkor rájöttünk arra, hogy nem tudunk nagyon különlegeset alkotni, csak ha becsempészünk egy kis jópofaságot, amit vagy értékel a zsűri, vagy nem. Ekkor került Pistabá képbe, mert ez egy modern székely ikon és ha már SzékelyData akkor legyen székely ízig-vérig és így a szójárást is örökölte. Ezt a dolgozatot bemutattuk még a Sapientia EMTE marosvásárhelyi karának TDK-ján is, ahol különdíjat kaptunk. Határidő előtti napon lett megalkotva, ezért a weblap kódja szétszórtra sikeredett, de legalább működik. Ha több időt szántunk volna rá kicsit strukturáltabb lett volna a kód és responsive is lett volna a web design.



A végleges termék:  **Tudásbázis alapú tisztítás és adatvizualizálás **

Összegzés

Mi nagyon örültünk ennek a kihívásnak. Egy hónapot dolgoztunk a projekten, ami tele volt tanulsággal és rengeteg tapasztalatot szereztünk vele. Felkeltette az érdeklődésünket az adatbányászat iránt.





**Salamon Evelin** és **Rapa Erik** Tudásbázis alapú tisztítás és adatvizualizálás című munkája **nyerte** az I. SZÉKELYDATA adatvizualizációs pályázat fődíját.