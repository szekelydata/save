---
title: A nagy népi időjóslás-teszt 🌞🌤️🌧️❄️
date: 2019-11-26 23:30:48
---


**Sándor, József, Benedek, zsákban hoznak meleget** - szól a mondás. De vajon tényleg hoznak? **Igen, 65%-ban**. Ebben a bejegyezésben több, mint hatvan évre visszamenő időjárás-adatsorral vizsgáljuk meg a népi időjóslatokat. A **II. székelydata adavizualizációs verseny** nagyfelbontású időjárás-adatsorát felhasználva, **50 mondást** fordítottunk le az adatok nyelvére és vizsgáltuk meg az érvényességüket. 



Minden **jövendölés két részből áll**: egy **feltétel**: "*Ha Katalinkor kopog*" - azaz ha november 25-én az átlagosnál hidegebb az idő, és egy jóslat: "*Karácsonykor locsog*" - azaz a december 24-27-i periódusban az átlagosnál melegebb idő várható.

Persze sok mindent meg lehetne vizsgálni az adatok longitudinális (időbeli) változását illetően - például, hogy a mekkora szerepet játszik a klímaváltozás - de összességében azt mondhatjuk el, hogy a magyar népi időjóslatok sajnos csak **egy kicsit jobbak a pénzfeldobásnál**: az átlagos találati arány **56%**. Természetesen a hagyományos tavasz-vagy őszkezdő napok jóslatai jönnek be a legnagyobb arányban, de a **januári fagyjövendölések** is **70%** fölött teljesítenek. Az **ismertebb mondások az átlag fölött teljesítenek**: **Sándor, József, Bendek 65%**-ot kap, **Medárd 66%**-ot, **László 79%**-ot, **Szent Anna 75%**-ot, **Péter 68%**-ot, **Márton 62%**-ot, **Katalin 67%**-ot.

És akkor íme, a részletes eredmények. Mindenik időjóslat érvényességét **két** függőleges **tengely** segítségével mutatjuk be, ahol a **feltétel** és a **jóslat** teljesülését mutatjuk, évente:





                                               



**ADATOK + KÓD: **A **mondásokat** **erről** , **erről** és **erről** a weboldalról gyűjtöttük össze. Mivel ezek magyar nyelvterületről származó mondások, az adatokat **10 erdélyi** és **18 magyarországi** településen elhelyezett időjárás-allomás adataiból raktuk össze. Ezeket most összesítve mutatjuk be, de itt elérhetőek országonként is. Minden év egy adatpontot jelent, településenként. Az idősorok a 50/70-es években kezdődnek és 2019-ig tartanak. Ez alapján **egy népi időjóslat érvényességének megállapítására** **általában** ≈60 év x ≈28 település → **≈1680 adatpont** áll rendelkezésre.

[caption id="attachment_1906" align="aligncenter" width="923"] Felhasznált időjárás-állomások és a kezdeti éveik[/caption]

A klíma-adatok forrása a **II. székelydata adatvizualizációs verseny** adatai. A nagyfelbontású, hosszútávú időjárás-adatok általában mindig fizetősek. Kivételt képeznek a **NOAA** (Amerikai Éghajlat- és Óceántanulmányozási Ügynökség) **adatbázisában** világszerte regisztrált időjárás-állomások adatai. Ez általában több évre visszamenőleg, óra felbontásban jelenti a hőmérséklet, látótávolság, szélsebesség, csapadék mennyisége (az elmúlt egy órában/napban), jégeső, hó észlelése, hóréteg vastagsága értékeket. Ezeknek a mennyiségeknek a megjelenítésére az infografikákon a következő ikonokat használtuk (a használt betűvel kicsit másképp néznek ki):


    Hőmérséklet: ♨️ hidegebb:✨️ melegebb: ☼
    Szél: ⛵️ gyengébb: ☘ erősebb: 🌀
    Eső: ☂️ kevés: 🌂 sok: ☔️
    Látótávolság: ⛅️ borús: ⛈️ tiszta: ☀️
    Hó: ❄️ kis mennyiség: ⚪️ nagy mennyiség: ☃️
    Hóvastagság: ⛷️ sekély: ⚪️ mély: ⛄️
    Jég: ✴️ kisszemű: ⚪️ nagyszemű: ⭕️


Ezzel és ezzel a Jupyter notebook-kal gyűjtöttük be a klíma-adatokat, és ezzel dolgoztuk fel őket. Csak azokat az **időjárás-állomásokat** és **éveket** tartottuk meg **Románia** és **Magyarország** adataiból, amelyeknél naponta legalább 4 érték, havonta legalább 6 nap és évente legalább 3 hónap rendelkezésre állt. Ezután az állomásokat szűrtük, hogy földrajzilag egyenletes eloszlást és egy reprezentatív  képet kapjunk. Az infografikákat matplotlib-el készítettük, a hegedűplotok kivételével. Ezek seaborn-al készültek. Az plottolás teljes forráskódját **itt** találod.

