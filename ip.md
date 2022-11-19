# TCP/IP
TCP/IP protokol je eden od gradnikov sodobnega interneta.

Praktično vsak računalnik, ki je povezan v internet, ima svoj IP naslov (ali več njih).

Najprej je obstajal IPv4, ki ga zapišemo s 4 števili od 0 do 255, ločenimi s pikami. Primer: `193.2.1.67`.

Nekateri naslovi so rezervirani za interno rabo v manjših, izoliranih omrežjih, kakor je omrežje pri vas doma ali v kakšni ustanovi, podjetju. Eden od teh razponov naslovov je npr. `192.168.0.0 – 192.168.255.255`.

Prostih IPv4 naslovov, zaradi naraščajočega števila ljudi z dostopom do interneta in hitre digitalizacije družbe, že dalj časa primanjkuje.

Zato se počasi uveljavlja IPv6, ki ima bistveno več prostih naslovov (~ 3.4×10^38). IPv6 naslov pa je sestavljen iz osmih
4-mestnih šestnajstiških števil (števke 0-9 in a-f). Primer: `2606:2800:220:1:248:1893:25c8:1946`.

Svoj IP naslov lahko dobiš z ukazom `ipconfig` (Windows) in `ifconfig` ali `ip addr` (Linux).

V domačem omrežju ti ta ukaz vrne _interni_ IP naslov, svoj _javni_ IP pa lahko vidiš npr. če v Google vtipkaš `what's my ip address`.
