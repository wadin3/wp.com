# Wadin Psykologi – projektöversikt

Den här filen är en överlämnings- och kontextfil för fortsatt utveckling av Wadin Psykologis webbplats. Den ska göra det möjligt att starta en ny ChatGPT-tråd, läsa in repot och fortsätta arbetet utan att vara beroende av tidigare chattlogg.

## 1. Projektets syfte

Wadin Psykologi är den kundvända psykologverksamheten inom Wadin Psykologi & Struktur AB.

Webbplatsen ska främst presentera psykologisk utredning, bedömning och urval. Fokus är inte behandling.

Målet med sajten är att:
- inge förtroende och kompetens
- kännas modern, specialistinriktad och tydlig
- göra det enkelt för privatpersoner och organisationer att förstå tjänsterna
- göra det enkelt att ta kontakt

Live-domän: https://wadinpsykologi.com
GitHub-repo: `wadin3/wp.com`
Hosting: GitHub Pages
Domän/DNS: STRATO

## 2. Arbetsmodell

Föredragen arbetsmodell är:

1. Användaren beskriver önskad förändring i ChatGPT.
2. ChatGPT läser vid behov aktuell kod från GitHub.
3. ChatGPT gör ändringen direkt i repot.
4. GitHub Pages bygger om sidan automatiskt.
5. Ändringen kontrolleras på live-sidan.

Undvik onödiga manuella steg för användaren när GitHub-kopplingen kan göra ändringen direkt.

Användaren är inte programmerare och vill ha raka, konkreta instruktioner och så lite teknisk komplexitet som möjligt.

## 3. Varumärke och visuell riktning

Önskad känsla:
- ren
- modern
- professionell
- kompetent
- specialist
- mänsklig men inte terapeutiskt mysig

Undvik:
- klassiska terapeutklichéer
- för mjuk eller sentimental design
- för generisk vårdcentral-känsla
- för akademisk eller tung ton

Nuvarande färgpalett i CSS:
- off-white / varm ljus bakgrund
- graphite / mörkgrå text
- petrol / gråblå huvudaccent
- dämpad rosa som sekundär accent

Aktuella CSS-variabler:
- `--paper:#f5f4ef`
- `--paper2:#fbfaf7`
- `--ink:#303538`
- `--muted:#667073`
- `--petrol:#316a73`
- `--petrol2:#214b53`
- `--petrol3:#173b42`
- `--rose:#b77f8c`
- `--rose2:#efe0e4`

Logotyp:
- fil: `wadin-psykologi-logo.png`
- ska användas i toppmenyn till vänster
- den riktiga PNG-logotypen ska användas, inte en ersatt eller nyritad SVG-version

## 4. Verksamheten

### Privatpersoner

#### Gratis NP-screening
- digitala formulär
- psykologisk genomgång och sammanfattning
- rekommendation om nästa steg
- är inte en diagnos eller full utredning
- pris: 0 kr

#### Neuropsykiatrisk utredning
- barn och vuxna
- ADHD/ADD, autism och intellektuell funktionsnedsättning kan vara aktuella frågeställningar
- bred psykologisk utredning
- specialistläkare/psykiater ansvarar för medicinsk del
- delar kan ske på distans, men testning/läkarbedömning kan kräva fysiskt möte
- pris: 24 500 kr

#### Begåvningsutredning
- kartläggning av kognitiv förmåga och profil
- vid frågeställning om intellektuell funktionsnedsättning räcker inte en fristående begåvningsbedömning ensam
- pris: 11 500 kr

### Organisationer

#### Urval & rekrytering
- stöd vid tidigt urval och Second Opinion
- kognitiva/logiska tester
- personlighetstest
- rollanalys
- strukturerad intervju när det är relevant
- offert vid förfrågan

#### Bedömningsstöd
- främst stöd till privata vårdgivare
- flexibel psykologisk bedömningshjälp
- pris: 1 400 kr/timme
- moms kan tillkomma beroende på uppdrag

