# HTML5 Tables & Bootstrap - Kurzy

Cvičení zaměřené na tvorbu sémantických HTML tabulek s využitím Bootstrap 5 frameworku.

[Hotový web - live preview](https://shiny-bassoon-7ep1ozk.pages.github.io/done.html).

## Cíl cvičení

Vytvořit komplexní tabulku s registrací do kurzů, která bude obsahovat:
- Správnou strukturu HTML5 tabulky
- Sémantické značky a atributy
- Stylování pomocí Bootstrap 5 tříd
- Interaktivní prvky (checkboxy, switche)

## Zadání

V souboru `index.html` najdete připravený startovací kód s:
- Hlavičkou stránky
- Kontejnerem pro tabulku (zatím prázdný)
- Pomocným blokem s prvky, které budete potřebovat
- Tlačítky a info alertem

**Vaším úkolem je vytvořit tabulku s přehledem kurzů**, která bude obsahovat následující kurzy rozdělené do 3 kategorií:

### Začátečnické kurzy
1. **HTML & CSS základy**
   - Lektor: Mgr. Jana Nováková
   - Cena: 2 500 Kč
   - Volná místa: 15/20
   - Popis: Naučte se základy značkovacího jazyka HTML5 a kaskádových stylů CSS3. Kurz zahrnuje sémantické značky, flexbox, grid a responzivní design.
   - Termín: Úterý 16:00-18:00 | Začátek: 15. 1. 2026

2. **JavaScript pro začátečníky**
   - Lektor: Ing. Petr Svoboda
   - Cena: 3 200 Kč
   - Volná místa: 8/15
   - Popis: Úvod do programování v JavaScriptu. Proměnné, funkce, podmínky, cykly, práce s DOM a základy událostí.
   - Termín: Čtvrtek 17:00-19:00 | Začátek: 20. 1. 2026

### Pokročilé kurzy
3. **React - moderní framework**
   - Lektor: Bc. Martin Dvořák
   - Cena: 4 500 Kč
   - Volná místa: 0/12 (obsazeno!)
   - Popis: Naučte se vytvářet moderní webové aplikace pomocí React frameworku. Komponenty, hooks, state management a propojení s API.
   - Termín: Středa 18:00-20:30 | Začátek: 10. 2. 2026

4. **Node.js & Express**
   - Lektor: Mgr. Lukáš Černý, Ph.D.
   - Cena: 4 800 Kč
   - Volná místa: 7/12
   - Popis: Backend development s Node.js a Express frameworkem. REST API, databáze, autentizace a deployment.
   - Termín: Pátek 16:30-19:00 | Začátek: 5. 2. 2026

### Designové kurzy
5. **UI/UX Design principy**
   - Lektor: MgA. Karolína Bílá
   - Cena: 3 800 Kč
   - Volná místa: 12/16
   - Popis: Základy uživatelského rozhraní a uživatelské zkušenosti. Figma, wireframing, prototyping a designové systémy.
   - Termín: Pondělí 17:00-19:30 | Začátek: 25. 1. 2026

6. **Responzivní webdesign**
   - Lektor: Bc. Tomáš Zelený
   - Cena: 3 000 Kč
   - Volná místa: 2/10
   - Popis: Pokročilé techniky responzivního designu. Mobile-first přístup, media queries, CSS Grid, Flexbox a optimalizace pro různá zařízení.
   - Termín: Úterý 18:00-20:00 | Začátek: 28. 1. 2026

## Struktura HTML5 tabulky

### Důležité atributy

#### `scope` - definuje rozsah hlavičkové buňky
- `scope="col"` - hlavička sloupce
- `scope="row"` - hlavička řádku
- `scope="colgroup"` - hlavička skupiny sloupců
- `scope="rowgroup"` - hlavička skupiny řádků

#### `rowspan` - spojení buněk vertikálně
```html
<td rowspan="2">Obsah přes 2 řádky</td>
```

#### `colspan` - spojení buněk horizontálně
```html
<td colspan="3">Obsah přes 3 sloupce</td>
```

### Sémantické značky v tabulce
- `<th>` - hlavičková buňka (použijte pro názvy kurzů, kategorie)
- `<td>` - datová buňka (použijte pro lektory, ceny, volná místa)
- `<caption>` - titulek tabulky (umístěte jako první element uvnitř `<table>`)

## Bootstrap 5 třídy - Přehled

### Tabulky - základní třídy
| Třída | Popis |
|-------|-------|
| `.table` | Základní třída pro tabulku (povinná!) |
| `.table-striped` | Pruhované řádky (zebra pattern) |
| `.table-hover` | Hover efekt na řádcích |
| `.table-responsive` | Responzivní scroll (obalovací div!) |
| `.align-middle` | Vertikální zarovnání na střed |

### Barevné styly řádků a buněk
| Třída | Použití |
|-------|---------|
| `.table-primary` | Primární barva (modrá) - pro hlavičku |
| `.table-light` | Světlá - pro názvy kategorií |
| `.table-success` | Zelená - dostupné kurzy |
| `.table-danger` | Červená - obsazené kurzy |

### Barevné třídy pro stav míst (text)
| Třída | Barva | Kdy použít |
|-------|-------|------------|
| `.text-success` | Zelená | Hodně volných míst (15/20, 12/16) |
| `.text-warning` | Žlutá/oranžová | Méně míst (8/15, 7/12) |
| `.text-danger` | Červená | Obsazeno nebo skoro plno (0/12, 2/10) |

### Typografie
| Třída | Popis |
|-------|-------|
| `.fw-semibold` | Polotučné písmo |
| `.text-muted` | Ztlumená barva textu |
| `.text-center` | Zarovnání na střed |
| `.text-secondary` | Sekundární barva |
| `.fs-5` | Velikost písma |

### Layout a rozestupy
| Třída | Popis |
|-------|-------|
| `.mt-1`, `.mt-2`, `.mt-4` | Margin top (1-5) |
| `.mb-0`, `.mb-3` | Margin bottom |
| `.p-3`, `.p-4` | Padding |
| `.d-block` | Display block |

### Caption
```html
<caption class="caption-top p-3 fs-5 fw-semibold text-secondary">
  Přehled dostupných kurzů - školní rok 2025/2026
</caption>
```
- `.caption-top` - umístí caption nad tabulku
- Přidejte padding, velikost písma a barvu pro lepší vzhled

## 💡 Tipy a postupy

### 1. Colgroup pro lepší strukturu
Před `<thead>` přidejte:
```html
<colgroup>
  <col>
</colgroup>
<colgroup>
  <col span="3">
</colgroup>
<colgroup>
  <col>
</colgroup>
```
Toto seskupuje sloupce: Název | Lektor+Cena+Místa | Registrace

### 2. Barvy podle stavu
- **15/20, 12/16** → `.text-success` (hodně míst)
- **8/15, 7/12** → `.text-warning` (méně míst)
- **0/12, 2/10** → `.text-danger` (obsazeno/skoro plno)
- Kurz React (0/12) → checkbox `disabled`, řádek `.table-danger`

### 3. Responzivita
Obalte celou tabulku do:
```html
<div class="table-responsive rounded">
  <table class="table ...">
  ...
  </table>
</div>
```

### 4. ID pro formulářové prvky
Každý checkbox/switch musí mít:
- Unikátní `id` (např. `htmlBasics`, `switchBeginners`)
- Odpovídající `for` v labelu
- Používejte camelCase názvy

**Switche pro kategorie:**
- `switchBeginners` - Začátečnické
- `switchAdvanced` - Pokročilé
- `switchDesign` - Designové

**Checkboxy kurzů:**
- `htmlBasics` - HTML & CSS základy
- `jsBasics` - JavaScript pro začátečníky
- `reactCourse` - React (disabled!)
- `nodeCourse` - Node.js & Express
- `uiuxCourse` - UI/UX Design principy
- `rwdCourse` - Responzivní webdesign

## Dokumentace

- [Bootstrap 5 Tables](https://getbootstrap.com/docs/5.3/content/tables/)
- [Bootstrap 5 Forms](https://getbootstrap.com/docs/5.3/forms/overview/)
- [MDN - HTML Tables](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/table)
