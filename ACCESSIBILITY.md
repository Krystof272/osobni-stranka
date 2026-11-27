# Zpráva o přístupnosti

Příklady řádků nahraďte vlastními výsledky. Zapište alespoň tři skutečné nálezy
a u každého hash commitu, který ho opravil (najdete ho v `git log --oneline`).

## Výsledky nástrojů

| Nástroj | Před opravami | Po opravách |
| --- | --- | --- |
| Lighthouse (Accessibility) | 75/100/100/91 | 100/100/100/91 |
| WAVE (Errors a Contrast Errors) | 10/10 | 10/10 |
| Test klávesnicí | funguje | funguje |

## Nalezené problémy a jejich opravy

| Problém | Jak jsem ho našel | Oprava (commit) | Kritérium WCAG |
| --- | --- | --- | --- |
| Například: odkaz „Více“ bez popisu | WAVE | `a1b2c3d` | 2.4.4 |
| format obrazku | Lighthouse | 'f06d270' | 1.4.5 |
| rozliseni obrazku | Lighthouse | 'f06d270' | 1.4.5 |
| opraveni main fokus | kontrola 2.4.1 | '79e0076' | 2.4.1

## Test media rules

| Nastavení | Co jsem při emulaci viděl | V pořádku |
| --- | --- | --- |
| prefers-color-scheme: dark | Barvy pozadí, textu, odkazů a karet se přepnou na tmavou paletu, aby stránka odpovídala nastavení zařízení. | Ano |
| prefers-contrast: more | Pozadí zbělá, text zčerná, odkazy se podtrhnou a okraje zesílí, aby se obsah lépe rozlišoval. | Ano |
| prefers-reduced-motion: reduce | Animace, přechody a plynulé rolování se vypnou, aby se omezil rušivý pohyb. | Ano |
| prefers-reduced-transparency: reduce | Průhledné pozadí karet se změní na plnou barvu a vypne se rozostření, aby byl obsah čitelnější. | Ano |
| forced-colors: active | Použijí se systémové barvy a viditelné okraje i fokus, aby ovládací prvky zůstaly rozeznatelné ve vynuceném schématu. | Ano |
| prefers-color-scheme: dark a prefers-contrast: more | Kombinace použije černé pozadí, bílý text a žluté odkazy, aby zůstal vysoký kontrast i v tmavém režimu. | Ano |

## Kritéria WCAG 2.2 úrovně A a AA

Specifikace: https://www.w3.org/TR/WCAG22/ (kritérium najdete podle čísla).
Úrovně A a AA mají dohromady 55 kritérií (31 úrovně A a 24 úrovně AA). Kritérium
4.1.1 Parsing bylo ve verzi 2.2 odstraněno, proto v tabulce není.

U každého kritéria nahraďte TODO. Ve sloupci Stav ponechte jedno ze tří slov:

- **Splněno**: do posledního sloupce napište, kde a jak (například „všechny obrázky mají alt“).
- **Nevztahuje se**: do posledního sloupce napište, proč (například „na stránce není video“).
- **Nesplněno**: kritérium opravte a stav změňte. V odevzdané verzi nesmí zůstat žádné
  Nesplněno ani TODO.

Kritéria označená „nové“ přibyla ve verzi 2.2.

### 1 Perceivable (vnímatelnost)

