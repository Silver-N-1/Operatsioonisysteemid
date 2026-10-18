# Praktikum 5



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

WM_NCHITTEST, sõnumi ID: 132 Tähendus (Non-Client Hit Test): Saadetakse aknale, et teha kindlaks, milline osa aknast vastab konkreetsele ekraanikoordinaadile. See võib juhtuda näiteks kursori liikumisel, hiirenupu vajutamisel või vabastamisel, või vastusena sellise funktsiooni nagu `WindowFromPoint` väljakutsumisele. Kui hiir ei ole hõivatud (st ükski aken pole seda enda kontrolli alla võtnud), saadetakse teade kursori all asuvale aknale. Vastasel juhul saadetakse teade aknale, mis on hiire enda kontrolli alla võtnud.
Parameetrite tähendus:

        wParam (0): Seda parameetrit selle sõnumi puhul ei kasutata.

        lParam (7799688): Sisaldab hiirekursori X ja Y koordinaate arvutiekraanil sõnumi saatmise hetkel. See arv koosneb kahest 16-bitisest osast. Kui arv 7799688 teisendada kuueteistkümnendsüsteemi (0x00770388), saab selle lahti murda:

            Alumine pool (0x0388 ehk detsimaalis 904) on X-koordinaat.

            Ülemine pool (0x0077 ehk detsimaalis 119) on Y-koordinaat.

WM_SETCURSOR, ID: 32 
    Mida tähendab: Windows saadab selle sõnumi, et aken saaks otsustada, millist hiirekursori ikooni tuleks kuvada (kas tavalist noolt, teksti sisestamise kriipsu (I-beam) või laadimise rullikut).

    Parameetrite tähendus:

        wParam (657014): Sisaldab selle akna või alamkomponendi (näiteks nupu või tekstivälja) unikaalset ID-d ehk Window Handle'it (HWND), mille kohal kursor parajasti asub.

        lParam (33554433): Sisaldab samuti kahte infojuppi, mis on kokku pakitud ühte 32-bitisesse arvu (Hex: 0x02000001).

            Alumine pool (0x0001) tähistab Hit Test koodi (eelmisest sõnumist). Väärtus 1 tähendab HTCLIENT ehk kursor on akna tavalisel tööalal.

            Ülemine pool (0x0200 ehk detsimaalis 512) näitab, milline hiiretegevus selle kursori uuendamise esile kutsus. Väärtus 512 on Windowsis WM_MOUSEMOVE sõnumi ID, mis kinnitab, et kursorit lihtsalt liigutati (mitte ei tehtud näiteks hiireklikki).
