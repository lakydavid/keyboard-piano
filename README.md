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
   2   3       5   6   7       9   Ö       Ó      ← fekete hangok (számsor)
 Q   W   E   R   T   Z   U   I   O   P   Ő   Ú    ← fehér hangok (QWERTZ-sor)

 BASSZUS · bal kéz · alsó két sor (bázis C3)
   A   S       F   G   H       K   L            ← fekete hangok (ASDF-sor)
 Í   Y   X   C   V   B   N   M   ,   .   -        ← fehér hangok (alsó sor)
```

A fekete billentyűk a **valódi billentyűzet-pozícióhoz** igazodnak: a fél billentyűnyi
sor-elcsúszás (row stagger) miatt a fekete hang mindig a fehértől jobbra-fel esik, pont
mint az igazi zongorán. Ez Dell és MacBook magyar billentyűzeten egyaránt stimmel.

- **Jobb kéz (dallam):** fehér hangok a `QWERTZ` soron, fekete hangok a számsoron.
- **Bal kéz (basszus):** fehér hangok az alsó (`ÍYXCV…`) soron, fekete hangok az `ASDF` soron.
- **Sustain pedál:** `Space` — amíg nyomod, a felengedett hangok tovább csengenek
  (vagy kattints a „🦶 Space" gombra, hogy rögzítsd — hasznos érintőképernyőn).
- **Globális oktávváltás:** `←` / `→` nyilak (vagy a `−` / `+` gombok), ±3 oktáv.
- Egyszerre több billentyű is leüthető (polifónia), így akkordokat is játszhatsz.

A két zóna egy oktáv eltéréssel szól (basszus C3-tól, dallam C4-től), és a középső
regiszterben átfednek, így folyamatos skálát is játszhatsz a két kéz között.

## Funkciók

- **7 hangszín-preset valódi hangszer-mintákkal:** Zongora, Elektromos zongora, Orgona,
  Vibrafon, Vonósok, Szintetizátor, Zenedoboz
- **Reverb (visszhang) effekt** — állítható mértékkel
- **Hangerő-szabályzó**
- **Sustain pedál** (`Space`)
- **Oktávváltás** ±3 oktáv
- Kattintható / érintőképernyőn is játszható (mobil/tablet)

## Daltanító mód

A felső panelen a **🎵 Daltanító** legördülőből választhatsz egy dalt, és a zongorán
**zölden kivilágosodnak a lenyomandó billentyűk**. Ahogy lejátszod őket, magától lép a
következő hangra/akkordra:

- **🔊 Mutasd** — eljátssza neked az aktuális lépést
- **▶ Lejátszás** — végigjátssza a teljes dalt demóként
- **◀ / ▶** — lépkedés kézzel, **⟲ Újra** — elölről

Beépített dalok (mind közismert / közkincs):
**Csillag-dal**, **Örömóda** (Beethoven), **Happy Birthday**, és egy
**négy-akkordos menet (C–G–Am–F)** — ez utóbbival rengeteg popdalt el lehet kísérni.

## Hogyan szól ilyen szépen?

A hangszerek **valódi felvett mintái** (GM SoundFont) töltődnek be a
[gleitz/midi-js-soundfonts](https://github.com/gleitz/midi-js-soundfonts) ingyenes,
szabadon használható gyűjteményéből (egy CDN-ről), és a böngésző **Web Audio API**-ján
keresztül szólalnak meg — a reverb effekt is itt készül. Az első billentyűleütéskor
töltődnek be a minták (a panelen látod a státuszt). Ha valamiért nem érhető el az
internet, az app **automatikusan visszavált** a beépített szintetizált hangokra, hogy
mindig szóljon valami.

## Megjegyzés a billentyűzethez

A kiosztás magyar (QWERTZ) billentyűzetre van hangolva (`É Á Ű`, `Ő`, `Z`).
Angol (QWERTY) kiosztáson is működik a fehér/fekete hangok többsége, és a `Z`
helyett `Y` is elfogadott a G# hanghoz. Ha bizonyos billentyűk nem szólnak, a
hangokra egérrel is rá lehet kattintani.
