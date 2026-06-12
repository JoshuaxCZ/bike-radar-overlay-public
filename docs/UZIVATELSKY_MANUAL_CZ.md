# Bike Radar Overlay — Uživatelský manuál

---

## 1. Úvod

### 1.1 Co je Bike Radar Overlay?

Bike Radar Overlay je bezplatná Android aplikace pro cyklisty, která zobrazuje data z cyklistických radarů (Garmin Varia, Coospo TR70 a jiná podporovaná zařízení) jako plovoucí overlay přes jakoukoli navigační aplikaci.

**Hlavní funkce:**
- Zobrazuje vozidla za cyklistou jako barevné body nebo siluety aut
- Barevné rozlišení hrozby: zelená (daleko), oranžová (středně), červená (blízko)
- Zobrazení GPS rychlosti jako tachometr
- Cyklocomputer na lock screenu (při zamčeném telefonu)
- Podpora navigace (OsmAnd, Bike Route Planner)

### 1.2 Proč Bike Radar Overlay?

- **Bezpečnost:** Zobrazí vozidla za vámi, i když nevidíte přes rameno
- **Univerzálnost:** Funguje přes jakoukoli navigační aplikaci
- **Sledování:** Umožňuje sledovat, kolik vozidel vás předjelo během jízdy
- **Lock screen:** Zobrazí rychlost, vozidla, vzdálenost a navigaci i na zamčené obrazovce

---

## 2. Systémové požadavky

- **Android:** 8.0 (API 26) nebo novější
- **Bluetooth LE:** Vyžadováno pro připojení radaru
- **GPS:** Vyžadováno pro měření rychlosti
- **Přístup k notifikacím:** Pro integraci s OsmAnd
- **Overlay permission:** Pro zobrazení přes navigaci

---

## 3. Instalace

### 3.1 Instalace z Google Play Store

1. Otevřete Google Play Store na vašem telefonu
2. Zadejte do hledání: **Bike Radar Overlay**
3. Klikněte na **Instalovat**
4. Po dokončení stahování klikněte na **Otevřít**

### 3.2 Instalace z APK souboru

1. Stáhněte si APK soubor z GitHubu
2. Přeneste APK na telefon (např. přes USB nebo email)
3. Otevřete soubor a povolte instalaci z neznámých zdrojů
4. Klikněte na **Instalovat**

---

## 4. První spuštění a nastavení

### 4.1 Po spuštění aplikace

1. Aplikace vás upozorní na požadovaná oprávnění:
   - **Povolit overlay** — pro zobrazení přes navigaci
   - **GPS** — pro měření rychlosti
   - **Bluetooth** — pro připojení radaru
   - **Notifikace** — pro integraci s OsmAnd (volitelné)

2. Povolte všechna požadovaná oprávnění

### 4.2 Připojení radaru

1. Zapněte svůj radar (Garmin Varia, Coospo TR70 nebo jiné podporované zařízení)
2. V aplikaci klikněte na tlačítko **Hledat radar**
3. Čekejte, dokud se nezobrazí seznam BLE zařízení
4. Klikněte na vaše zařízení (např. "Varia RTL515" nebo "Coospo TR70")
5. Povolte párování v dialogu Androidu

Po párování se radar automaticky připojí a začne zobrazovat data.

### 4.3 Konfigurace nastavení

V hlavní obrazovce můžete nastavit:

| Nastavení | Popis |
|-----------|-------|
| **Smart Screen** | Automatické probuzení obrazovky při detekci vozidla |
| **Ponechat obrazovku zapnutou** | Obrazovka zůstává zapnutá po celou dobu jízdy |
| **Zobrazit tachometr** | Zobrazí GPS rychlost |
| **Zvuková upozornění** | Pípnutí při detekci vozidla |
| **Skrýt pruh bez vozidel** | Pruh se sbalí na baterii, když je cesta volná |
| **Jednotky** | km/h nebo mph (imperiální jednotky) |

**Důležité:** Po změně nastavení restartujte radar (tlačítko **Zastavit Radar**, poté **Start**).

---

## 5. Hlavní obrazovka

### 5.1 Stav připojení

| Stav | Popis |
|------|-------|
| **Připravena** | Aplikace je připravena k připojení radaru |
| **Připojování** | Probíhá připojení k radaru |
| **Připojeno** | Radar je připojen a sleduje vozidla |
| **Odpojeno** | Radar je odpojen |

