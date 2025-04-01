---
title: Adatviz pályázat: Székely(földi)ek életpályája
date: 2018-08-16 06:20:44
---


Adatviz pályázat vendégbejegyzés: Lőrincz Szabolcs



Székely(földi)ek életpályája
Ahogyan a cím is mutatja, a projektem célja felkutatni az összefüggéseket a székely(földi)ek születési helyei, lakhelyei, tanulmányi területei, és szakmái között. Elsősorban azért foglalkoztatott ez a téma, mert kíváncsi voltam, hogy milyen módon és mértékben befolyásolja a székely(földi) emberek életét, illetve döntéseit a származási helyük, lakhelyük. Olyan fontos kérdésekre tudunk válaszolni továbbá, mint például mennyire tudnak az emberek a saját szakterületükön belül elhelyezkedni, milyen tanulmányi területek, illetve szakterületek népszerűek a székely(földi)ek körében, valamint az egyes településeken.


A továbbiakban szeretnék beszámolni az általam használt adatfeldolgozási-, illetve vizualizálási módszerekről, eszközökről, majd röviden bemutatom az eredményeimet.



Adattisztítás
Az első lépés azon emberek adatainak kiválasztása, akik publikussá tették a lakhelyüket, tanulmányi területeiket és szakmáikat a Facebook profiljukon. (A születési hely minden, az adathalmazban szereplő egyén esetén meg volt adva, hiszen eredetileg az alapján voltak gyűjtve az adatok.)


Második lépésként sorban feldolgoztam a megadott születési helyeket, lakhelyeket, szakmákat. Előbb eltávolítottam az ékezeteket, majd csoportosítottam őket. A csoportosítás volt az egyik legidőigényesebb feladat, hiszen az adathalmaz többnyelvűségének, és a helyesírási hibáknak köszönhetően az adatok sokfélék voltak.


Az első gondolatom az volt, hogy valamilyen felügyelet nélküli tanulásra (unsupervised learning) épülő módszert alkalmazzak, hiszen megkönnyítené a munkám, ha nem kellene pár ezer adatot egyenként csoportokba soroljak. Ilyen klaszterező például a K-means, melynek egy hasonlósági (távolság) függvényre van szüksége a csoportok meghatározásához, hasonlóan más klaszterezőkhöz. A szavakra alkalmazható távolságfüggvények részletes összehasonlítását a JoyOfData oldalon lehet elolvasni. Mindben az a közös, hogy csak az írásbeli (szintaktikai) különbségeket tudják kiküszöbölni, éppen ezért a szinonimákat és a különböző nyelven megadott szavakat nem képesek egymáshoz hasonlónak tekinteni, és így egy csoportba sorolni őket.  Emiatt döntöttem úgy, hogy saját kezűleg fogom az adatokat csoportosítani, ennek érdekében létrehoztam olyan „szótárakat” amelyek a különböző lakhelyeket, tanulmányi területeket, és szakterületeket csoportokba sorolja. A csoportosítás előtt 1781 tanulmányi területet, 4597 szakterületet, illetve 3600 lakhelyet tartalmazott az adathalmaz, a tísztítást követően ez 11-, 18-, és 12-re csökkent.


Az adattisztítást ezzel a Jupyter munkafüzettel végeztem, felhasznált könyvtárak között mindenképp  megemlíteném a pandas-t, mellyel könnyedén és hatékonyan lehet úgy strukturált, mint strukturálatlan adatokat kezelni és feldolgozni.



Statisztikák kinyerése és vizualizáció
Az adatok “tisztogatása” után a statisztikák kinyerése egyszerű feladatnak bizonyult, ezt ugyancsak a fennebb említett munkafüzettel valósítottam meg, majd a kinyert információkat json formátumban mentettem le a vizualizáláshoz.


Az adatvizualizáció egy újabb kihívás volt számomra, mert ezen a téren rendelkezek a legkevesebb tapasztalattal. Sokáig tanakodtam a különböző könyvtárak között, mint például a Tableau, D3.js, D3plus, Chart.js, végül a Plotly.js javascript könyvtárat választottam, részben azért, mert már használtam a Plotly Python API-t. Az elkészült diagramok magukban hordozzák a bejegyzés elején feltett kérdésekre a válaszokat, melyeket röviden be is mutatom.



Születési hely és tanulmányok kapcsolata
[iframe src="//plot.ly/~LorinczSzabolcs/13.embed" width="750px" height="600px"]


A fenti hőtérképről (interaktív, statikus) leolvashatóak a  tanulmányok és a születési helyek közötti összefüggések. Soronként értelmezve a hőtérképet megfigyelhetjük, hogy egy településen belül milyen tanulmányi területek népszerűbbek. Oszloponként értelmezve pedig tanulmányozhatjuk, hogy mely településekről származó emberek választanak többen egy adott tanulmányi területet. Minél világosabb egy téglalap, annál több ember választotta az adott tanulmányi területet az adott városból.


A rövid magyarázatot követően már egyszerűen észrevehetjük a világosabb oszlopok alapján, hogy a székely(földi)ek körében a legnépszerűbb tanulmányok a következőek: egészségügy, matematika/informatika, mérnöki/technológia, pénzügy/management, társadalomtudományok. Az is kitűnik sajnos, hogy az alkalmazott tudományokat (szakképzést) és az oktatást választók aránya alacsony.


A világosabb sorok (Marosvásárhely, Kolozsvár) azt jelképezik, hogy több adat származik az adott városban született emberektől, mint a sötétebb sorokat képviselő városokból. Ez is logikus, hiszen a nagyobb városokból több adatot lehet összegyűjteni. Kivételt képez Kovászna, innen szinte ugyanannyi adat származik, mint Kolozsvárról vagy Marosvásárhelyről, ezt különösnek is találtam. Feltételezem, hogy az adatok gyűjtésekor a Kovászna megyeiek belekerülhettek a Kovászna városból származók közé, ezért történt ez a növekedés. Előfordulhat ugyanakkor az is, hogy a Kovászna városban születettek szívesebben teszik közzé Facebook profiljukon a születési helyüket.


