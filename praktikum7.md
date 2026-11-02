# Praktikum 7

_Ül 7.1_

Uued andmekandjad võivad tehasest tulles olla ilma loogilise struktuurita, mistõttu operatsioonisüsteem ei tea veel, kuidas kettale andmeid paigutada. Ketta lähtestamise käigus luuakse partitsioonitabel (MBR või GPT), mis kirjeldab ketta partitsioonide paigutust ja piire. Seejärel saab kettale luua partitsioone ning need sobiva failisüsteemiga (nt NTFS või ext4) vormindada, et operatsioonisüsteem saaks sinna andmeid salvestada ja lugeda.

_Ül 7.2_

1) MBR kasutab 32-bitist LBA-d (Logical Block Addressing), mis võimaldab adresseerida kuni 2,2 TB andmeruumi (2³² * 512 baiti). GPT kasutab 64-bitist adresseerimist, võimaldades teoreetiliselt kuni 9,4 zettabaidi (ZB) suurustele andmekandjatele.
2) MBR Toetab ainult 4 põhipartitsiooni.  GPT aga 128 põhipartitsiooni.
3) MBR partitsiooniandmed on salvestatud 64 baidi ulatuses, kusjuures iga partitsioonikirje võtab enda alla 16 baiti. GPT-l iga partitsioonikirje võtab enda alla 128 baiti
4) GPT salvestab kettatabelist varukoopia ketta lõppu. Andmete tervikluse kontrollimiseks kasutab GPT CRC32 kontrollsummasid, mis võimaldab andmete riknemise korral need taastada.

_Ül 7.3_
https://kodu.ut.ee/~silvernogols/opsys/hdd.png