### 5.2 Navigační menu (levý spodní roh)

| Položka | Popis |
|---------|-------|
| **Overlay — upravit rozmístění** | Přesun a změna velikosti pruhu |
| **Lock screen — upravit rozmístění** | Přesun pruhu na lock screenu |
| **Zvuková upozornění** | Nastavení zvuků |
| **Navigace** | Nastavení navigace (OsmAnd, BRP) |
| **PRO funkce** | Vysvětlení Pro verzí (když budou aktivní) |
| **Funkce** | Popis všech funkcí |
| **Manuál** | Tento manuál |
| **Historie jízd** | Prohlížení zaznamenaných jízd |

---

## 6. Základní funkce

### 6.1 Radarový pruh

**Co je to radarový pruh?**

Radarový pruh je tenký proužek, který se zobrazí v horní části obrazovky. Zobrazuje:

- **Baterii radaru** (např. "85") — levý horní roh
- **Vozidla** — jako tečky nebo siluety aut

**Barevné kódy hrozby:**

Upřesnění: Každý výrobce definuje úrovně hrozby jinak:

**Garmin Varia (3 úrovně):**
- 🟢 **Zelená (LOW)**: Vozidlo se přibližuje pomalu
- 🟠 **Oranžová (MEDIUM)**: Vozidlo se přibližuje středně rychle  
- 🔴 **Červená (HIGH)**: Vozidlo se přibližuje rychle
- *Poznámka:* Garmin Varia používá relativní rychlost vozidla k určení hrozby

**Coospo TR70 (2 úrovně):**
- 🟢 **Zelená (LOW)**: Vozidlo je daleko
- 🔴 **Červená (HIGH)**: Vozidlo je blízko
- *Poznámka:* Coospo TR70 používá pouze 2 úrovně hrozby, bez mezikroku MEDIUM

### 6.2 Tachometr (speed widget)

**Co je to tachometr?**

Tachometr je okénko s aktuální rychlostí, které můžete umístit kdekoli na obrazovku.

**Jak přepínat mody:**

Jednoduchým kliknutím na tachometr přepínáte mezi:
1. **Rychlost** — aktuální GPS rychlost (např. "27 km/h")
2. **Trip** — vzdálenost aktuální jízdy (např. "12.3 km")
3. **ODO** — celková vzdálenost (např. "847.5 km")

**Jak změnit velikost:**

1. Zapněte **Upravit rozložení**
2. Klikněte na **Upravit velikost overlay**
3. V panelu spodním najdete tlačítka **+** a **−** pro tachometr
4. Tlačítkem **+** zvětšíte, **−** zmenšíte
5. Klikněte **Uložit rozložení**

### 6.3 Upravit rozložení

**Co můžete upravovat:**

| Prvek | Co lze upravit |
|-------|----------------|
| **Radarový pruh** | Pozice (přetáhnout), šířka, výška, velikost teček, styl (tečky/siluety) |
| **Tachometr** | Pozice (přetáhnout), velikost (šířka/výška) |

**Jak upravit:**

1. Klikněte na **Upravit rozložení**
2. Zobrazí se modrý obrazec a panel níže
3. **Přetahujte** pruh a tachometr prstem na požadované místo
4. **Upravte velikost** pomocí sliderů v panelu
5. Klikněte na **Uložit rozložení** (v panelu)

**Tip:** Panel se objeví vždy při kliknutí na pruh nebo tachometr (když je v edit módu).

---

## 7. Lock screen a Smart Screen

### 7.1 Lock screen displej

**Co je to lock screen displej?**

Lock screen displej je "cyklocomputer", který se zobrazí na zamčené obrazovce. Umožňuje sledovat rychlost, vozidla, navigaci a vzdálenost bez odblokování telefonu.

**Jak povolit:**

1. Zapněte **Smart Screen** nebo **Ponechat obrazovku zapnutou** v nastavení
2. Zámek telefonu při jízdě (zakliknutí na bok, sněním nebo gestem)
3. Obrazovka se probudí automaticky při detekci vozidla nebo při přiblížení k manévru

**Co lock screen zobrazuje:**

| Sekce | Informace |
|-------|-----------|
| **Horní část** | Baterie radaru (číslo) + vozidla (tečky) |
| **Střední část** | Rychlost (27 km/h), počet vozidel (2), vzdálenost (85 m) |
| **Spodní část** | Trip (14.2 km) + ODO (1284 km) |
| **Navigační část** | Šipka, vzdálenost, instrukce, ETA |