| Kritérium | Název | Úroveň | Stav | Kde a jak / proč ne |
| --- | --- | --- | --- | --- |
| 1.1.1 | Non-text Content | A | Splněno | Všechny významné fotografie mají atribut `alt` popisující jejich obsah. |
| 1.2.1 | Audio-only and Video-only (Prerecorded) | A | Nevztahuje se | Stránka neobsahuje předem nahrané ani živé audio ani video. |
| 1.2.2 | Captions (Prerecorded) | A | Nevztahuje se | Stránka neobsahuje předem nahrané video ani audio, které by vyžadovalo titulky. |
| 1.2.3 | Audio Description or Media Alternative (Prerecorded) | A | Nevztahuje se | Stránka neobsahuje předem nahrané audio ani video. |
| 1.2.4 | Captions (Live) | AA | Nevztahuje se | Stránka neobsahuje živé audio ani video. |
| 1.2.5 | Audio Description (Prerecorded) | AA | Nevztahuje se | Stránka neobsahuje předem nahrané audio ani video. |
| 1.3.1 | Info and Relationships | A | Splněno | Obsah používá sémantické prvky `header`, `nav`, `main`, `section`, `article` a `footer`; tabulka má `caption`, `th` a atributy `scope`. |
| 1.3.2 | Meaningful Sequence | A | Splněno | Zdrojové pořadí odpovídá vizuální posloupnosti: záhlaví a navigace, hlavní sekce, patička. |
| 1.3.3 | Sensory Characteristics | A | Splněno | Pokyny a popisy závisí na textu a sémantické struktuře, nikoli pouze na barvě, tvaru nebo poloze. |
| 1.3.4 | Orientation | AA | Splněno | CSS nerozlišuje ani neomezuje orientaci zařízení; rozvržení se přizpůsobuje dostupné šířce. |
| 1.3.5 | Identify Input Purpose | AA | Nevztahuje se | Stránka neobsahuje formuláře ani vstupní pole uživatele. |
| 1.4.1 | Use of Color | A | Splněno | Informace nejsou sdělovány pouze barvou; text, nadpisy, odkazy a tabulkové hlavičky jsou čitelné samostatně. |
| 1.4.2 | Audio Control | A | Nevztahuje se | Stránka automaticky nepřehrává žádné zvukové médium. |
| 1.4.3 | Contrast (Minimum) | AA | Splněno | CSS definuje kontrastní světlou i tmavou paletu pro text, tlumený text, odkazy a pozadí; přepínače poskytují vysoký kontrast. |
| 1.4.4 | Resize Text | AA | Splněno | Text je nastaven relativními jednotkami a layout reaguje na změnu velikosti viewportu i zvětšení textu. |
| 1.4.5 | Images of Text | AA | Splněno | Obrázky jsou fotografie a grafika projektů; text stránky není vykreslen jako soubor obrázku. |
| 1.4.10 | Reflow | AA | Splněno | Při zmenšení šířky se navigace a projektové karty přeorganizují do menšího počtu sloupců, nakonec do jednoho sloupce. |
| 1.4.11 | Non-text Contrast | AA | Splněno | Ohraničení, text a odkazy používají výrazné systémové i vlastní kontrastní barvy ve všech barevných variantách. |
| 1.4.12 | Text Spacing | AA | Splněno | Rozvržení nepoužívá absolutní výšky ani pevná omezení, která by bránila zvětšení řádkování a mezer. |
| 1.4.13 | Content on Hover or Focus | AA | Nevztahuje se | Stránka nezobrazuje další obsah při najetí myší ani při fokusu. |

### 2 Operable (ovladatelnost)

| Kritérium | Název | Úroveň | Stav | Kde a jak / proč ne |
| --- | --- | --- | --- | --- |
| 2.1.1 | Keyboard | A | Splněno | Veškeré dostupné funkce jsou odkazy a jsou ovladatelné klávesnicí: Tab, Shift+Tab a Enter. |
| 2.1.2 | No Keyboard Trap | A | Splněno | Žádný prvek neuvězňuje fokus; po posledním ovládacím prvku lze pokračovat mimo stránku. |
| 2.1.4 | Character Key Shortcuts | A | Nevztahuje se | Stránka nepoužívá zkratky tvořené jedním znakem. |
| 2.2.1 | Timing Adjustable | A | Nevztahuje se | Stránka nemá časový limit ani časově omezenou aktivitu. |
| 2.2.2 | Pause, Stop, Hide | A | Splněno | Stránka nemá automaticky začínající animace, blikání ani měnící se informace. |
| 2.3.1 | Three Flashes or Below Threshold | A | Splněno | Stránka neobsahuje blikající ani třepající se obsah. |
| 2.4.1 | Bypass Blocks | A | Splněno | Odkaz „Přejít na obsah“ umožňuje přeskočit záhlaví a navigaci; cílový `<main>` je díky `tabindex="-1"` programově focusovatelný. |
| 2.4.2 | Page Titled | A | Splněno | Dokument má unikátní, popisný titul „Krystof Maly – osobní stránka“. |
| 2.4.3 | Focus Order | A | Splněno | DOM pořadí odpovídá logické cestě: přeskočit obsah, navigační odkazy, hlavní obsah a e-mailový odkaz. |
| 2.4.4 | Link Purpose (In Context) | A | Splněno | Texty „O mně“, „Projekty“, „Dovednosti“ a „Kontakt“ i e-mail jasně určují účel nebo cílovou akci. |
| 2.4.5 | Multiple Ways | AA | Nevztahuje se | Jedná se o jednostránkový dokument; neexistuje sada podobných webových stránek, v níž by bylo nutné více způsobů navigace. |
| 2.4.6 | Headings and Labels | AA | Splněno | Nadpisy `h1`–`h3` pojmenovávají sekce a projekty; tabulka má popisek a pojmenovaná záhlaví. |
| 2.4.7 | Focus Visible | AA | Splněno | Prvky `a:focus-visible` mají výrazný obrys, posun od okraje a skip-link se při fokusu zobrazí. |
| 2.4.11 | Focus Not Obscured (Minimum) (nové) | AA | Splněno | Stránka nemá sticky ani pevné překryvy; kolem fokusu není prvek, který by ho zakrýval. |
| 2.5.1 | Pointer Gestures | A | Nevztahuje se | Stránka nepoužívá vícedotykové ani složité gesta. |
| 2.5.2 | Pointer Cancellation | A | Splněno | Akce se provádí na odkazech pomocí standardního aktivování po kliknutí nebo stisku; vlastní operace při stisku ukazatele chybí. |
| 2.5.3 | Label in Name | A | Splněno | Viditelné texty navigačních odkazů a e-mailového odkazu jsou použity i jako jejich přístupné názvy. |
| 2.5.4 | Motion Actuation | A | Nevztahuje se | Stránka nepoužívá pohybové senzory ani pohyb zařízení. |
| 2.5.7 | Dragging Movements (nové) | AA | Nevztahuje se | Stránka neobsahuje ovládací prvky ani obsah, který by vyžadoval přetahování. |
| 2.5.8 | Target Size (Minimum) (nové) | AA | Splněno | Navigační a skip odkazy mají cílovou plochu větší než 24 px; e-mailový odkaz je v textovém řádku a má příslušnou výjimku. |

