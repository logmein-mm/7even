# 7EVEN Inruilcalculator

Mobiele inruilcalculator voor de sales van de 7EVEN-winkel (later ook voor klanten).
Een verkoper taxeert de oude e-step en ziet direct het inruilvoorstel op de **7EVEN 1st Edition (€799 incl. btw, excl. leges)**.

## Gebruik
Open `index.html` in een browser. Het is één losse pagina zonder installatie, gemaakt voor de telefoon (responsive) en in de 7EVEN-huisstijl.

## Velden
- Merk (67 merken, aangevuld met merken die op Marktplaats voorkomen), type (optioneel), single of dual engine
- Vermogen motoren totaal in watt, met controle op foute invoer (bijv. Kaabo King GT: 2× 1.100 W = 2.200 W)
- Leeftijd in jaren en maanden, kilometerstand
- Rijdt / rijdt niet, staat ten opzichte van nieuw, onderhoud (met/zonder bonnen), adapter aanwezig, aankoopbewijs aanwezig
- Automatische marktvergelijking NL per model (tweedehands, refurbished, nieuw) uit `markt.json`; het inruilbod wordt daaraan getoetst

## Voorstel
Verkoop + leges = totale verkoopprijs (VKP) − inruil = bij te betalen

## Rekenregels (standaard)
- Basiswaarde op basis van vermogen (350 W ±€550 … 2.000 W ±€1.360 … 5.000 W ±€2.470); zonder vermogen €550 single / €1.100 dual (7EVEN €799, Selana €1.900, StapStep €630)
- Afschrijving 25% in jaar 1, daarna 18% per jaar
- Inruilwaarde = 70% van de marktwaarde, minimaal €100, geen maximum (klant ontvangt het verschil als de inruil hoger is)
- Alle bedragen incl. btw

De waarden zijn aan te passen onder het tandwieltje (alleen bewaard op dat toestel).
De volledige onderbouwing met Nederlandse bronnen staat in de bijlage onderaan de pagina.

## Marktdata
`markt.json` bevat de Nederlandse marktreferenties per merk/model (incl. btw) met peildatum en bronnen. De pagina laadt dit bestand bij het openen; als het ontbreekt, gebruikt ze de ingebouwde set.