### 7.2 Smart Screen

**Co je to Smart Screen?**

Smart Screen automaticky probouzí obrazovku při detekci vozidla za vámi nebo při přiblížení k navigačnímu manévru.

**Jak Smart Screen funguje:**

1. **Probuzení při vozidle:** Když radar detekuje vozidlo blízko vás, obrazovka se probudí
2. **Probuzení při navigaci:** Když jste blízko manévru (< 200 m), obrazovka se probudí
3. **Vypnutí:** Po uplynutí časového limitu (nastavitelné v nastavení) se obrazovka zhasne

**Nastavení Smart Screen:**

| Nastavení | Popis |
|-----------|-------|
| **Smart Screen ON** | Zapne/vypne Smart Screen |
| **Timeout** | Doba po kterou zůstává obrazovka zapnutá (5–60 sekund) |

### 7.3 Ponechat obrazovku zapnutou

**Co je to Ponechat obrazovku zapnutou?**

Tato funkce udržuje obrazovku zapnutou po celou dobu jízdy. Použijte, pokud potřebujete mít vše vždy vidět.

**Důležité:** Smart Screen a Ponechat obrazovku zapnutou nelze použít současně — zapnutí jednoho automaticky vypne druhé.

---

## 8. Sound alerts (zvuková upozornění)

### 8.1 Pět typů alertů

| Event | Popis | Kdy se přehraje |
|-------|-------|-----------------|
| **New vehicle** | Nové vozidlo | Když radar detekuje nové vozidlo |
| **Threat LOW** | Malá hrozba | Když je vozidlo daleko |
| **Threat MEDIUM** | Střední hrozba | Když se vozidlo přibližuje |
| **Threat HIGH** | Vysoká hrozba | Když je vozidlo blízko |
| **All clear** | Vše volno | Když vozidla zmizí |

### 8.2 Konfigurace alertů

Každý alert má tři parametry:

| Parametr | Rozsah | Popis |
|----------|--------|-------|
| **Frekvence** | 200–4000 Hz | Výška tónu (číslo v Hz) |
| **Počet pípnutí** | 1–3 | Kolikrát se pípne |
| **Délka** | 50–500 ms | Jak dlouho trvá jedno pípnutí |

**Jak nastavit:**

1. Klikněte na **Zvuková upozornění**
2. Klikněte na **Přehrát** u každého alertu, abyste uslyšeli výsledek
3. Upravte parametry pomocí sliderů nebo vstupních polí
4. Klikněte **Uložit** (pokud je vidět) nebo **Zpět**

### 8.3 Příklady nastavení

**Rychlý alert (vysoká hrozba):**
- Frekvence: 2000 Hz
- Počet: 1
- Délka: 100 ms

**Upozornění (nízká hrozba):**
- Frekvence: 800 Hz
- Počet: 2
- Délka: 150 ms

---

## 9. Navigace

### 9.1 Podporované aplikace

| Aplikace | Metoda | Nutná oprávnění |
|----------|--------|-----------------|
| **OsmAnd** | Notifikace | Přístup k notifikacím |
| **Bike Route Planner** | Broadcast | Žádná (explicitní broadcast) |

### 9.2 Nastavení OsmAnd

1. V aplikaci klikněte na **Navigace**
2. Zapněte **OsmAnd**
3. Otevřete **Nastavení Androidu** → **Speciální přístup** → **Přístup k notifikacím**
4. Povolte **Bike Radar Overlay**

### 9.3 Nastavení Bike Route Planner (BRP)

1. V aplikaci klikněte na **Navigace**
2. Zapněte **Bike Route Planner**
3. V BRP otevřete **Navigation settings**
4. Povolte **Send navigation data to Bike Radar**

### 9.4 Co navigace zobrazuje

| Prvek | Popis |
|-------|-------|
| **Šipka** | Směr (↑ rovně, ← vlevo, → vpravo, atd.) |
| **Vzdálenost** | Vzdálenost k manévru (např. "320 m") |
| **Instrukce** | "Odbočte vlevo", "Kruhový objezd", atd. |
| **Ulice** | Název ulice |
| **ETA** | Čas do příjezdu (např. "8.3 km | 24 min | 14:47") |

**Barvy vzdálenosti:**
- **Bílá** | > 100 m
- **Žlutá** | ≤ 100 m
- **Červená** | ≤ 50 m

---

