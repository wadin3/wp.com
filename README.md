# Wadin Psykologi

Webbplatsen är byggd som en liten statisk webbapp för att vara enkel att underhålla och publicera.

## Filer
- `index.html` – sidans skal, toppmeny, logotyp och footer
- `styles.css` – all design, färger, typografi, layout och responsivitet
- `app.js` – allt sidinnehåll, tjänster, priser, profilbild och navigering

## Redigering
Tjänstetexterna ligger samlade högst upp i `app.js` i objektet `services`. Det gör att pris, rubrik eller text för en tjänst kan ändras på ett ställe utan att samma information behöver upprepas på flera undersidor.

Sidan använder hash-baserade adresser, till exempel `#/np`, `#/urval` och `#/om`. Det gör att den fungerar på enkel statisk hosting utan serverkonfiguration.
