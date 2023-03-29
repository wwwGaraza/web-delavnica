# Konfiguracija novega strežnika

Ko zakupimo strežnik in izvemo njegov IP naslov, se lahko povežemo nanj.
Za strežnike z operacijskim sistemom Linux za ta namen najpogosteje uporabimo *SSH*.

    ssh root@<naslov>

Če smo nastavili SSH ključ, se lahko na strežnik povežemo brez gesla, v nasprotnem primeru, ga bo pa potrebno vpisati.

Pametno je najprej namestiti posodobitve:

    apt update && apt upgrade
   

## Dodajanje novih uporabnikov

Uporabnika `root` je smiselno uporabljati izključno za prvotno dodajanje novih uporabnikov v sistem.

Pametno se je v sistem prijavljati z nekim drugim uporabniškim imenom in, kadar je potrebno, uporabiti `sudo`.

Novega uporabnika dodamo z naslednjim ukazom:

    useradd <username>


Uporabniku omogočimo prijavo z SSH ključem tako, da na strežniku v datoteko `/home/<username>/.ssh/authorized_keys` skopiramo njegov **javni** ključ (običajno `id_rsa.pub`).

    # Zamenjamo trenutnega userja, da bo .ssh imel pravilnega ownerja.
    sudo -iu <username>
    mkdir .ssh
    nano .ssh/auhtorized_keys
    # Nazaj na root userja
    exit


Če hočemo uporabniku omogočiti uporabo ukaza `sudo`, ga moramo dodati v skupino `sudo` (Ubuntu) ali `wheel` (nekatere druge distribucije).

   usermod <username> -G sudo


## SSH varnost

Potem, ko smo nastavili vsaj enega dodatnega uporabnika, ki ima dostop do `sudo`, lahko v `/etc/ssh/sshd_config` dodamo naslednje nastavitve:

    PermitRootLogin no
    PermitEmptyPasswords no
    PasswordAuthentication no
    UsePAM no

S tem bomo prepovedali prijavo z `root` in prijave z geslom ter tako bistveno izboljšali nivo varnosti strežnika.

Poženemo 

    systemctl reload sshd

*trenutnega okna ne zapiramo* in se v novemu oknu poskusimo povezati na strežnik.

S tem se prepričamo, da je s SSH konfiguracijo vse ok in da se nismo zaklenili iz strežnika.