És végül pedig: ❤️ Köszönöm, hogy elolvastad ezt a vaskos bejegyzést! Még több adatvarázslatért **olvasd** el a **sztorit**, és ha megteheted **támogasd** a **székelydatát** a láblécen megjelölt opciók egyikén: **Patreon**-on, **Paypal**-on, vagy küldhetsz **kriptót** is!



Itt a mondások teljes listája, a vizsgálható hipotézisre való fordításokkal (természetesen nem lehet mindent tökéletesen lefordítani, így a legtalálóbb közelítéseket használtuk):




**Dátum**
**Mondás**
**Jelentés**


**jan. 6**
*A vízkereszti hó tartós hó.*
Ha ezen a dátumon havazik, akkor a következő hónapban az átlagosnál hidegebb idő várható.


**jan. 18**
*Ha Piroska napján fagy, az negyven napig el nem hagy.*
Ha ezen a dátumon fagy, akkor a következő 40 napban fagypont alatti idő várható.


**feb. 2**
*Ha a medve ma meglátja a saját árnyékát, hosszú tél lesz!*
Ha ezen a dátumon derűs, a következő két hónapban az átlagosnál hidegebb idő várható.


**feb. 3**
*A Balázs napi esõ jégverést hoz.*
Ha ezen a dátumon esik, jégeső várható a nyár elején.


**feb. 6**
*Dorottya szorítja, Julika tágítja!*
Ha ezen a dátumon fagy, akkor a következő 10 napban fagypont alatti idő várható.


**feb. 19**
*Ha Zsuzsanna napján a pacsirták szólnak, vége lesz a hónak.*
Ha ezen a dátumon derűs, a következő hónapban az átlagosnál melegebb idő várható.


**feb. 24**
*Mátyás ront, ha talál, (ha nem talál, csinál)!*
Ha ezen a dátumon fagy, akkor a következő 10 napban az átlagosnál melegebb idő várható.


**feb. 24**
*Mátyás (ront, ha talál), ha nem talál, csinál!*
Ha ezen a dátumon nem fagy, akkor a következő 10 napban az átlagosnál hidegebb idő várható.


**márc. 10**
*Ha Ildikó napján fagy, negyven napig lehet fagy.*
Ha ezen a dátumon fagy, akkor a következő 40 napban az átlagosnál hidegebb idő várható.


**márc. 12**
*Ha Gergely napján esik, még áprilisban is havazik. *
Ha ezen a dátumon esik, a következő hónapban az átlagosnál hidegebb idő várható.


**márc. 12**
*Gergely napi szél Szent György napig él. *
Ha ezen a dátumon szeles, a következő 43 napban az átlagosnál szelesebb idő várható.


**márc. 18**
*Sándor, József, Benedek zsákban hoznak meleget. *
Ha ezeken a dátumokon az átlagosnál melegebb az idő, az a következő hónapban is kitart.


**márc. 24**
*Szent György napja õsi tavaszkezdõ nap. *
Ezt a dátumot követő két hétben átlagosan melegebb az idő, mint az azt megelőzőben.


**márc. 25**
*Gyümölcsoltó Boldogasszony negyven napig tart.*
Amilyen ezen a dátumon az idő, olyan lesz a következő 40 napban.


**ápr. 1**
*A Szent György havi esõ kergeti a fagyot (és esõs májust jósol)! *
Ha április első felében az átlagosnál több eső esik, a következő hónapban az átlagosnál melegebb idő várható.


**ápr. 1**
*A Szent György havi esõ (kergeti a fagyot) és esõs májust jósol! *
Ha április első felében az átlagosnál több eső esik, májusban az átlagosnál esősebb idő várható.


**jún. 8**
*Ha Medárd napján esik, negyven napig esik. *
Ha ezen a dátumon esik, a következő 40 napban az átlagosnál esősebb  idő várható.


**jún. 10**
*Margit napja esõs nap. *
Ezen a dátumon átlagosan többet esik, mint az ezt megelőző és követő két hétben.


**jún. 24**
*Szent-Iván éjjele negyven napig tart.*
Amilyen ezen a dátumon az idő, olyan lesz a következő 40 napban.


**jún. 27**
*Jól figyeld meg László napját, Jó előre megjósolja az idő járását.*
Amilyen ezen a dátumon az idő, olyan lesz a következő hónapban.


**jún. 29**
*Péter-Pál napja hagyományos búzaarató nap.   *
Ezt a dátumot követő két hétben átlagosan kevesebbet esik, mint az ezt megelőző két hétben.


**júl. 25**
*Ha Jakab napján sok a felhő, sok lesz a hó.*
Ha ezen a dátumon felhős, az átlagosnál havasabb tél várható.


**júl. 25**
*Ha Jakab napján nagyon süt a nap, nagy tél várható.*
Ha ezen a dátumon derűs, az átlagosnál hidegebb tél várható.


**júl. 25**
*Ha Jakab napján esik, akkor enyhébb lesz a tél.*
Ha ezen a dátumon esik, az átlagosnál enyhébb tél várható.


