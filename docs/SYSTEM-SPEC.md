### 01 — Ügyfélszerző rendszer

**Eredmény:** a jelentkezéstől az ügylet állapotáig egy követhető út. Nem ígér önmagában forgalmat vagy új ügyfelet; a látogatók megszerzése külön üzleti tevékenység.

**Bemenet:** szolgáltatás és célcsoport, jóváhagyott landing szöveg, érdeklődő neve/e-mailje/igénye, forrásjelölés, foglalási link, értékesítési szakaszok, kommunikációs szabályok.

**MVP:** egy szolgáltatás landingje és űrlapja; köszönőoldal; tartós leadlista; szerkeszthető AI-összefoglaló és választervezet; két utánkövetési tervezet; foglalási link; kézi pipeline; alap eseményszámlálók. A 02/03/07 rendszerek teljes képességeit nem kell beépíteni: ez az egyszerű végigérő út, később bővíthető modulokkal.

**Képernyők:** látogatóknak szánt landing (MVP-ben csak helyi előnézet, élesben nyilvános); jelentkezés visszaigazolása; belső érdeklődőlista; lead részlet és idővonal; szövegsablonok; áttekintés.

**Folyamat:** űrlap szerveroldali ellenőrzése → lead.created → összefoglaló → emberi ellenőrzés → válasz/foglalási link → foglalás állapotának rögzítése → ajánlat/nyert/vesztett. Szakaszok: új, átnézendő, kapcsolatfelvétel, foglalt, ajánlat, nyert, vesztett. Ugyanaz a beküldési azonosító egy rekordot hoz létre; ugyanazon személy új igénye külön lead lehet.

**AI feladata:** igény összefoglalása, saját szolgáltatáshoz kapcsolás, választervezet. Ár és eredményígéret csak jóváhagyott szolgáltatásadatból.

**Bekötött verzió:** tranzakciós levélküldés; foglalási webhook; válaszok és leiratkozások kezelése; ütemezett feladatok. Marketingüzenetek és az érdeklődésre adott válasz külön célként legyenek kezelve.

**Egyedi verzió:** több ajánlat, több értékesítő, forrás szerinti bontás, külső CRM. Hirdetéskezelés és automatikus hideg megkeresés nincs a V1-ben.

**Mérés:** új érdeklődések száma; medián idő az első emberileg jóváhagyott válaszig; foglalások; nyert ügyletek. Konverzióknál az időszak és a kohorsz különüljön el, 0 nevező esetén nincs adat.

**Elfogadási esetek:** 01-A: azonos beküldés kétszer → egy lead. 01-B: hibás e-mail → mezőszintű hiba, nincs küldés. 01-C: AI-kiesés → lead megmarad, kézi feldolgozás elérhető. 01-D: lemondott foglalás → nem számít aktívnak. 01-E: nyert státusz → függő értékesítési follow-up törlődik.


Tényleges készültség: CAPABILITIES.md. A specifikáció nem készültségi állítás.
