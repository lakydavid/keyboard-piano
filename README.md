# 🎹 Billentyűzet Zongora

Egy **böngészőben futó zongora**, amit a számítógéped / laptopod billentyűzetén lehet játszani.
Nincs telepítés, nincs függőség — csak nyisd meg a `index.html` fájlt, és működik.

## Indítás

**A legegyszerűbb:** kattints duplán az `index.html` fájlra — megnyílik a böngészőben, és kész.

Vagy ha helyi szervert szeretnél (pl. fejlesztéshez):

```bash
# Python 3
python3 -m http.server 8000
# majd nyisd meg: http://localhost:8000
```

Vagy tedd fel **GitHub Pages**-re (Settings → Pages → Branch), és bárhonnan elérhető lesz egy linken.

## Kiosztás — kétkezes (split)

A billentyűzet két regiszterre van osztva, hogy mindkét kézzel egyszerre játszhass,
oktávváltogatás nélkül — mint egy igazi zongorán:

```
 DALLAM · jobb kéz · felső két sor (bázis C4)
   1   2       4   5   6       8   9       Ö      ← fekete hangok (számsor)
 Q   W   E   R   T   Z   U   I   O   P   Ő   Ú    ← fehér hangok (QWERTZ-sor)

 BASSZUS · bal kéz · alsó két sor (bázis C3)
   S   D       G   H   J       L   É            ← fekete hangok (ASDF-sor)
 Í   Y   X   C   V   B   N   M   ,   .   -        ← fehér hangok (alsó sor)
```

- **Jobb kéz (dallam):** fehér hangok a `QWERTZ` soron, fekete hangok a számsoron.
- **Bal kéz (basszus):** fehér hangok az alsó (`ÍYXCV…`) soron, fekete hangok az `ASDF` soron.
- **Sustain pedál:** `Space` — amíg nyomod, a felengedett hangok tovább csengenek
  (vagy kattints a „🦶 Space" gombra, hogy rögzítsd — hasznos érintőképernyőn).
- **Globális oktávváltás:** `←` / `→` nyilak (vagy a `−` / `+` gombok), ±3 oktáv.
- Egyszerre több billentyű is leüthető (polifónia), így akkordokat is játszhatsz.

A két zóna egy oktáv eltéréssel szól (basszus C3-tól, dallam C4-től), és a középső
regiszterben átfednek, így folyamatos skálát is játszhatsz a két kéz között.

## Funkciók

- **5 hangszín-preset:** Klasszikus zongora, Elektromos zongora, Orgona, Szintetizátor, Zenedoboz
- **Reverb (visszhang) effekt** — állítható mértékkel
- **Hangerő-szabályzó**
- **Oktávváltás** ±3 oktáv
- Kattintható / érintőképernyőn is játszható (mobil/tablet)

Minden a böngésző beépített **Web Audio API**-jával készül, valós időben — nincsenek
letöltött hangminták, így a teljes alkalmazás egyetlen kis HTML fájl.

## Megjegyzés a billentyűzethez

A kiosztás magyar (QWERTZ) billentyűzetre van hangolva (`É Á Ű`, `Ő`, `Z`).
Angol (QWERTY) kiosztáson is működik a fehér/fekete hangok többsége, és a `Z`
helyett `Y` is elfogadott a G# hanghoz. Ha bizonyos billentyűk nem szólnak, a
hangokra egérrel is rá lehet kattintani.
