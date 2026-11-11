# Praktikum 9

Selles prakrikumis õppisin kasutama ja haldama keskkonnamuutujaid ning aliaseid Linuxis/Windowsis Õpin haldama taustateenuseid (daemoneid) ning eemaldasin mittevajalikku tarkvara ja rakendusepakette (apt, AppX).
Lõpuks uuendasin Ubuntu virtuaalmasina uusimale versioonile Ubuntu 26.10.



## Ül 9.1

PWD=/ , kuna käsu "sudo su" ja "env" andmise ajal olin juba juurkaustas, siis oli see mul väljundiks. 

## Ül 9.2

<img width="491" height="563" alt="9 2" src="https://github.com/user-attachments/assets/859ac7a5-2511-4629-8028-17903074de39" />


## Ül 9.3

Valisin "gamemode" tarkvara. See on Linuxile mõeldud daemonist ja teegist koosnev lahendus, mis võimaldab mängudel taotleda teatud optimeeringute ajutist rakendamist host-operatsioonisüsteemis.
Kuna virtuaalmasinas pole vaja mänge optimiseerida, siis seda daemoni pole vaja ning selle eemaldamine ei lõhu Linuxi süsteemi.
Kokku vabastatud maht: 319,1 MB


<img width="643" height="459" alt="9 3 1" src="https://github.com/user-attachments/assets/fe45e711-b49e-4776-bef6-a5415b638357" />


<img width="643" height="463" alt="9 3 2" src="https://github.com/user-attachments/assets/f9cb4796-d2d1-4bbd-ab16-01c6a31fe2eb" />


<img width="641" height="462" alt="9 3 3" src="https://github.com/user-attachments/assets/4753ff29-71ec-46c9-b269-71c9b2def496" />


<img width="641" height="464" alt="9 3 4" src="https://github.com/user-attachments/assets/838eac05-29ef-48f5-8909-52838016f955" />


<img width="643" height="463" alt="9 3 5" src="https://github.com/user-attachments/assets/0de557ee-c549-4ef0-b2e0-38676ff59377" />


## Ül 9.4

<img width="641" height="425" alt="9 4" src="https://github.com/user-attachments/assets/b3160bb1-f335-4066-ae30-ab48e915ea2f" />


## Ül 9.5 

Käivitatakse Süsteemi %Path% kataloogis asuv fail. Kuna süsteemi %PATH% kataloogid asuvad sõnes eespool, leitakse ja käivitatakse seal asuv .exe fail enne, kui otsing jõuab kasutaja %PATH% kataloogideni.

## Ül 9.6

Valisin Netlogon
Otstarve: Domeenis olevate kasutajate ja seadmete valideerimiseks või autentimiseks. Seda kasutatakse kasutaja identiteedi kinnitamiseks võrgus, millele kasutaja püüab ligi pääseda. 
See on minu arvutis vajalik (kasutan kooli antud sülearvutit), kuna login sisse kooli meilikontoga, ehk seade on liidetud kooli kesksesse domeeni. Ei tohi panna oleku diabled.

## Ül 9.7

PS C:\WINDOWS\system32> Get-AppxPackage -Name "Microsoft.YourPhone" | select packageFullName

PackageFullName
---------------
Microsoft.YourPhone_0.26092.119.0_x64__8wekyb3d8bbwe


PS C:\WINDOWS\system32> Remove-AppxPackage -Package Microsoft.YourPhone_0.26092.119.0_x64__8wekyb3d8bbwe
PS C:\WINDOWS\system32> Get-AppxPackage -Name "Microsoft.YourPhone" | select packageFullName
PS C:\WINDOWS\system32>

## Ül 9.8

<img width="481" height="562" alt="9 8" src="https://github.com/user-attachments/assets/c7b9039b-cf81-4e8b-bd30-c2372dfa8486" />