## 10. Historie jízd

### 10.1 Co se ukládá

Každá jízda (s délkou minimálně 10 minut) se uloží s následujícími daty:

- Datum a čas zahájení
- Celková vzdálenost (trip)
- Celková doba trvání
- Počet detekovaných vozidel
- Režim správy obrazovky (Smart Screen / Keep ON)
- Úspora baterie (pro Smart Screen)

### 10.2 Jak procházet historii

1. Klikněte na **Historie jízd** v menu
2. Zobrazí se všechny zaznamenané jízdy v seznamu
3. Každá jízda ukazuje:
   - Datum a čas
   - Vzdálenost a dobu
   - Počet vozidel
   - Barový graf úspory baterie (zelená = čas, kdy byla obrazovka vypnutá díky Smart Screen)

### 10.3 Agregátní statistiky

V horní části historie se zobrazují:
- **Celkový počet jízd**
- **Celková doba v hodinách**
- **Průměrná úspora baterie** (pouze pro Smart Screen jízdy)

---

## 11. Všechny funkce zahrnuty

Všechny funkce popsány v tomto manuálu jsou součástí bezplatné verze aplikace. Aktuálně neexistuje žádná oddělená Pro verze - veškerá funkčnost je dostupná pro všechny uživatele.

---

## 12. Řešení problémů

### 12.1 Radar se nepřipojuje

**Problém:** Aplikace hledá, ale nenajde žádné zařízení.

**Řešení:**
1. Ujistěte se, že radar je zapnutý a v dosahu (max. 200 m)
2. Restartujte radar (vypněte a zapněte znovu)
3. Restartujte Bluetooth na telefonu
4. V aplikaci klikněte na **Zapomenout** a znovu na **Hledat radar**

### 12.2 Vzdálenost není přesná

**Problém:** Zobrazená vzdálenost se liší od skutečné.

**Poznámka:** Vzdálenost je orientační a závisí na:
- Typu radaru (Garmin Varia vs Coospo TR70)
- Směru radaru (řízení směrem od vozidel)
- Prostředí (urban canyon, lesy)

### 12.3 Smart Screen se neprobouzí

**Problém:** Obrazovka se neprobouzí při detekci vozidla.

**Řešení:**
1. Zkontrolujte, zda je zapnutý **Smart Screen** v nastavení
2. Povolte **Povolit výjimku z režimu nevypadávání** v nastavení baterie telefonu
3. Ujistěte se, že aplikace nemá omezenou pozadí (v nastavení baterie)

### 12.4 Zvuk se nepřehrává

**Problém:** Některé nebo všechny zvuky se nepřehrávají.

**Řešení:**
1. Zkontrolujte hlasitost telefonu
2. Zkontrolujte nastavení zvuku v aplikaci
3. Restartujte radar (tlačítko **Zastavit Radar**, poté **Start**)
4. Ujistěte se, že v nastavení baterie není omezena aplikace

### 12.5 Tachometr nezobrazuje rychlost

**Problém:** Tachometr je prázdný nebo zobrazuje "--".

**Řešení:**
1. Zapněte **GPS** v nastavení
2. Vyčkejte 10–30 sekund, dokud aplikace nepřijme signál z GPS
3. Pohybujte se nebo vychozí na místo s lepším GPS signálem (ven)

### 12.6 Aplikace se zasekne nebo se neodpovídá

**Problém:** Aplikace neběží správně.

**Řešení:**
1. Ukončete aplikaci (dlouhým stiskem Home/Recent apps a přejetím aplikace pryč)
2. Restartujte aplikaci
3. Pokud problém přetrvává, odinstalujte a znovu nainstalujte aplikaci

---

## 13. Podpora

### 13.1 Jak získat podporu

Pokud máte problém, který není řešen v této příručce:

1. V aplikaci klikněte na **Log** v dolní části hlavní obrazovky
2. Klikněte na **Kopírovat** a připojte log do zprávy
3. Poslete e-mail na: support@vgos.cz nebo vytvořte issue

### 13.2 Podpora

Pokud potřebujete další pomoc, napište na support@vgos.cz

---

## 14. Díky

Děkuji, že používáte Bike Radar Overlay!

Tato aplikace byla vytvořena s cílem zvýšit bezpečnost cyklistů a zpříjemnit jízdu na kole.

---

**Verze:** 0.9.42  
**Datum:** 2026-06-12  
**Autorské právo:** © 2026 David Urbancik
