# Munt-bespaarcheck

Standalone, toegankelijke hypotheek-bespaarcheck (4 stappen) in Hypotheekbond-huisstijl.

- Eén bestand: `index.html` — geen externe API's, geen build-step, geen afhankelijkheden.
- Volledig met het toetsenbord te bedienen: aanbieder-tegels zijn native `<button>`s met
  roving tabindex en pijltjestoetsnavigatie, zichtbare focusindicator, `aria-pressed` status.
- WCAG 2.1 AA-contrast in zowel lichte als donkere modus.
- Nederlandse getal-/valutanotatie (`Intl.NumberFormat('nl-NL')`).
- Geen `localStorage`; alle invoer leeft alleen in het geheugen van de sessie.
- De berekening in stap 4 is **indicatief** (vaste markrente-tabel, vereenvoudigde
  boeterente-schatting) en expliciet gemarkeerd als geen Wft-advies.

## Openen

Open `index.html` direct in de browser, of host het bestand statisch (GitHub Pages,
Google Sites embed, etc.).

## Bekende verbeteringen t.o.v. de originele tool

De live tool op `munt-bespaarcheck.hypotheekbond.nl` had volgens een toegankelijkheids-
audit de volgende knelpunten, die in deze versie zijn opgelost:

- Stap 1 was niet bruikbaar met het toetsenbord (aanbieders niet selecteerbaar,
  geen doorgang naar stap 2).
- Onvoldoende contrast in donkere modus (faalde WCAG AA).

In deze versie zijn tegels, formuliervelden en knoppen allemaal met toetsenbord en
schermlezer te bedienen, met live aankondigingen (`aria-live`) bij stapwisselingen en
resultaten.
