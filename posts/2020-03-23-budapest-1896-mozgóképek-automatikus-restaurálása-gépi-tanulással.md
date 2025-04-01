---
title: Budapest 1896 📽 Mozgóképek automatikus restaurálása gépi tanulással
date: 2020-03-23 00:00:21
---


Mostanában egyre több videó lát napvilágot, amelyeken egy nagyon régi - rendszerint, több, mint száz éves - mozgóképet láthatunk, 4K-s felbontásban, (majdnem) mai standardoknak megfelelően megszépítve. Kontextuális szempontból ez egy rendkívül érdekes eljárás, hiszen az elmúlt évszázad tudását felhasználva próbálunk jobb képeket alkotni a még távolabbi múltunkról - de ugyanakkor egy fölöttébb érdekes **gépi tanulási** probléma. 


Here is the English version of this post


Dióhéjban az eljárás a következő: megmutatsz egy algoritmusnak sok-sok képet arról, hogy hogy néz ki ma a világunk, megmutatsz néhány (amennyit össze tudsz gyűjteni) képet arról, hogy nézett ki a világunk régen és az algoritmus megpróbálja rekreálni a modern képek *érzését* a régi képeken (és a videó meg csak képek láncolata).




Talán a legkiemelkedőbb alakja ennek a területnek Denis Shiryaev, ő készítette az Arrival of a Train at La Ciotat restaurálását, **1896**-ból (egyike az első mozgó képeknek) és A Trip Through New York City-t, **1911**-ből. Denis leírja az eljárásait, de csak ötlet szintjén, és mindenki, aki egy picit jártas a témában, sejti, hogy több lépésből áll a teljes eljárás. De sebaj, elkezdtem keresgélni régi **Budapest **felvételek iránt és már meg is volt a következő hétvégi projektem... De még mielőtt mélyebben elmerülünk a részletekben, emelem 👒-om Denis előtt: mert végül ez naaagyon hosszú és nehéz folyamat volt.





📽 Forrásvideók





Hamar rádöbbentem, hogy a projekt talán legnagyobb kihívása a megfelelő jó minőségű forrásvideók felkutatása lesz. Denis restuarálásai gyönyörűek, nem utolsó sorban azért, mert jó minőségű forrásvideókat használ - melyek sokszor már manuálisan restaurálva voltak egyszer. De persze nagyságrendekkel nehezebb Budapestről és a magyar örökségről régi videókat találni, mint mondjuk Párizsról (minél régebbit szerettem volna). Végül megállapodtam néhány (rövid és általában rossz minőségű) **Budapestről** és **Erdélyről** forgatott klipen. Itt talán érdemes megjegyeznem, hogy a filmezés a 20 század előrehaladásával karöltve alakult ki, tehát a késő 19. és korai 20. századi felvételek *nagyságrendekkel* rosszabb minőségűek, mint mondjuk az 1940 utániak.




Miután tudatosítottam a kihívás mértékét és kiválasztottam a legkorábbi videókat, amiket találtam, egy **7-lépéses eljárást** állítottam fel. A teljes eljárást, forráskódókkal együtt ebben a mappában megtalálod (ebben a repóban is tükrözve van, de a videófájlok itt nincsenek duplikálva). Megpróbáltam az egész folyamatot Google Colab munkafüzetekben végezni, amennyire csak lehetett. *Elméletileg*, te is megpróbálhatod reprodukálni a lépéseket és a padláson talált poros filmszalagokat restaurálhatod (digitalizálásuk után) 😎.






**Budapest 1896**-ban, talán **a valaha rögzített első mozgókép Magyarországon**, a Lumière fivérek, a mozgókép feltalálói  az **1896**-os Millenniumi Díszfelvonulásról készítették, csak egy évvel a technológia 1895-ös születése után
**Budapest 1916**-ban, az **első magyar dokumentumfilm**
**Budapest 1925**-ben, (talán) a Magyar Híradó 54. száma
**Budapest 1927**-ben, részlet a holland *Land en volk van Hongarije* filmből
**Budapest a 1930**-as években, a British Pathé felvétele
Talán a **legkorábbi mozgókép Kolozsvárról**, **1930**-ból - amatőr felvétel
**Erdélyi** kivonatok, a *Világhíradó* adásból, **1941-1943 **között
A **Székelyföldet és Erdélyt** átszelő vasútvonal építéséről szóló dokumentumfilm az **1940**-es évekből




🎉 Az eredmény


https://youtu.be/DqnK8OshG6E




https://www.youtube.com/watch?v=DXpM0TGIBJU





🎠 A folyamat