**júl. 26**
*Ha Szent Anna napján esõ esik, hat hétig esni fog.  *
Ha ezen a dátumon esik, a következő 42 napban az átlagosnál esősebb  idő várható.


**júl. 31**
*Ha Ernő napján esik, akkor enyhe tél következik.*
Ha ezen a dátumon esik, az átlagosnál melegebb tél várható.


**aug. 1**
*Ha Pétertől Lőrincig nagy a hőség, soká fehér lesz a tél.*
Ha ezeken a dátumokon az átlagosnál melegebb az idő, az átlagosnál hidegebb tél várható.


**aug. 4**
*Ha Domonkos napján nagy a meleg, akkor télen nagyon hideg lesz.*
Ha ezen a dátumon az átlagosnál melegebb az idő, az átlagosnál hidegebb tél várható.


**aug. 4**
*Ha Domonkos napján hideg van, akkor enyhe télre számíthatunk.*
Ha ezen a dátumon az átlagosnál hidegebb az idő, az átlagosnál melegebb tél várható.


**aug. 20**
*Ha Szent István napja esõs, száraz lesz az õsz. *
Ha ezen a dátumon esik, az átlagosnál szárazabb ősz várható.


**aug. 24**
*Amilyen Szent Bertalan, olyan az õsz.   *
Amilyen ezen a dátumon az idő, olyan lesz az ősz.


**szept. 1**
*Ha Egyed napján esik, esõs lesz az õsz. *
Ha ezen a dátumon esik, az átlagosnál esősebb ősz várható.


**szept. 1**
*Ha Viktor napján szép idõ van, hosszú lesz az õsz. *
Ha ezen a dátumon derűs, az átlagosnál melegebb ősz-vég és tél-elő várható.


**szept. 1**
*Szeptemberi meleg éjszakák finom bort érlelnek.*
Ha ezen a dátumon az átlagosnál melegebb az idő, az átlagosnál melegebb ősz várható.


**szept. 8**
*Ha hidegre fordulnak Máriák, a borok savanyúak lesznek.*
Ha ezen a dátumon az átlagosnál hidegebb az idő, az átlagosnál hidegebb ősz várható.


**szept. 12**
*Ha Mária napján szép idõ van, szép lesz az õsz.    *
Ha ezen a dátumon derűs, az átlagosnál melegebb ősz várható.


**szept. 14**
*Ha Lambert napján szép az idő, szép lesz majd a tavasz is.*
Ha ezen a dátumon derűs, az átlagosnál melegebb tavasz várható.


**szept. 18**
*Negyven napig olyan időt várj, mint Péterkor.*
Amilyen ezen a dátumon az idő, olyan lesz a következő 40 napban.


**szept. 28**
*Eljött immár Simon, Júdás, jaj neked, te põregatyás. *
Ezt a dátumot követő két hétben átlagosan hidegebb az idő, mint az azt megelőzőben.


**szept. 29**
*Ha dörög az ég, szép leend az ősz, (de nagy tél következik).*
Ha ezen a dátumon esik, az átlagosnál melegebb ősz várható.


**szept. 29**
*Ha dörög az ég, (szép leend az ősz), de nagy tél következik.*
Ha ezen a dátumon esik, az átlagosnál hidegebb tél várható.


**szept. 29**
*Szent Mihálykor keleti szél, nagyon kemény telet ígér.*
Ha ezen a dátumon az átlagosnál erősebb a szél, az átlagosnál hidegebb tél várható.


**okt. 21**
*Amilyen Orsolya, olyan a tél.   *
Amilyen ezen a dátumon az idő, olyan lesz a tél.


**okt. 26**
*Dömötör napján ha hideg szél fúj, igen hideg lészen a tél is.*
Ha ezen a dátumon az átlagosnál erősebb a szél, az átlagosnál hidegebb tél várható.


**nov. 1**
*Ha Mindenszentek nedves, akkor lágy tél következik.*
Ha ezen a dátumon az átlagosnál több eső esik, az átlagosnál melegebb tél várható.


**nov. 1**
*Ha Mindenszentek száraz, akkor kemény tél következik.*
Ha ezen a dátumon az átlagosnál kevesebb eső esik, az átlagosnál hidegebb tél várható.


**nov. 11**
*Ha Márton napján a lúd jégen jár, Karácsonykor sárban botorkál.*
Ha ezen a dátumon fagy, Karácsonykor az átlagosnál melegebb idő várható.


**nov. 19**
*Ha Erzsébet megrázza a pöndölyét, lészen hó karácsonykor is.*
Ha ezen a dátumon havazik, Karácsonykor is nagy hó lesz.


**nov. 25**
*Ha Katalinkor kopog, Karácsonykor locsog. *
Ha ezen a dátumon az átlagosnál hidegebb az idő, Karácsonykor az átlagosnál melegebb lesz.


**dec. 25**
* Fekete Karácsony - Fehér Húsvét.*
Ha ezen a dátumon nincs hó, a következő áprilisban lesz.