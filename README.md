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

## Kiosztás

A billentyűzet úgy van leképezve, mint egy igazi zongora: az **`A`** billentyű a C alaphang,
a fölötte lévő **`W`** a félhang (C#), és így tovább felfelé.

```
Fekete (módosított) hangok – felső sor:
   W   E       T   Z   U       O   P       Ő
 A   S   D   F   G   H   J   K   L   É   Á   Ű
Fehér hangok – középső sor (C-től G-ig)
```

- **Fehér billentyűk:** `A S D F G H J K L É Á Ű` (12 db)
- **Fekete billentyűk:** `W E T Z U O P Ő` (8 db)
- **Oktávváltás:** `←` / `→` nyilak (vagy a `−` / `+` gombok)
- Egyszerre több billentyű is leüthető (polifónia), így akkordokat is játszhatsz.

### Hány oktáv ez?

Az `A`-tól `Ű`-ig terjedő 12 fehér billentyű a C-dúr skála 12 hangja, ami **1 oktáv + egy kvint**,
vagyis kb. **1,7 oktáv** (C4-től G5-ig). A fekete hangokkal együtt összesen **20 hang** szól.
Ha többre van szükséged, az `←` / `→` nyilakkal ±3 oktávot tolhatsz a kiosztáson.

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
