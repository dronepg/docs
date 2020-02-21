# SAFEDAM

Projekt safedam realizuje temat:
*Zaawansowane technologie wspomagające przeciwdziałanie zagrożeniom związanym z powodziami*
Projekt jest finansowany ze środków NCBR w programie Bezpieczeństwo i Obronność.
Excento również dostaje finansowanie z NCBR.

!!! note
    Safedam jest to system który kompleksowo podchodzi do problemu.
    Ma o wiele więcej ludzi zangarzowanych w problem. 
    Dlatego nie powinniśmy czuć się zniechęceni, widząc, ze realizujemy tylko podsystem ich całego projektu.



W skład konsorcjum SAFEDAM wchodzi:

- Wydział Geodezji i Kartografii
- Instytut Meteorologii i Gospodarki Wodnej
- Astri Polska Sp. z o.o.(firma odpowiedzialna za integrację systemów IT)
- Szender Marcin MSP (firma od której mają drona i samolot)
- Centralna Szkoła Państwowej Straży Pożarnej

[Kontakty](https://www.safedam.gik.pw.edu.pl/Wykonawcy):

- [dr inż. Krzysztof Bakuła](http://www.gik.pw.edu.pl/index.php/kontakt-pracownicy/21-zaklad-fotogrametrii-i-teledetekcji-2/108-dr-inz-krzysztof-bakula) - przewodniczący Komitetu Sterującego, przedstawiciel PW 
- [mgr inż. Edmund Sieinski](http://www.imgw.pl/dzialalnosc-imgw-pib/struktura-organizacyjna/komorki-organizacyjne-2/oddzial-morski-w-gdyni/) - przedstawiciel IMGW - Centrum Państwowej Służby ds. Bezpieczeństwa Budowli Piętrzących
- [mrg. Dagmara Zelaya Wziątek](https://www.linkedin.com/in/dagmara-zelaya-wziątek-41938a61) - SAFEDAM Project Coordinator at IMGW

Nad projektem Safedam na "pełen etat" pracuje:

- 3 Osoby z IMGW
- 4 Osoby z PW
- 4 Osoby z Astri

!!! note
    Jak widać część informatyczna nie jest dziedziną dominującą nad tym problemem, wniosek płynący z tego jest taki ze programiści są jedynie odpowiedzialni za implementacje rozwiązań, które tworzą powyższe podmioty. 

Wczesne wykrycie [uszkodzeń](../levees/levees.md#uszkodzenia) [wałów przeciwpowodziowych](../levees/levees.md), a szczególnie zmiany geometrii wałów, a tym samym identyfikacja potencjalnych uszkodzeń, daje możliwość szybkiej reakcji w postaci zabezpieczenia lub modernizacji zagrożonego odcinka. Ponadto znajomość precyzyjnych danych wysokościowych, z dokładnością poniżej decymetra, usprawnia zarządzanie akcją ratowniczą, a przede wszystkim pozwala na oszacowanie zagrożenia związanego z przelaniem się wody przez korpus wału (poprzez oszacowanie różnicy wysokości zwierciadła wody do korony wału). Wykrywanie potencjalnych uszkodzeń wału może odbywać się na pojedynczej serii danych pomiarowych (wówczas analizie podlegają wykryte anomalie terenu rozumiane jako zaburzenia struktury wałów) lub na podstawie detekcji zmian terenu w czasie.

Dodatkowo SAFEDAM zaadresował problem [roślinności](../levees/levees.md#roslinnosc) która porasta wały przeciwpowodziowe. 

System SAFEDAM zaproponował 2 tryby działania swojego systemu

1. [Tryb prewencyjny](#tryb-prewencyjny)
2. [Tryb interwencyjny](#tryb-interwencyjny)

## Tryb prewencyjny

W tym trybie platforma pozwala na:

1. Zbieranie danych pomiarów satelitarnych, kamer fotogramatycznych (zakres RGB), bliskiej podczerwieni (NIR), oraz przestrzennych za pomocą skanowania laserowego (LiDAR), 

2. Analizowaniu ocen zagrożenia dzięki obrazom lotniczym i satelitarnym [ISOK](https://isokmapy.kzgw.gov.pl/imap_rzgw/Imgp.html).

3. Wizualizowanie danych na potrzeby służb hydrologicznych i specjalistów zarządzania kryzysowego

4. Ocena stanu wałów pod kątem wystąpienia zagrożenia.

5. W przypadku identyfikacji obszarów zagrożenia, przekazywana jest informacja do Centrum Modelowania Powodzi i Suszy [CMPiS](http://baltyk.pogodynka.pl/index.php?page=2&subpage=59) w celu aktualizacji map zagroenia przeciwpowodziowego. 

W trybie prewencyjnym system nastawiony jest na badanie obwałowań oraz ruchu mas gruntu przy normalnym stanie wód. Ze względu na potrzebę szybkiego pomiaru dużego obszaru, zdecydowano o zastosowaniu bezzałogowego samolotu fotogrametrycznego, przystosowanego do przenoszenia skanera laserowego - LIDAR. Został on wyposażona w ultralekki skaner laserowy, dwie cyfrowe kamery kadrowe o dużej rozdzielczości, obrazujące w zakresie RGB i NIR i dostarczające wysokiej jakości obrazy z pikselem kilkucentymetrowym, co pozwala na generowanie ortofotomap o wysokiej rozdzielczości. Połączenie dwóch takich samych kamer, z czego jedna rejestruje wyłącznie NIR, daje z kolei możliwość analiz danych wielospektralnych. 

Do trybu prewencyjnego zastosowano UAV typu płatowiec NEO3 firmy MPS, więcej informacji w rozdziale poświęconym tej konstrukcji.

## Tryb Interwencyjny

W przypadku zaistnienia zagrożenia system przechodzi w tryb interwencyjny, pomaga straży pożarnej oraz służbą zarządzania kryzysowego. UAV dostarcza danych z kamery światła widzialnego oraz termowizyjnego. Dostępne są wtedy podstawowe narzędzia podglądu stanu wałów, pomiaru odległości, objętości, wysokości względnej od lustra wody i wysokości wałów przeciwpowodziowych. Tworzone sa równiez szkice do prowadzonej akcji, oraz dokumentacja dla Straży Pożarnej.

W wyborze platformy w wersji interwencyjnej kierowano się przede wszystkim dyspozycyjnością i łatwością operowania nią oraz jak najszybszą możliwością przesyłania danych w czasie rzeczywistym. Te wymagania spełnia platforma typu wielowirnikowiec, którą jest udoskonalana obecnie wersja maszyny ZAWISAK produkcji firmy MSP, więcej informacji w [rozdziale poświęconym tej konstrukcji](zawisak.md). Platforma jest wyposażona w głowicę obserwacyjną w zakresie optycznym i termalnym, co umożliwi ciągły monitoring akcji również w warunkach nocnych.

