# Kafé Hörnet – designöverlämning

Det här är en överlämning från en designer till dig som utvecklare. Precis som du gjorde designdokument i Interaktionsdesign får du nu ett att bygga ifrån. Allt du behöver finns här: bilder på hur sidorna ska se ut, texterna, designens färger och typsnitt, och en lista på vad som ska hända när man klickar.

Du bygger tre sidor:

| Sida | Fil | Vad den gör |
|---|---|---|
| Start | `index.html` | välkomnar, visar veckans favoriter och öppettider |
| Meny | `menu.html` | listar kaffe, bakat och lunch med priser |
| Boka bord | `booking.html` | ett formulär som kontrollerar att allt är ifyllt innan det "skickas" |

Mockuperna finns i `design/` i två versioner per sida: dator (1280 px bred) och mobil (390 px bred). Texterna finns i `Texter – Kafé Hörnet.md`. Placeholderbilder finns i `images/`: kopiera mappen som den är till din projektmapp. Byt gärna till riktiga foton (se Bilder nedan).

## Delar som finns på alla sidor

**Sidhuvud (header).** Logotypen är bara text, "Kafé Hörnet", till vänster. Till höger en navigering med tre länkar: Start, Meny, Boka bord. Länken till sidan man är på är understruken. På mobil ersätts länkarna av en knapp med texten "Meny ☰" som visar och döljer länkarna när man klickar (JavaScript).

**Sidfot (footer).** Tre kolumner på dator, staplade på mobil: Hitta hit (adress), Öppettider, Kontakt (e-post och telefon). Längst ner en rad med "© Kafé Hörnet 2026".

## Start

1. **Hero.** Stor bild till höger, text till vänster: rubrik "Fika som på farmors tid", en kort ingress och en knapp "Boka bord" som leder till `booking.html`. På mobil ligger bilden under texten.
2. **Veckans favoriter.** Rubrik och tre kort bredvid varandra (staplade på mobil). Varje kort har bild, rubrik, en mening och pris.
3. **Öppet just nu.** En ljus ruta med öppettiderna och adressen, samt en länk "Se hela menyn".

## Meny

1. **Intro.** Rubrik "Meny" och en mening om att allt bakas på plats.
2. **Tre avdelningar:** Kaffe, Bakat, Lunch. Varje avdelning är en rubrik följd av en lista. Varje rad i listan har namnet till vänster, priset till höger, och under namnet en kort beskrivning i mindre, gråare text. Veganska rätter har en liten grön etikett "vegansk" efter namnet.
3. **Svart påbyggnad (frivillig):** knappar "Alla / Kaffe / Bakat / Lunch" ovanför listan som filtrerar vad som visas.

## Boka bord

1. **Intro.** Rubrik "Boka bord" och en mening om att bokningar bekräftas via e-post.
2. **Formuläret.** Fält i den här ordningen, alla med en synlig etikett (label):
   - Namn (text, obligatoriskt)
   - E-post (e-post, obligatoriskt)
   - Datum (datum, obligatoriskt)
   - Tid (lista: 09:00, 10:00, 11:00, 12:00, 13:00, 14:00, 15:00, 16:00)
   - Antal personer (siffra 1–8, obligatoriskt)
   - Meddelande (större textruta, frivilligt)
   - Knapp "Skicka bokning"
3. **Så ska det fungera (JavaScript).** När man klickar på knappen kontrolleras fälten. Tomma obligatoriska fält får en röd ram och ett rött felmeddelande under sig, t.ex. "Fyll i ditt namn". Om allt är ifyllt döljs formuläret och en grön ruta visas: "Tack Anna! Vi har tagit emot din bokning för 4 personer den 2026-12-05 kl 12:00. Du får en bekräftelse på anna@example.com." Namn, antal, datum, tid och e-post hämtas från det som fyllts i.
4. **Bredvid formuläret** på dator (under på mobil): en ruta "Bra att veta" med tre punkter.

## Design

| | |
|---|---|
| Bakgrund | `#FBF7F2` (varm vit) |
| Text | `#2B2118` (mörkbrun) |
| Accent (knappar, länkar, priser) | `#B5502B` (terrakotta) |
| Accent mörk (hover) | `#8F3E20` |
| Grön (etiketter, bekräftelse) | `#5E7F5A` |
| Ljus ruta | `#F1E8DC` |
| Kort | vit med 1 px ram `#E6DCCF`, hörnradie 12 px |
| Fel | `#C0392B` |
| Rubriker | Georgia, serif |
| Brödtext | system-ui / Helvetica / Arial, 18 px, radavstånd 1,6 |
| Max innehållsbredd | 1100 px, centrerad, 24 px marginal i sidled |
| Knapp | accentfärg, vit text, 12 px / 24 px padding, hörnradie 8 px |
| Brytpunkt mobil | under 700 px |

Mått i mockuperna är riktmärken, inte exakta krav. Det viktiga är att sidan ser ut *ungefär* som bilden, fungerar på mobil och att koden validerar.

## Bilder

Placeholderbilderna i `images/` har rätt proportioner och fungerar att bygga med. Vill du ha riktiga foton: sök på Unsplash (fria att använda) efter "latte", "cinnamon bun", "cafe interior" och spara dem med samma filnamn.

| Fil | Används | Proportion |
|---|---|---|
| `hero.svg` | Start, hero | 4:3 |
| `cinnamon-bun.svg` | Start, kort 1 | 3:2 |
| `latte.svg` | Start, kort 2 | 3:2 |
| `soup.svg` | Start, kort 3 | 3:2 |

## Så hänger designen ihop med kursen

| Du bygger | Vecka | Det använder |
|---|---|---|
| alla tre sidornas HTML, formuläret | 47 | semantiska element, listor, länkar, formulär med label |
| färger, typsnitt, kort, knappar | 48 (tis) | selektorer, box model, färg, typografi |
| sidhuvud, kort i rad, sidfotens kolumner, mobilversion | 48 (tors) | flexbox, media queries |
| mobilmenyn | 49 (tis) | DOM, events |
| formulärkontrollen och bekräftelsen | 49 (tors) | villkor, formulärvalidering |

Det som står under "Svart påbyggnad" är frivilligt och ger inget extra betyg. Det finns för att det är roligt.
