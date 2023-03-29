# HTTP
`HTTP` je protokol, s katerim brskalnik od strežnika zahteva nek dokument.
Najpogosteje se z njim prenašajo HTML spletne strani z vsemi pritiklinami (slike, fonti, Javascript).

```
GET /index.html HTTP/1.1
Accept: text/html
Host: example.com
```


## Glagoli
Glagol oz. `HTTP verb` serverju pove, katero akcijo bi client rad izpeljal nad nekim resourcom.

Najpomembnejši glagoli so

GET - branje
POST - dodajanje novega recorda
PUT - dodajanje novega recorda z določenim ključem
DELETE - brisanje recorda
PATCH - spreminjanje obstoječega recorda

Primer:

GET /users/ bi vrnil seznam uporabnikov.
POST /users/ bi dodal novega uporabnika
GET /users/janez bi vrnil janezove podatke
DELETE /users/janez bi izbrisal tega uporabnika

## Headerji
S headerji tako server, kot tudi client, nastavljata metapodatke, kot so npr. format podatkov, cookieji, jezik strani, tokeni za avtentikacijo zahtevkov, pa še mnogo več.

## Vaje
Poskusi z ukazom `telnet DOMENA PORT` od poljubnega strežnika zahtevati neko datoteko.

