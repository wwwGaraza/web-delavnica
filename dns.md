# DNS
Ker so IP naslovi nekoliko nepregledni in si jih je težko
zapomniti, so izumili DNS (Domain Name System). DNS je sistem, ki pretvarja med domenami in IP naslovi.
Z njim tvoj računalnik `www.arnes.si` pretvori v `193.2.1.67`.

## Registracija domene

Z različnimi krovnimi domenami (`.com`, `.net`, `.si` ...) upravljajo različne organizacije.
S `.com` recimo podjetje Verisign, s `.si` pa Arnes.
Domeno v sistemu DNS lahko registrira vsak.
Registracijo se izpelje preko _registrarja_, ki mu je potrebno plačati letno uporabnino.

Kdor zakupi svojo domeno, lahko prosto razpolaga z njo in njenimi _poddomenami_. `blog.mojadomena.si` bi tako lahko usmeril na en IP naslov, `www.mojadomena.si` pa na drugega.

## Tipi zapisov

DNS je sestavljen iz različnih tipov zapisov. Za nas bosta najpomembnejša CNAME in A ali AAAA. CNAME uporabimo, če eno hočemo eno izmed poddomen usmeriti na neko drugo domeno. A in AAAA pa uporabimo, če želimo domeno usmeriti na nek IPv4 (A) ali IPv6 (AAAA) naslov.

Poleg tega poznamo še veliko [drugih tipov DNS zapisov](https://en.wikipedia.org/wiki/List_of_DNS_record_types) vendar za nas niso tako pomembni.

## Uporabni ukazi

Če hočeš preveriti, na kateri IP naslov neka domena kaže, lahko uporabiš `nslookup www.rtvslo.si` (Windows) ali `dig www.rtvslo.si` (Linux).

## Vaja

Poišči IP naslov za stran `amazon.com` in `google.com`.
Vidiš kakšno zanimivo razliko med obema odgovoroma?
