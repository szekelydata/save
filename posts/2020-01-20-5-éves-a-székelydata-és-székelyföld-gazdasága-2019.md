---
title: 5️⃣ éves a Székelydata 🎂 és Székelyföld Gazdasága 2019
date: 2020-01-20 20:48:33
---


Ez egy régebbi bejegyzés második frissítése.
Itt olvashatod az első frissítést.
5️⃣ évvel ezelőtt született meg az első bejegyzés a **székelydata** blogon 🎉 ! Mivel ez  **Székelyföld Gazdaságát** mutatta be, most ugyanezt a témát honoráljuk, 5 évvel frissebb adatokkal.


✴ Egy hasonló frissítést már a tavaly is elvégeztünk, akkor használtuk ezen a blogon először (az akkor még teljesen új) Flourish eszközzel készített **interaktív vizualizációkat**.





🚩 2019-ben megtartottuk az **I. erdélyi adatvizualizációs mini-konferenciát**, elkészítettük a **medvetérképet**, a **nagy népi időjóslás teszt**et, illetve **klímaváltozás-adatokat** használva meghirdettük a **II. erdélyi adatvizualizációs verseny**t, amit a **II. erdélyi adatvizualizációs mini-konferenciá**n élőben **díjaztunk**!


▶ Ugyanakkor, **Marosvásárhelyen ****(1, 2)**, **Budapesten** és **Kolozsváron** is látthatok székelydatás előadásokat.




👍 2020-ra a **Facebook** oldalunkat már **2700**-an követik.



Mint minden évben, az **omnibus.ro** cégportál 2019-ben is elkészítette a székelyföldi cégek toplistáját. Erre most a 2015-2018 között jegyzett adatok kerültek fel. A cégeket **árbevétel** és az **alkalmazottak száma** szerint rangsorolták. Ezeket a számokat kibővítettük a tavaly elemzett 2014-es adatokkal és így vizsgáltuk az eredményeket. Az alábbi **interaktív** Flourish vizualizációban a ◀▶ gombokkal lépegethetsz a sztoriban. Ez az eszköz kiemelkedően jó a történetmesélésben, és mivel kompatibilis Vega-val, gyakorlatilag bármilyen viz beágyazása lehetséges - illetve az adatvizualizációt kezdőként tanuló diákok is nagy kedvence, mert viszonylag szelíd a tanulási görbéje. **(🕹️ interaktív)**




[iframe height="700" src="https://public.flourish.studio/story/163324/embed"]



Az omnibus.ro által közzétett listát kísérte két (3D-s) tortadiagram is:












Ezek közül az elsőt átvette a Székelyhon napilap és a szekelyhon.ro portál is. Csakhogy **a Székelyhon értelmezése hibás volt, mind a portálon, mind a napilapban**: a tortadiagram a **székelyföldi top 50** céget mutatja, es **nem a régiók szerinti lebontást**. Ezért helytelen a többi cég ráhelyezése a tortadiagrammra, mert így azt a **torz benyomást kelti**, hogy mondjuk az egész Gyergyószék régió 2%-ot jelent, holott **a valós szám háromszor ekkora**. Itt a fő hiba a **kontextus** elhagyása volt: az omnibus.ro tortadiagramjának számait használták, hiába voltak ott **a táblázatok a helyes számokkal**. Az már csak **hab a tortán** (vagy tortadiagrammon? 😈), hogy a Székelyhon az omnibus.ro **foglalkoztatói top 50**-es diagram (második ábra) számait vette át és mutatta be, mint **árbevétel szerinti top 50**. De még nincs vége... 😂










**Sajnos az eredeti**, csak a székelyföldi top 50 céget figyelembe vevő **omnibus.ro-s diagram is kontextuálisan hibás**. Így néz ki arányosan, a diagram fölött bemutatott táblázatot használva:




 




[iframe height="400" src="https://app.powerbi.com/view?r=eyJrIjoiYjkyZDBjYTgtZDExMy00YmMzLWI1Y2YtMWQ3OTJkZjBlM2NjIiwidCI6IjUxMGM0Y2MwLTdiMDctNGIyOC05Yjk5LWY2YzMzMDEwMjA5ZiIsImMiOjh9"]




 




Azaz az  árbevétel szerinti top 50 székelyföldi cégek ***árbevételének*** 75%-a marosszéki. Itt az történt, hogy az omnibus.ro a ***cégek számát** *jelenítette meg a tortadiagrammon (3. és 4. oldal a fenti beágyazott vizualizációban). Ez viszont helytelen, mert - ha már mindeképpen tortadiagrammon szeretnénk a cégeket összehasonlítani - abszolút nem mindegy,  hogy van egy mammutcég, vagy 25 törpecég egy adott megyéből...





Helyesen, **minden céget figyelembe véve**, ez a tortadiagram így néz ki:




[iframe height="700" src="https://public.flourish.studio/visualisation/1259853/embed"]



**ADATOK + KÓD:** Az adatokat ezzel a Jupyter notebook-kal dolgoztuk fel, Ez volt az iparágakra való lebontás, és ez a végső formázás. A közbirtokosságok térképét ezzel a munkafüzettel készítettük el. Az interaktív vizualizációhoz a Flourish-t és PowerBI-t használtunk. Az adatok forrása az omnibus.ro volt.


A poszt célja nem a hajszálpontos adatszolgáltatás, hanem az, hogy egy általános képet adjon a székelyföldi régióban létező cégek jelenlegi gazdasági helyzetről és regionális eloszlásukról. Az iparágakba történő besorolás korántsem tökéletes és valószínüleg finomítható. Jelen célra, azonban ez a megközelítés megfelelt.