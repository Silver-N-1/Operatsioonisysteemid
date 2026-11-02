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


_Ül 7.4_


<img width="499" height="563" alt="OS_7 4" src="https://github.com/user-attachments/assets/51cd65f4-a1bc-4434-891c-74478b5d3f64" />


_Ül 7.5_

1) -o ro (read-only): Haagib mälupulga ainult lugemiseks. Mälupulgal olevaid faile saab avada ja vaadata, kuid sinna ei saa uusi faile salvestada, olemasolevaid muuta ega kustutada.

2) -t auto (type auto): Annab süsteemile korralduse mälupulga failisüsteemi tüüp (nt FAT32, NTFS, ext4) automaatselt tuvastada, nii et kasutaja ei pea seda käsitsi määrama.

_Ül 7.6_

Ubuntu asendas auto parameetri väärtusega vfat.

_Üll 7.7_


<img width="506" height="560" alt="OS_7 7" src="https://github.com/user-attachments/assets/5d4b5e6f-8e3b-4de3-aa40-337bcd7571b9" />


