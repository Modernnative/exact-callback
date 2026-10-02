# Terugkeerpagina voor de Exact Online koppeling

Een statische pagina, een taak. Exact Online eist bij het registreren van een app een
**redirect URL** over HTTPS, en stuurt je browser daarheen zodra je de koppeling hebt
goedgekeurd. In dat adres zet Exact de autorisatiecode. Deze pagina leest die code uit de
adresbalk en toont hem met een kopieerknop, zodat je hem in het koppelscript kunt plakken.

Het adres dat in Exact Online geregistreerd moet staan:

```
https://modernnative.github.io/exact-callback/
```

Letterlijk zo, inclusief de slash op het eind. Wijkt het af, dan weigert Exact de koppeling.

## Wat hier niet gebeurt

Geen server, geen opslag, geen verzending. De code staat alleen in de adresbalk van de
browser van degene die de koppeling goedkeurt, en wordt met JavaScript in de pagina
getoond. Er gaat niets naar GitHub en niets naar een derde partij. De code is bovendien
een paar minuten geldig en eenmalig inwisselbaar.

## Hoort bij

`Administratie/exact_koppel.py` in de operations-repo, dat de code omwisselt voor een
access token en een refresh token.