A teljes folyamat neve öregetlenítés (**deoldifying) **és több lépésből tevődik össze. Ezek nem föltétlenül az előírt lépések, vagy a sorrendjük, egyszerűen én így jutottam el a folyamat végére - valószínűleg jócskán lehet a végső minőségen javítani még több kísérletezgetéssel. Ami viszont fontos, hogy ez egy **automatikus folyamat**, a **mesterséges intelligencia** és a **gépi tanulási eljárások** előrehaladása teszi ezt lehetővé, **csak 2019-2020 óta** (egyes algoritmusok olyan "forrók", hogy még nem is voltak tudományos cikkben vagy konferencián bemutatva). Persze ez a folyamat valószínűleg *sokkal* egyszerűbb és gyorsabb lesz majd néhány év múlva, de most itt tartunk. Nekem személyesen, *gőzöm sincs* hogyan kell régi felvételeket restaurálni, csak szeretek kóddal játszadozni 🤓. 





0. Előkészületek





Lemásolhatod a teljes mappámat, de ha frissen szeretnéd kezdeni, akkor hozz létre egy dolgozó mappát, és ebben egy raw nevű almappát. A legjobb eredményekért használj mp4 formátumot a forrásvideóknál.




Ugyanakkor az egész folyamatot futtathatod a **felhőben**, talán Google Colab-on vagy hasonlón, mert a legtöbb normális felbontású videónál (>640x480), legalább **16GB **grafikus memória szükséges (GPU RAM), ami több, mint a legtöbb asztali grafikus kártya memóriája. Ja igen, mindenképpen **szükséged lesz egy grafikus processzorra (GPU)**. Ha több graikus kártyád van párhuzamosan kötve, akkor **>40GB GPU RAM**-al kényelmesen elboldogulsz. A **Jupyter munkafüzetek, **amiket a mappámban találsz úgy lettek kialakítva, hogy férjenek bele **Google Colab **GPUk (Nvidia Tesla P100, ha szerencsés vagy) 16GB-os memória-limitjébe - de ez sokszor a méret csökkentésével jár 😐. Mindegyik munkafüzet első cellája megmondja milyen GPU kaptál a Googletől. Az **Nvidia** compute cloud-out is kipróbálhatod.







A munkafüzetekben a **Google Drive**-ot használtam a fájlok tárolására. A második cella mindig a a saját Google Drive-od csatolja a Colab munkafüzethez - a Google's hivatalos folyamatát követve. Egy egyéni kulcsot kell beillessz és ezt a lépést *minden* munkafüzet esetében meg kell ismételned.





1. Stabilizálás





Az első lépés a videók **stabilizálása**. A régi felvételek mindig rázkódnak és ez nem jó minőségű bemenet az algoritmusoknak. A megvalósításhoz Adam Spannbauer **vidstab** algoritmusát használtam. Kövesd a lépéseket a 1_stabilize munkafüzetben. Az végrehajtás után az 1 nevű mappában találod a stabilizált videókat. A vidstab nem végzi a legjobb munkát a különböző színhelyek közötti átmenetek esetében, de most megteszi.





2. Felnagyítás





A második lépés a videó **felnagyítása **(**upscale**). Emlékszel még a 90-es évek akciófilmjeiben hogyan nagyítják a pixeles biztonsági kamerás felvételeket? Na ez gyakorlatilag lehetetlen volt - *egészen mostanig*. Azért mert amikor ráközelítünk valamire, akkor az új, keletkező pixeleket ki kell valamilyen módon színezni. A bevett technika az **interpolálás** lenne - de ez persze egy nagyon elmosódott képet eredményez. De **gépi tanulással** felismerhetjük a képen megjelenő főbb vonásokat, alakokat, épületeket (**features**) - és így hatékonyabban ki tudjuk az új pixeleket tölteni.







Ennek a lépésnek a végrehajtására kép opciónk van:






A 2_upscale munkafüzet segítségével a mappából - ez a **VaporSynth** algoritmust futtatja, az AlphaAtlas-tól, ellenben eléggé nehéz rávenni, hogy elinduljon..
A másik opció a **Topaz **Video Enhance AI, aTopaz Labs-tól. Ez egy önálló program, ami Windows operációs rendszeren fut - a trial verzió elegendő ehhez a projekthez.






Ha elkészültél, akkor a felnagyított videókat helyezd a 2-es mappába. Ha Topaz-t használtál (mint én), megtarthatod az automatikus fájlneveket.





3. Öregetlenítés





A következő lépés a monokróm videók mesterséges **kiszínezése** és a maszatok, foltok **kijavítása** - amennyire csak lehetséges. Ehhez Jason Antic **DeOldify **algoritmusát használjuk - és innen választottam a nevét a teljes eljárásnak: **öregetlenítés** (**deoldify**). Ahhoz, hogy ezt a lépést le tudd futtatni, fel kell töltsd a feldolgozandó videókat a YouTube-ra és el kell mentened a videó-linkeket. Ezután a 3_deoldify munkafüzet segítségével hajthatod végre a öregetlenítést. Az én tapasztalatom szerint a render_factor legjobb értéke 10-15 között van. ha elkészültél, a munkafüzet feltölti az öregetlenített, kiszínezett videókat a 3-as mappába.