#### Hyra psykolog
- tillfällig psykologresurs för utredning/bedömning
- kan gälla klinik, skola, arbetsliv eller rekrytering
- på plats, distans eller hybrid
- pris: 1 400 kr/timme + moms

## 5. Sidstruktur

Nuvarande webbplats är en statisk SPA med hash-routing.

Viktiga filer:
- `index.html` – skal, header, navigation, footer
- `styles.css` – all huvudsaklig styling
- `app.js` – sidinnehåll, routing och komponentliknande markup
- `wadin-psykologi-logo.png` – officiell logotyp

Tjänstesidor bör i regel innehålla:
- Vad är det?
- Hur går det till?
- Vad händer sedan?
- Pris
- kontakt-CTA nära toppen och längst ner

Viktiga routes har tidigare omfattat:
- startsida
- screening
- NP-utredning
- begåvningsutredning
- urval
- bedömningsstöd
- hyra psykolog
- om
- kontakt

Läs alltid aktuell `app.js` innan större ändringar eftersom route-namn och innehåll kan ha ändrats.

## 6. Om Kenny Wadin

Kenny Wadin är legitimerad psykolog.

Relevant bakgrund som kan användas på Om-sidan:
- arbetar som psykolog sedan 2013
- arbetar med neuropsykiatriska utredningar sedan 2019
- har genomfört flera hundra utredningar
- erfarenhet från vård, skola, arbetsliv och rekrytering
- uppdrag/erfarenhet från bland annat Bonliva Care, Coperio, SMART Psykiatri och WeMind
- pågående specialistutbildning inom arbets- och organisationspsykologi
- konsult för Assessio
- erfarenhet av Second Opinion och psykometrisk testning
- certifieringar: MAP, Matrigma, MAP-X och Match-V

Verksamheten är baserad i området Alingsås, Borås och Göteborg och har ingen fast mottagning som måste dominera kommunikationen. Flexibilitet i plats och distansarbete är en styrka.

Wadin Struktur kan ge administrativt stöd internt, men Wadin Psykologi ska uppfattas som en tydlig egen kundvänd verksamhet.

## 7. Ton och copy

Språket ska vara:
- tydligt
- professionellt
- konkret
- varmt utan att bli mjukt eller fluffigt
- lätt att förstå även för personer utan psykologisk fackkunskap

Undvik överdrivet akademiskt språk, vårdbyråkrati och typisk AI-copy.

Det ska framgå att Wadin Psykologi är specialistinriktat på utredning och bedömning snarare än behandling.

## 8. Teknisk drift

Sajten publiceras via GitHub Pages från huvudbranchen.

Custom domain:
- `wadinpsykologi.com`

Även `www.wadinpsykologi.com` pekar till sajten via CNAME.

HTTPS är aktiverat via GitHub Pages.

När kod ändras på `main` ska GitHub Pages normalt publicera ändringen automatiskt efter en kort stund.

## 9. Viktiga arbetsregler för fortsatt utveckling

- Läs aktuell kod innan större ingrepp.
- Bevara fungerande delar om inte användaren uttryckligen vill ändra dem.
- Gör hellre små, tydliga commits än stora osäkra omskrivningar.
- Använd den befintliga designidentiteten som utgångspunkt.
- Byt inte ut officiella bildfiler eller logotyper mot genererade eller rekonstruerade varianter.
- Om en ändring kan göras direkt via GitHub-kopplingen: gör den hellre än att instruera användaren att redigera kod manuellt.
- Efter ändring: berätta kort vad som ändrades och att GitHub Pages kan behöva någon minut för att uppdateras.

## 10. Underhåll av denna fil

När större beslut fattas om varumärke, tjänster, struktur, priser, teknik eller arbetsmodell bör `PROJECT.md` uppdateras så att den fortsätter vara användbar som överlämningsfil.

I en ny ChatGPT-tråd kan användaren med fördel skriva:

> Läs `PROJECT.md` och den aktuella koden i GitHub-repot `wadin3/wp.com`. Fortsätt utveckla Wadin Psykologis hemsida utifrån det som står där.
