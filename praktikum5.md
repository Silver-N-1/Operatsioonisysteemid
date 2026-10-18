# Praktikum 5

Selles praktikumis õppisime vaatlema süsteemis töötavaid protsesse kasutades ps ja jobs ning mõistma protsessi ID (PID). Lisaks panime protsessid käivitama taustal (&) ning nende viimist esiplaanile ja taustale (fg, bg). Uurisime signaalide saatmist ning panime protsesse peatama, katkestama ja tapma (Ctrl+C, Ctrl+Z, kill). Lõpuks saime koostada ümber suunamisega protsessi sisendeid, väljundeid ja veateateid (>, >>, <, 2>) ning ühendasime need käsud torude (|) abil.  

_Ül 5.1_

<img width="643" height="456" alt="OS_5 1" src="https://github.com/user-attachments/assets/178c49ef-a6e9-412a-8dc2-a0cc9a27eb97" />


_Ül 5.2.1_

<img width="638" height="453" alt="OS_5 2_1" src="https://github.com/user-attachments/assets/aca639e8-fea7-47d4-80dc-cae9ece958a2" />


_Ül 5.2.2_

<img width="639" height="455" alt="OS_5 2_2" src="https://github.com/user-attachments/assets/f28894ec-efe5-4eb4-8728-1642c7dffbb9" />


_Ül 5.3_

<img width="642" height="455" alt="OS_5 3" src="https://github.com/user-attachments/assets/388c91bc-103a-4aaa-ae79-446e808392ce" />

_Ül 5.4_

<img width="644" height="457" alt="OS_5 4" src="https://github.com/user-attachments/assets/de297f04-c459-4719-bba3-158569e4cda8" />

_Ül 5.5_

WM_NCHITTEST, sõnumi ID: 132 
Tähendus (Non-Client Hit Test): Saadetakse aknale, et teha kindlaks, milline osa aknast vastab konkreetsele ekraanikoordinaadile. See võib juhtuda näiteks kursori liikumisel, hiirenupu vajutamisel või vabastamisel, või vastusena sellise funktsiooni nagu `WindowFromPoint` väljakutsumisele. Kui hiir ei ole hõivatud, st ükski aken pole seda enda kontrolli alla võtnud, saadetakse teade kursori all asuvale aknale. Vastasel juhul saadetakse teade aknale, mis on hiire enda kontrolli alla võtnud.

Parameetrite tähendus:

wParam (0): Seda parameetrit selle sõnumi puhul ei kasutata.

lParam (7799688): Sisaldab hiirekursori X ja Y koordinaate arvutiekraanil sõnumi saatmise hetkel. 

https://learn.microsoft.com/en-us/windows/win32/inputdev/wm-nchittest

WM_SETCURSOR, ID: 32 
Mida tähendab: Saadetakse aknale, kui hiir põhjustab kursori liikumise akna sees ja hiire sisend ei ole hõivatud.

Parameetrite tähendus:

wParam (657014): Viit aknale, mis sisaldab kursorit.

lParam (33554433): Sisaldab samuti kahte infojuppi, mis on kokku pakitud ühte 32-bitisesse arvu.

Alumine pool (0x0001) tähistab Hit Test koodi.
Ülemine pool (0x0200) näitab, milline hiiretegevus selle kursori uuendamise esile kutsus. Väärtus 512 on Windowsis WM_MOUSEMOVE sõnumi ID, mis kinnitab, et kursorit lihtsalt liigutati.

https://learn.microsoft.com/en-us/windows/win32/menurc/wm-setcursor

Failis nimeks ??? ja id < 45000:
Ei suutnud tekitada sellist olukorda, mille puhul id jääks alla 45000. Kõik mille läbi katsetasin tulid id'd suuremad kui 45000. Näiteks katsetasin ekraani heledaks/tumedaks teha, heli juurde/vähem, hiire rullikut vajutada ja teisi veel.