4. Előkészítés





A következő lépés az **újrahívás (remastering) **- hasonló ahhoz a folyamathoz, amit a régi filmszalagok **manuális restaurálásánál** követnél. De ebben az esetben természetesen mindent automatikusan végzünk, gépi tanulás segítségével. Az újrahívás eltűnteti a maszatokat, porfoltokat és kiégéseket a régi felvételről.







Ehhez Satoshi Iizuka **DeepRemaster** algoritmusát használjuk. De mivel ez egy **átviteli tanulásos** (**transfer learning**) algoritmus, először kell mutassunk neki néhány **jó példát** arról, hogy az újrahívott videó hogyan kellene kinézzen. Ezek egy mappában tárolt (ideális esetben kiszínezett) képek a videó egyes jeleneteiről, ahol nincs túl sok hiba a felvételen. Ezeket természetesen manuálisan is elkészítheted - és a legjobb eredmények érdekében ez az ajánlott módszer - de most ezt a lépést is automatizáljuk:






Az első lépés ebben a folyamatban a **jelenetfelismerés** (**scene detection)**. Ehhez Brandon Castellano **pyscenedetect** algoritmusát alkalmazzuk. Ez az algoritmus a videóban jelenetváltozásokat detektál és felszabdalja azt a különböző **jelenetekre**. Ezután minden jelenetről készít néhány reprezentatív lenyomatot. Hajtsd végre a jelenetfelismerést mind az öregetlenítés *előtt *és *után* is - tehát a 2-es és 3-az mappa összes fájlaira. A jeleneteket az algoritmus mindkét mappában egy scenes nevű almappába menti. Amikor a jelenetfelismerés véget ért, fésüld át a scenes mappát, és válassz ki néhány **jól kinéző, reprezentatív jelenetet**, ahol **tiszta a kép **és másold át ezeket a goodscenes almappába, mind a 2-es és 3-as mappa esetében. Ehhez az 4a_scene_detection munkafüzetet használhatod.
Ezután, mivel az újrahíváshoz **színes jelenetképek** szükségesek, ki kell színeznünk őket. Ezt újra megtehetnénk manuálisan, de most automatizáljuk az eljárást. Előszöris, ha helyesen végezted az öregetlenítést, akkor a 3-as mappában már kellene legyen egy sor színes jelenet. De most hozzunk létre egy második szett kiszínezett jelenetet is, egy másik színező algoritmus segítségével. Ehhez Richard Zhang **ideepcolor**eljárását (vagy ezt az alternatívát) használjuk. És mivel ez is egy *átviteli tanulásos* algoritmus, kell választanunk egy **színpéldát** minden videóhoz. Ehhez egy mostanában készült fotóra van szükségünk, amelyen valami olyasmi van, mint ahogyan a videó legreprezentatívabb részében szeretnénk, hogy a színek kinézzenek. Ennek a példának a **szín-összetételét **(color composition, histogram) fogja az algoritmus rávinni a színezetlen jelenetekre. Miután minden videóhoz kiválasztottad a színpéldát, töltsd fel a 2/goodscenes mappába, és nevezd el ugyanúgy, mint a videó, csak .png kiterjesztéssel. Tehát ha az eredeti klip címe bp1.mp4 (meg talán néhány felnagyított változata), akkor nevezd a színpéldát bp1.png-nek. Futtasd le a 4b_ideepcolor munkafüzetet. Ez létrehozza a 4-es mappát és két almappát:

colorzed_auto - ide rakjuk majd a vakon, **automatikusan színezett **képeket
colorized_ref - ide pedig az **átviteli tanulással**, a színpélda felhasználásával színezetteket


Végül pedig össze kell hozzuk az összes színezett jelenetet videónként egyetlen közös mappába, ehhez futtasd le a 4c_prepare munkafüzetet.




5. Újrahívás





Most minden készen áll az **újrahíváshoz**. Ne feledd, Satoshi Iizuka **DeepRemaster** algoritmusát használjuk. Mivel ez egy *átviteli tanulásos* algoritmus (transfer learning), meg kell adnunk egy mappát, ahol hibátlan, kiszínezett jeleneteket mutatunk, mint példa az algoritmusnak** **- ezt hoztuk létre a fenti folyamattal. Futtasd le az 5_remaster munkafüzetet, hogy végrehajtsd az újrahívást. A folyamat végén az5, 5b, 5c mappák jönnek létre - azért, mert a videó **több verzióján** végrehatjuk az újrahívást: színezetlen és  öregetlenítéssel színezett verziókon *egyaránt*. Itt fontos megjegyezni, hogy lehetséges, hogy a videók felbontását **csökkenteni** kell, mert ez egy nagyon memóriaéhes lépés. Az én tapasztalatom szerint, az öregetlenített videók jobban szolgálnak forrásvideóként (tehát a 3-as mappa), talán egy 12-es  render_factor-ral.





