Use Case 7: Obsługa dostawy
=====================

**Aktor podstawowy:** Dostawca


Główni odbiorcy i oczekiwania względem systemu:
-----------------------------------------------

- Dostawca: Oczekuje możliwości szybkiego i sprawnego wprowadzenia produktów zarówno mechanicznie do magazynu Pizzomatu, jak i do pamięci wewnętrznej systemu. Oczekuje bezproblemowego dostępu do kasy Pizzomatu, by dodawać brakujące nominały i pobierać zarobione pieniądze.

- Klient: Oczekuje obecności w magazynie Pizzomatu większości oferowanych dóbr bez konieczności oczekiwania na dostawę 

- Serwisant: Oczekuje, że w razie dowolnych usterek maszyny podczas dostawy, zostanie o nich niezwłocznie poinformowany.

- Przedsiębiorstwo: Oczekuje, że dostawa będzie przeprowadzona szybko, sprawnie i bez utrat pieniędzy ani produktów, aby Pizzomat dalej mógł generować zyski.

Warunki wstępne:
----------------
Dostawca otrzymał i przywiózł produkty mające zostać dostarczone do Pizzomatu.

Warunki końcowe:
----------------
Maszyna została poprawnie zamknięta. W magazynie maszyny znajdują się przewiezione produkty. Stan pamięci maszyny zgadza się z stanem faktycznym jej magazynu. Nie występują braki produktów ani nominałów. Nadmiar gotówki został pobrany przez dostawcę.

Scenariusz główny (ścieżka podstawowa):
---------------------------------------

  1. Dostawca wydaje polecenie zdjęcia blokad.
  2. System zwalnia blokady i otwiera się mechanicznie.
  3. Dostawca fizycznie wprowadza produkt do części magazynowej.
  4. Dostawca wprowadza identyfikator produktu do systemu.
*Dostawca powtarza kroki 4-5 aż wprowadzone zostaną wszystkie produkty.*
  5. System oblicza obecny stan magazynu na podstawie poprzednich danych oraz wprowadzonych zmian.
  6. Dostawca porównuje stan faktyczny z stanem systemu.
  7. Dostawca uzupełnia brakujące i pobiera nadmiarowe nominały.
  8. Dostawca wprowadza zmiany w gotówce na stanie magazynu. 
  9. Dostawca wydaje polecenie zamknięcia maszyny i uruchomienia blokad bezpieczeństwa.
  10. System zapisuje w pamięci wewnętrznej datę dostawy, identyfikator dostawcy i zmiany w magazynie.

Rozszerzenia (ścieżki alternatywne):
------------------------------------
*a. W dowolnym czasie, dotyczy sytuacji kiedy system zawiesza się:
1. Dostawca restartuje system, loguje się ponownie oraz sprawdza stan systemu
2. System odtwarza stan przed zawieszeniem się
2a. System wykrywa błędy: Dostawca rozpoczyna procedurę wprowadzenia danych o dostawie od nowa.

2a. - Błędny identyfikator
System sygnalizuje błąd i odrzuca próbę logowania się. Po trzech nieskutecznych próbach logowania, system blokuje mechanizm logowania na 5 minut.

 4a - Maszynowe zdjęcie blokad nie powodzi się:
1. System musi poinformować o usterce dostawcę, umożliwić mu restart Pizzomatu oraz przekazać mu dane kontaktowe do serwisanta.
2. Dostawca restartuje system, loguje się i ponawia żądanie
3. Ponowne żądanie otwarcia powodzi się - dostawca wraca do 5. oraz informuje o problemie serwisanta
4. Błąd powtarza się - dostawca informuje o problemie serwisanta oraz odkłada dostawę w czasie (przechodzi do 13.)

5-6a Do wprowadzenia jest kilka produktów tego samego typu, o identycznym identyfikatorze.
1. Dostawca fizycznie wprowadza wszystkie produkty do magazynu
2. Dostawca wprowadza identyfikator produktu oraz ilość produktów.

8a Któryś z produktów z uwagi na zdatność do spożycia lub inne usterki powinien zostać usunięty z magazynu
1. Dostawca fizycznie usuwa produkt
2. Dostawca wprowadza identyfikator oraz ilość usuwanych produktów

12a. Zasoby pamięci wewnętrznej są bardzo małe (Poniżej 50MB wolnej pamięci)
1. System wyświetla dostawcy komunikat o brakach wolnej pamięci oraz podaje kontakt do serwisanta
2. Serwisant podczas następnego okresowego przeglądu (patrz use case 10, w ramach prac konserwacyjnych) eksportuje dane do zewnętrznej pamięci oraz czyści pamięć wewnętrzną.


Wymagania specjalne:
--------------------

  - Czytelny ekran dotykowy umożliwiający przekazywanie komunikatów przez system oraz przekazywanie danych na temat dostawy do systemu. Tekst powinien być na nim widoczny z odległości co najmniej 1 metra.
  - Magazyn umożliwiający przechowywanie produktów spożywczych w sposób bezpieczny.
  - Autoryzacja dostawcy musi być dokonana w ciągu 5 sekund w 99% przypadków.

Wymagania technologiczne oraz ograniczenia na wprowadzane dane:
---------------------------------------------------------------

 2a. Identyfikator dostawcy wprowadzony z klawiatury ekranowej.

 6a. Identyfikator każdego produktu wprowadzony z klawiatury ekranowej.

 12a. Pamięć wewnętrzna o pojemności minimum 128mb. 

Kwestie otwarte:
----------------

  - Czy konieczna jest możliwość szybkiego anulowania całej dostawy w trakcie jej wykonywania?
  - Możliwe zmiany i problematyka związana z prawem w kontekście przechowywania żywności (Zasady i kontrole Państwowej Inspekcji Sanitarnej)
  - Czy komunikację dostawca-serwisant można zautomatyzować?


