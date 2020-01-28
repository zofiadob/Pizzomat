Opis skrócony przypadków użycia
===============================

Aktorzy procesu i ich cele
--------------------------

Aktor       Cel 

---

Klient   -   Nabycie produktu.
Dostawca   -  Uzupełnienie stanu magazynowego Pizzomatu.
Serwisant - Wykonanie prac konserwacyjnych. 

Słownik
-------

Hasło       Opis

---

Produkt   Pizza, napój lub deser

Pizzomat Nazwa maszyny której przypadki użycia czytasz!

Typ produktu  Rodzaj produktu klasyfikowany unikalną nazwą.

Zestaw    Dowolna kombinacja dowolnej ilości dowolnych typów produktów

Transakcja Przepływ środków pieniężnych

Przypadki użycia
----------------

### Use case 1: Zamówienie pizzy.

System wyświetla slogan wraz z podprogowym przekazem narzucającym zamówienie pizzy. Klient wybiera pizzę z listy dostępnych pizz. System wyświetla kwotę, którą należy uiścić. Klient płaci gotówką lub kartą. System przygotowuje pizzę i ją wydaje. Klient otrzymuje pizzę.

### Use case 2: Zamówienie napoju.

System wyświetla slogan wraz z podprogowym przekazem narzucającym zamówienie pizzy. Klient wybiera napój z listy dostępnych napoi. System wyświetla kwotę, którą należy uiścić. Klient płaci gotówką lub kartą. Klient otrzymuje napój.

### Use case 3: Zamówienie deseru.

System wyświetla slogan wraz z podprogowym przekazem narzucającym zamówienie pizzy. Klient wybiera deser z listy dostępnych deserów. System wyświetla kwotę, którą należy uiścić. Klient płaci gotówką lub kartą. Klient otrzymuje deser.

### Use case 4: Zamówienie zestawu.

System wyświetla slogan wraz z podprogowym przekazem narzucającym zamówienie pizzy. Klient wybiera produkty w ilości >= 2 spośród całego asortymentu. System wyświetla kwotę, którą należy uiścić. Klient płaci gotówką lub kartą. Klient otrzymuje zamówienie. 

### Use case 5: Płatność kartą.

System wyświetla kwotę do zapłaty oraz dostępne sposoby płatności. Klient wybiera płatność kartą. System uruchamia terminal płatniczy. Klient wprowadza kartę do terminalu. System prosi klienta o podanie PINu. System przetwarza transakcję. System wyświetla stosowny komunikat o powodzeniu transakcji. System kontynuuje działanie. 

### Use case 6: Płatność gotówką.

System wyświetla kwotę do zapłaty oraz dostępne sposoby płatności. Klient wybiera płatność gotówką. Klient płaci. System przetwarza transakcję oraz wydaje ewentualną resztę. System wyświetla stosowny komunikat o powodzeniu transakcji. System kontynuuje działanie. 

### Use case 7: Obsługa dostawy.

Dostawca autoryzuje się w systemie. System wyświetla komunikat potwierdzający autoryzację i zwalnia blokady magazynowe. Dostawca uzupełnia stan magazynu oraz wprowadza dane odnośnie ilości i typów uzupełnionych produktów i/lub nominałów. Dostawca wydaje polecenie zablokowania magazynu. Dostawca sprawdza szczelność blokad. Po potwierdzeniu szczelności blokad, proces ulega zakończeniu.

### Use case 8: Wezwanie serwisanta

W razie zauważenia uchybień bezpieczeństwa przez dostawcę, pobiera on z systemu dane kontaktowe do serwisanta. Dostawca wydaje polecenie bezwzględnej blokady systemu. Dostawca kontaktuje się z serwisantem, który niezwłocznie przybywa na miejsce.

### Use case 9: Naprawa Pizzomatu

Serwisant autoryzuje się w systemie oraz zdejmuje wszelkie blokady systemu. Serwisant wykonuje niezbędne naprawy.  System wprowadza do pamięci wewnętrznej dane na temat daty wystąpienia usterki, identyfikatora serwisanta oraz ewentualnych kodów błędów.

### Use case 10: Okresowy przegląd Pizzomatu

Serwisant autoryzuje się w systemie. Serwisant sprawdza działanie wszystkich podsystemów Pizzomatu. System wprowadza do pamięci wewnętrznej dane na temat daty przeglądu i identyfikatora serwisanta.

### Use case 11: Powiadomienia o brakach produktów

W momencie wydania ostatniego produktu danego typu system powiadamia dostawcę o konieczności dostawy. System blokuje możliwość zakupienia danego produktu. 

### Use case 12: Awaria zamówienia

W trakcie realizacji zamówienia dochodzi do błędu. System informuje klienta o zaistniałej sytuacji. System bezwzględnie blokuje działanie Pizzomatu i wyświetla informacje na temat kontaktu z serwisem.  Klient kontaktuje się z serwisantem i informuje o problemie. Klient dochodzi swoich roszczeń na drodze reklamacji. Serwisant przyjmuje zgłoszenie.

### Use case 13: Powiadomienie o braku środków


W momencie wydania ostatniej jednostki obsługiwanego nominału, system powadamia dostawcę o konieczności uzupełnienia kasy. 