6. Élesítés





A következő lépés a videó **élesítése** (**deblur** és nem *sharpen*!). Ez nagyon hasonló a felnagyításhoz, és ugyanúgy mély neuronhálókat használunk a kép karakterisztikus elemeinek a felismerésére és újrarajzolására, élesítésére. Erre jelenleg a legjobban működő eljárás Minyuan Ye **SIUN **algoritmusa, amit a 6_deblur munkafüzetben futtathatsz. A folyamat végén egy szimmetrikus struktúrát kapunk: az 5, 5b, 5c bemeneti mappák eredményei a6, 6b, 6cmappákban lesznek elmentve.





7. Interpolálás





Végül pedig, mivel a régi felvételek általában alacsonyabb képkocka-sebességen (framerate, frames per second, **fps**) futnak, mint a mai videók (és persze ez sokszor nem egyenletes, és az operatőr kézügyességétől függött 😀), szükséges a képkockák közötti **interpolálás**, a **képkocka-sebesség  növelésének** érdekében. Ez egy nagyon gyorsan változó terület, de jelenleg erre a feladatra a legjobb eszköz messze Bao Wendo **DAIN** algoritmusa - ez egy három dimenziós modellt épít az egyes jelenetek köré és így a **mélység-információ** kiszámításával szuper minőségű interpolálást végez. Ellenben nekem sajnos nem sikerült a saját videóimon alkalmaznom ezt az algoritmust (bár a példavideókon tökéletesen működik - UPDATE: úgy néz ki, hogy van egy verzió Windows-ra), ezért muszáj volt egy alternatívát keressek. Végül Shurui Gui és Chaoyue Wang **FeatureFlow**algoritmusát használtam, amit a 7_interpolate munkafüzetben találsz. Akárcsak az előző lépésnél, itt is egy szimmetrikus mappa-struktúra az eredmény: 7, 7b, 7c. Akárcsak az újrahívásnál, néha itt is szükséges csökkenteni a felbontást a feldolgozás előtt - ezek a fájlok kerülnek az alapértelmezett nevek alá a 7, 7b, 7c mappákba, míg a feldolgozott videók a _Sedraw végződést kapják. Az eljárás végén a vegső videókat az 8, 8b, 8c mappákba mozgatjuk. Ha nincs felbontás-csökkentésre szükség, akkor a 7, 7b, 7c mappák üresen maradnak (valószínűleg csak a 7b mappában találsz fájlokat, mivel a többi videót már az újrafeldolgozás lépésnél lekicsinyítettük).





🏁 Befejezés





Befejezésképpen, mielőtt feltöltenéd a munkádat a YouTube-ra, használhatsz egy **videószerkesztő** szoftvert, hogy megmutasd a különbségeket - én a nyílt forráskódú **OpenShot**-ot használtam. És ha gondolod, hogy segít, talán újra lefuttathatod a **Topaz**-t, hogy tovább nagyítsd a videódat, de túldolgozottnak tűnhet majd.



raw - eredeti forrásvideók
1 - stabilizált
2 - felnagyított
3 - színezett deoldify-al
4 - jelenetekre bontva 2 és 3
Innen a fájlok száma sokszorozódik:

file1 - stabilizált, felnagyított
file1_12 - stabilizált, színezett deoldify-al, render_factor=12
file1_21 - stabilizált, színezett deoldify-al, render_factor=21


5 - újrahívott, csökkentett felbontású (hogy beleférjen a memóriába), újraszínezett ideepcolor-al
5b - újrahívott, eredeti méret
5c - újrahívott, csökkentett felbontású
Innen 5 → 6, 5b → 6b, ... szabály érvényes
6, 6b, 6c - élesített
7, 7b, 7c - tovább csökkentett, ha szükséges az interpoláláshoz
7req - az interpoláláshoz szükséges modellfájlok
8, 8b, 8c - interpolált, befejezett








És ennyi! Megtanultad hogyan tudsz **automatikusan régi videókat restaurálni**, **mesterséges intelligencia** segítségével, 7 mély neuronhálós **gépi tanulási** algoritmust alkalmazva. Jelezd **kommentben** ha sikeresen alkalmaztad **saját videón**, vagy ha van egy szuper** javaslatod forrásvideóra**!