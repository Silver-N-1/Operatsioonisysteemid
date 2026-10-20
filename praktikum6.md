# Praktikum 6
Selles praktikumis õppisime pääsuõigustest, määrasime failide ning kataloogide õigusi ja muutisime omanikke. Lisaks lõime uusi gruppe ning kasutajaid. Üldjoontes sain enda arust praktikumiga hästi hakkama.

_6.1_
<br> a)
Kaustale /tmp/kaust on vaja ainult sisenemisõigust (x), sest siis pääseb kausta sisse ning õigust (r) pole vaja, kuna me teame faili nime. Failile minufail.txt on vaja ainult lugemisõigust (r), sest siis on võimalik faili sisu lugeda.
b) Kataloogil /tmp/kaust on vaja õigusi (w, x), sest on vaja kausta sisse pääseda (x) ja failide muutmiseks kausta sees on vaja kirjutamis (w) õigust. Failile minufail.exe ei vaja ühtegi õigust, kui tahta seda kustutada, sest kui kataloogis, kus see fail sees on sul õigus kirjutada (w), siis saab selle faili ära kustutada.


_6.2_

Kui anda ette (Kaust3/skript.sh), siis linux loeb skript.sh faili kui tekstifailina ning ei piisa, et sellel on ainult käivitamise õigus (x), vaid see vajab ka lugemisõigust lisaks. Aga kui anda ette (sh Kaust3/skript.sh), siis isegi pole (x) õigust vaja, vaid piisab ka (r) õigussest

_6.3_

UPG-ga on võimalik luua keskkond, kus kasutajad saavad jagada faile/kaustasid, ilma enda isiklike failide turvalisust ohverdamata. Ilma UPG-ta oleksid kasutajad ühes grupis (users). Selleks, et teised kasutajad sinu faile muuta ei saaks, peaks umask olema range 022 (grupil puudub kirjutamisõigus). UPG süsteemis on umaskiks vaikimisi 002 (grupil on kirjutamisõigus). Kuna uue faili omanikgrupiks on kasutaja omanimeline privaatgrupp, milles on liikumis õigus (x) ainult temal endal, ei pääse teised kasutajad faile muutma.

_6.4_

<img width="641" height="457" alt="OS_6 4" src="https://github.com/user-attachments/assets/460fa7cc-102d-4e54-bbd0-02e938af548d" />

_6.5_

<img width="642" height="454" alt="OS_6 5" src="https://github.com/user-attachments/assets/d892939c-4a4d-4e5c-ae85-e49cd4da347d" />

Setuid õigust on vaja selleks, et tavakasutaja saaks käivitada teatud programmi selle programmi omaniku õigustega, mitte enda tavaliste õigustega.

_6.6_

Setuid kasutamine nii tõstab, aga samas ka vähendab turvalisust. 
Näiteks (+): Lubab setuid tavakasutajal teha tegevust, mis nõuab kõrgemaid õigusi, andmata talle neid õigusi jäädavalt või liiga laialdaselt. 
Näiteks (-): Suurim probleem setuid'l on õiguste Privilege Escalation. Kui setuid-õigusega fail kuulub root kasutajale, on see ründajate jaoks kõige parem sihtmärk.

_6.7_

Kasutaja peeter faili saab kustutada: peeter (faili omanik), opetaja (kataloogi omanik) ja root (absoluutne võim)

_6.8_

Märkan, et õiguste lõpus on lisatud + (-rw-rw----+)

# file: home/opetaja/klass/hinded.txt
# owner: opetaja
# group: opetaja
user::rw-
group::---
group:direktor:rw-
mask::rw-
other::---

_6.9_

Mitte keegi ei saa faili (+i) sisu muuta (isegi root). Seda saab kustutada, kui teha: 
1) sudo chattr -i testfail-2
2) rm testfail-2
  
