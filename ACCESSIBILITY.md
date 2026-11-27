# Zpráva o přístupnosti

Příklady řádků nahraďte vlastními výsledky. Zapište alespoň tři skutečné nálezy
a u každého hash commitu, který ho opravil (najdete ho v `git log --oneline`).

## Výsledky nástrojů

| Nástroj | Před opravami | Po opravách |
| --- | --- | --- |
| Lighthouse (Accessibility) | 75/100/100/91 | 100/100/100/91 |
| WAVE (Errors a Contrast Errors) | 10/10 | 10/10 |
| Test klávesnicí | TODO | TODO |

## Nalezené problémy a jejich opravy

| Problém | Jak jsem ho našel | Oprava (commit) | Kritérium WCAG |
| --- | --- | --- | --- |
| Například: odkaz „Více“ bez popisu | WAVE | `a1b2c3d` | 2.4.4 |
| format obrazku | Lighthouse | 'f06d270' | 1.4.5 |
| rozliseni obrazku | Lighthouse | 'f06d270' | 1.4.5 |

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
| 1.1.1 | Non-text Content | A | TODO | TODO |
| 1.2.1 | Audio-only and Video-only (Prerecorded) | A | TODO | TODO |
| 1.2.2 | Captions (Prerecorded) | A | TODO | TODO |
| 1.2.3 | Audio Description or Media Alternative (Prerecorded) | A | TODO | TODO |
| 1.2.4 | Captions (Live) | AA | TODO | TODO |
| 1.2.5 | Audio Description (Prerecorded) | AA | TODO | TODO |
| 1.3.1 | Info and Relationships | A | TODO | TODO |
| 1.3.2 | Meaningful Sequence | A | TODO | TODO |
| 1.3.3 | Sensory Characteristics | A | TODO | TODO |
| 1.3.4 | Orientation | AA | TODO | TODO |
| 1.3.5 | Identify Input Purpose | AA | TODO | TODO |
| 1.4.1 | Use of Color | A | TODO | TODO |
| 1.4.2 | Audio Control | A | TODO | TODO |
| 1.4.3 | Contrast (Minimum) | AA | TODO | TODO |
| 1.4.4 | Resize Text | AA | TODO | TODO |
| 1.4.5 | Images of Text | AA | TODO | TODO |
| 1.4.10 | Reflow | AA | TODO | TODO |
| 1.4.11 | Non-text Contrast | AA | TODO | TODO |
| 1.4.12 | Text Spacing | AA | TODO | TODO |
| 1.4.13 | Content on Hover or Focus | AA | TODO | TODO |

### 2 Operable (ovladatelnost)

| Kritérium | Název | Úroveň | Stav | Kde a jak / proč ne |
| --- | --- | --- | --- | --- |
| 2.1.1 | Keyboard | A | TODO | TODO |
| 2.1.2 | No Keyboard Trap | A | TODO | TODO |
| 2.1.4 | Character Key Shortcuts | A | TODO | TODO |
| 2.2.1 | Timing Adjustable | A | TODO | TODO |
| 2.2.2 | Pause, Stop, Hide | A | TODO | TODO |
| 2.3.1 | Three Flashes or Below Threshold | A | TODO | TODO |
| 2.4.1 | Bypass Blocks | A | TODO | TODO |
| 2.4.2 | Page Titled | A | TODO | TODO |
| 2.4.3 | Focus Order | A | TODO | TODO |
| 2.4.4 | Link Purpose (In Context) | A | TODO | TODO |
| 2.4.5 | Multiple Ways | AA | TODO | TODO |
| 2.4.6 | Headings and Labels | AA | TODO | TODO |
| 2.4.7 | Focus Visible | AA | TODO | TODO |
| 2.4.11 | Focus Not Obscured (Minimum) (nové) | AA | TODO | TODO |
| 2.5.1 | Pointer Gestures | A | TODO | TODO |
| 2.5.2 | Pointer Cancellation | A | TODO | TODO |
| 2.5.3 | Label in Name | A | TODO | TODO |
| 2.5.4 | Motion Actuation | A | TODO | TODO |
| 2.5.7 | Dragging Movements (nové) | AA | TODO | TODO |
| 2.5.8 | Target Size (Minimum) (nové) | AA | TODO | TODO |

### 3 Understandable (srozumitelnost)

| Kritérium | Název | Úroveň | Stav | Kde a jak / proč ne |
| --- | --- | --- | --- | --- |
| 3.1.1 | Language of Page | A | TODO | TODO |
| 3.1.2 | Language of Parts | AA | TODO | TODO |
| 3.2.1 | On Focus | A | TODO | TODO |
| 3.2.2 | On Input | A | TODO | TODO |
| 3.2.3 | Consistent Navigation | AA | TODO | TODO |
| 3.2.4 | Consistent Identification | AA | TODO | TODO |
| 3.2.6 | Consistent Help (nové) | A | TODO | TODO |
| 3.3.1 | Error Identification | A | TODO | TODO |
| 3.3.2 | Labels or Instructions | A | TODO | TODO |
| 3.3.3 | Error Suggestion | AA | TODO | TODO |
| 3.3.4 | Error Prevention (Legal, Financial, Data) | AA | TODO | TODO |
| 3.3.7 | Redundant Entry (nové) | A | TODO | TODO |
| 3.3.8 | Accessible Authentication (Minimum) (nové) | AA | TODO | TODO |

### 4 Robust (robustnost)

| Kritérium | Název | Úroveň | Stav | Kde a jak / proč ne |
| --- | --- | --- | --- | --- |
| 4.1.2 | Name, Role, Value | A | TODO | TODO |
| 4.1.3 | Status Messages | AA | TODO | TODO |
