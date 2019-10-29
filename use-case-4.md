Use Case 4: Obsługa zamówienia
=====================

**Aktor podstawowy:** Klient


Główni odbiorcy i oczekiwania względem systemu:
-----------------------------------------------

- Klient: Chce otrzymać zamówiony posiłek
- Bank: Chce pośredniczyć w płatności między Klientem a Systemem.


Warunki wstępne:
----------------
Klient posiada odpowiednią ilość gotówki, aby zakupić produkty. Klient rozumie komunikaty Systemu. Klient jest w stanie wykonać polecenia, które wyda mu Pizzomat.

Warunki końcowe:
----------------
Klient otrzymał zamówione produkty. Fundusze klienta zostały uszczuplone o sumę potrzebną do nabycia produktów. 

Scenariusz główny (ścieżka podstawowa):
---------------------------------------

  1. System wyświetla komunikat nakłaniający do zamówienia pizzy.
  2. Klient podchodzi do Pizzomatu.
  3. Klient wybiera co chce zamówić z listy dostępnych mu opcji.
  4. System dodaje wybrany produkt do listy zamówionych produktów.
  5. System wyświetla sumaryczny koszt zamówienia produktów które wybrał.
  6. Klient decyduje czy chce zamówić kolejny produkt.
  *Pizzomat powtarza kroki 4-6 do moment aż klient zdecyduje się nie zamawiać kolejnego produktu*
  7. Pizzomat wyświetla ostateczna kwotę jaką Klient powinien zapłacić.
  8. System proponuje metody płatności. 
  9. Klient wybiera płatność kartą.
  10. System wyświetla informację prosząc klienta o postępowanie zgodnie ze wskazówkami wyświetlanymi na terminalu banku.
  11. System czyta dane z karty z pomocą terminala i łączy się z Bankiem przekazując płatność do autoryzacji.*(klient realizuje płatność w sposób zawarty w Use Case: Płatność Kartą)*
  12. System odbiera informację o pomyślnym zakończeniu płatności. 
   13. System przygotowuje i wydaje zakupione przez klienta produkty. 
   14. System aktualizuje stany magazynowe. 
   15. System wyświetla komunikat nakłaniający do zamówienia pizzy.

Rozszerzenia (ścieżki alternatywne):
------------------------------------
 10a. Klient wybiera płatność gotówką. 
 11a. Pizzomat wyświetla informację proszącą o przekazanie pieniędzy do maszyny. 
 12a. System odbiera pieniądze i zmienia stan kasy w swojej pamięci.
 13a. System dokonuje niezbędnych obliczeń i decyduje czy wydać resztę czy nie. 
 14a. System wydaje resztę i ponownie aktualizuje stan kasy.

 14a*. System nie wydaje reszty. 

 12b. System odbiera informację o niepomyślnym zakończeniu płatności. 
 13b. System powiadamia klienta o problemie. 
 14b. System proponuje wybór metody płatności. 

Wymagania specjalne:
--------------------
  - Czytelny ekran przystosowany do wyświetlania komunikatów Systemu.
  - Autoryzacja płatności w czasie krótszym niż 30s w 90% przypadków. 
  - Przygotowanie i wydanie pizzy w czasie krótszym niż 5 min w 99% przypadków. 
  - Przygotowanie i wydanie napoju w czasie krótszym niż 40s w 95% przypadków. 
  - Przygotowanie i wydanie deseru w czasie krótszym niż 40s w 95% przypadków.
  - Wydanie pizzy, napoju i/lub deseru nadających się do spożycia w 99,99% przypadków. 
  
Wymagania technologiczne oraz ograniczenia na wprowadzane dane:
---------------------------------------------------------------

 12. Informacja o karcie wprowadzana przez czytnik kart połączony z Systemem. 
 13. Połączenie przez terminal płatniczy Pizzomatu i Banku.
 
Kwestie otwarte:
----------------

  - Brak blokady zamówienia większej ilości produktów od tej znajdującej się w magazynie.
  - Problemy z zaklinowaniem sie produktów podczas ich wydania.
  - Nie uwzględniono możliwości wycofania zamówienia. 
  - Nie uwzględniono możliwości usunięcia produktu z koszyka. 