Fontos észrevenni, hogy a marosvásárhelyi emberek vesznek részt legnagyobb mértékben egészségügyi oktatásban, ez egybevág azzal, hogy ott található a Marosvásárhelyi Orvosi és Gyógyszerészeti Egyetem). Azt is érdemes kiemelni, hogy szakképzést választók főleg a kisebb településekről származnak.



Lakhely és tanulmányok kapcsolata
[iframe src="//plot.ly/~LorinczSzabolcs/7.embed" width="750px" height="600px"]


A tanulmányok és a lakhely (interaktív, statikus) között erősebb korreláció áll fent, ezt a kisebb számú, világosabb négyzet mutatja. Láthatjuk, hogy a Marosvásárhelyen lakók között népszerű az egészségügyi-, mérnöki-, társadalmi-, illetve informatika képzés. Ott található többek között a Marosvásárhelyi Orvosi és Gyógyszerészeti Egyetem (egészségügyi képzés) és a Sapientia Erdélyi Magyar Tudományegyetem (főként mérnöki-, társadalmi-, illetve informatika képzés), mely jól magyarázza az eddig észrevett információkat. A Kolozsváron lakók között a legnépszerűbb tanulmányi területek a matematika/informatika, a mérnöki/technológia, pénzügy/management, illetve a társadalomtudományok. Kolozsváron ezeket a tanulmányi területeket oktató intézmények: a  Babeș–Bolyai Tudományegyetem, és a Műszaki Egyetem. Kisebb csoportot képviselnek ugyan, de meg kell említeni a Kolozsváron lakók közül azokat, akik egészségügyi-, valamint művészeti oktatásban vesznek/vettek részt a következő intézmények keretein belül: Iuliu Hațieganu Orvosi és Gyógyszerészeti Egyetem, Kolozsvári Agrártudományi és Állatorvosi Egyetem, és a Művészeti és Design Egyetem. Szembetűnő még a Sepsiszentgyörgyön lakó társadalomtudományokat tanuló emberek száma, ez valószínüleg a BBTE Sepsiszentgyörgyi Kihelyezett Tagozatának köszönhető.



Lakhely és születési hely kapcsolata a szakterületekkel
[iframe src="//plot.ly/~LorinczSzabolcs/9.embed" width="750px" height="600px"]


Három fontos észrevételt tehetünk a foglalkozási területek esetén (interaktív, statikus), úgy születési hely, mint lakhely szerint csoportosítva. Az első, amelyről még később beszélek majd, hogy a foglalkozási területek városonkénti eloszlása nagyjából követi a tanulmányi területek eloszlását (arra utalva, hogy az emberek nagyjából el tudnak helyezkedni azon a területen belül, amit tanultak). A második egy kivétel az előbbi észrevétel alól, hogy  kimagaslóan sokan helyezkedtek el oktatásban, ellentétben azzal, hogy hányan választották ezt a területet tanulmányaikként. (Ez magyarázható azzal, hogy Romániában nincs dedikált tanári szak, csak opcionális modul, ezért sokan akik tanítani akarnak, nem kifejezett pedagógiai/didaktikai képzésen vesznek részt.) A harmadik észrevétel pedig az, hogy kimagaslóan sokan foglalnak el tulajdonosi/menedzseri pozíciót.



Tanulmányi területek és szakterületek kapcsolata
[iframe src="//plot.ly/~LorinczSzabolcs/11.embed" width="750px" height="500px"]


Erről (interaktív, statikus) a hőtérképről egy nagyon fontos információt olvashatunk le, hogy mennyire lehet az egyes tudományterületeket hasznosítani, tehát mennyire lehet elhelyezkedni az egyes területeken belül. A saját tudományterületüket nagy mértékben tudják hasznosítani az egészségügyi-, a matematika/informatikai-,  mérnöki-, művészeti-, és az oktatási képzést választók. Megfigyelhetjük továbbá a magyarázatot arra, hogy aránylag sok az oktató, annak ellenére, hogy kevesen végeztek oktatói képzést. Látható, hogy sokan oktatói pályán helyezkednek el a matematika/informatika, a humán tárgyak és a társadalomtudományok képviselői közül is. A sok sötét téglalap azt jelképezi, hogy minden egyes tanulmányi területen belül csupán egy-két szakterületre összpontosul az elhelyezkedés, és ez az egy-két szakterület többnyire összefüggésben van a tanulmányokkal, ami jó hír. A két legerősebb korrelációban álló tanulmányi-, és szakterület páros az egészségügy és az oktatás.



Összegzés
Mindent figyelembe véve, nagyon sok információt ki lehetett olvasni a rendelkezésre álló adatokból, és lehetne akár többet is. A diagramok rengeteg információt tartalmaznak, ezért érdemes figyelmesen fürkészni őket. Az itt bemutatott grafikonokon kívül továbbiakat is meg lehet tekinteni a projekt weboldalán, és el lehet olvasni a pályázatra benyújtott elemzésemet is.


Végül pedig szeretnék köszönetet mondani a pályázat kiírójának a lehetőségért, ugyanakkor a zsűri tagjainak a munkájukért, és az építő jellegű hozzászólásaikért. Ez a rövid adatelemzés és vizualizáció az első (és reményeim szerint nem az utolsó) ilyen jellegű munkám, és elmondhatom, hogy szívesen dolgoztam a rajta, sokat tanultam a lefolyása alatt.