### 3 Understandable (srozumitelnost)

| Kritérium | Název | Úroveň | Stav | Kde a jak / proč ne |
| --- | --- | --- | --- | --- |
| 3.1.1 | Language of Page | A | Splněno | Kořenový element `<html>` má atribut `lang="cs"`, takže jazyk celé stránky je správně určený jako čeština. |
| 3.1.2 | Language of Parts | AA | Splněno | Textové části stránky jsou česky; názvy projektů nebo technická označení nejsou samostatné pasáže v jiném přirozeném jazyce. |
| 3.2.1 | On Focus | A | Splněno | Přesun fokusu na navigační odkaz nebo přeskočovací odkaz nemění kontext ani automaticky neotevírá nové obsahy. |
| 3.2.2 | On Input | A | Nevztahuje se | Stránka neobsahuje formuláře ani vstupní ovládací prvky, u kterých by zadání měnilo kontext. |
| 3.2.3 | Consistent Navigation | AA | Splněno | Navigace je uvedena pouze v jednom pevně pojatém seznamu a její pořadí je na celé stránce konzistentní. |
| 3.2.4 | Consistent Identification | AA | Splněno | Odkazy a nadpisy sekcí mají ustálené, jednoznačné texty; stejné typy prvků se identifikují stejným způsobem. |
| 3.2.6 | Consistent Help (nové) | A | Nevztahuje se | Stránka neposkytuje nápovědu, podporu ani další mechanismy pomoci, které by bylo nutné konzistentně umísťovat. |
| 3.3.1 | Error Identification | A | Nevztahuje se | Na stránce není formulář ani uživatelské zadávání dat, které by mohlo vyvolat identifikovatelnou chybu. |
| 3.3.2 | Labels or Instructions | A | Nevztahuje se | Stránka nemá vstupní pole ani úkony, které by potřebovaly popisky nebo zadávací instrukce. |
| 3.3.3 | Error Suggestion | AA | Nevztahuje se | Stránka neposkytuje vstupy ani ověřování údajů, u kterých by bylo možné navrhnout opravu. |
| 3.3.4 | Error Prevention (Legal, Financial, Data) | AA | Nevztahuje se | Stránka nepřijímá ani neodesílá právní, finanční nebo citlivé uživatelské údaje. |
| 3.3.7 | Redundant Entry (nové) | A | Nevztahuje se | Stránka nemá vícestupňový ani informačně opakovaný proces zadávání. |
| 3.3.8 | Accessible Authentication (Minimum) (nové) | AA | Nevztahuje se | Stránka neobsahuje přihlášení, autentizaci ani kognitivní ověřovací úlohy. |

### 4 Robust (robustnost)

| Kritérium | Název | Úroveň | Stav | Kde a jak / proč ne |
| --- | --- | --- | --- | --- |
| 4.1.2 | Name, Role, Value | A | Splněno | Nativní HTML prvky mají správné názvy, role a hodnoty: odkazy, navigace, záhlaví, sekce, tabulka a její buňky. |
| 4.1.3 | Status Messages | AA | Nevztahuje se | Stránka nezobrazuje dynamická stavová hlášení ani automatické aktualizace obsahu; nejsou zde žádné upozornění nebo procesy potřebující živý region. |
