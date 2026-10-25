# Bygga profilen i PowerPoint

Allt i profilen går att bygga med PowerPoints egna verktyg. En färdig mall (.potx) kommer i nästa version.

## Bakgrund, mörkt läge
**Formatera bakgrund → Toningsfyllning → Radiell**, med centrum uppe till höger.

| Palett | Stopp 0 % | 30 % | 70 % | 100 % |
|---|---|---|---|---|
| Grön skog | #1E7A55 | #14523C | #0A1F18 | #06140F |
| Svart och vit | #5A5A5A | #2A2A2A | #111111 | #060606 |
| Mörkblå | #3B78D8 | #1A3D7A | #07102A | #040A1A |

För mörkblått: lägg bakgrunden som en linjär toning (#0B1834 → #040A1A) och en mindre radiell glöd som en egen form i hörnet, med 100 % genomskinlighet i ytterkanten.

## Bakgrund, ljust läge
En vit bakgrund med en radiell toning nere till höger: #D9DDDA → #F3F5F3 → #FFFFFF. För svart och vit och mörkblått används en neutral grå i stället.

## Gradienttext
Markera texten och välj **Formatera form → Textfyllning → Toningsfyllning**, linjär 135°, med de tre stoppen i `accentGradient` (se `tokens/tokens.json`). Lägg till en **yttre skugga**: svart, 15 % opacitet, oskärpa 1 pt, avstånd 1 pt.

## Glaskort
1. Skapa en rundad rektangel.
2. **Fyllning:** solid #B0B4B2 med 78 % genomskinlighet.
3. **Linje:** vit, 0,5 pt, 25 % genomskinlighet.
4. **Skugga:** yttre, svart, 7 % opacitet, oskärpa 14 pt, avstånd 6 pt nedåt.
5. **Glansreflex (bara hjältekortet):** lägg en parallellogram över kortet med en vit toning som går från 100 % till 70 % och tillbaka till 100 % genomskinlighet, och beskär den till kortets form.

PowerPoint saknar riktig bakgrundsoskärpa. Känslan av glas kommer från den halvgenomskinliga fyllningen, den ljusa kanten och skuggan.

## Brobågen
Rita en båge med **Infoga → Former → Båge** eller en frihandskurva. Använd 1,5 pt linje i accentfärgen med 40–60 % genomskinlighet, plus en tunnare kopia förskjuten nedåt med 75 % genomskinlighet.

## Animering (planerad)
| Element | Effekt |
|---|---|
| Brobågen | **Torka** från vänster, 1,2 s |
| Stor siffra | **Tona in** och **Växa** 90 → 100 %, 0,6 s |
| Staplar | **Torka** nedifrån, en efter en med 0,15 s fördröjning |
| Glaskort | **Tona in** och **Flyga in** 20 px uppifrån, i sekvens |
| Mellan slides | **Morph**, så att framstegslinjen växer mjukt |
