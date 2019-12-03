Zdarzenia systemowe
===================

Use case 1: Zamówienie pizzy.
-----------------

  - Klient wybiera rodzaj pizzy.
  - Klient wybiera ilość zamówionych pizz.
  
Use case 2: Zamówienie napoju.
-----------------

  - Klient wybiera rodzaj napoju.
  - Klient wybiera ilość zamówionych napojów.
 
  Use case 3: Zamówienie deseru.
-----------------

  - Klient wybiera rodzaj deseru.
  - Klient wybiera ilość zamówionych deserów.
 
  Use case 4: Zamówienie zestawu.
-----------------

  - Klient inicjalizuje zamówienie.
  *Klient powtarza zdarzenia z UseCase 1-3*  
  - Klient wybiera rodzaj płatności.
  *Klient jednokrotnie wykonuje zdarzenia z UseCase 5-6*
  - Klient odbiera zamówienie.
  - Klient potwierdza poprawność zakupu.
 
  Use case 5: Płatność kartą.
-----------------

  - Klient przykłada kartę.
  - Klient wpisuje PIN, jeśli to konieczne.
  
  Use case 6: Płatność gotówką.
-----------------
    
  - Klient wprowadza gotówkę.
 
  Use case 7: Obsługa dostawy.
-----------------

  - Dostawca autoryzuje się jako dostawca.
  - Dostawca wydaje polecenie zwolnienie blokady
  - Dostawca dodaje do systemu magazynowego produkt.
  - Dostawca usuwa z systemu magazynowego produkt.
  - Dostawca dodaje do systemu wydawania reszty nominał.
  - Dostawca wydaje polecenie założenia blokad.
  - Dostawca wylogowuje się.
 
  Use case 8: Wezwanie serwisanta.
-----------------
  - Dostawca wydaje polecenie wyświetlenia danych kontaktowych.
  - Dostawca wydaje specjalne polecenie bezwzględnej blokady systemu.

  Use case 9: Naprawa Pizzomatu.
-----------------
  - Serwisant autoryzuje się jako serwisant.
  - Serwisant wydaje polecenie zdjęcia blokad systemu.
  - Serwisant wydaje polecenie nałożenia blokad systemu.
  - Serwisant wylogowuje się.

  Use case 10: Okresowy przegląd Pizzomatu.
-----------------
  - Serwisant autoryzuje się jako serwisant.
  - Serwisant wydaje polecenie zdjęcia blokad systemu.
  - Serwisant wydaje polecenie nałożenia blokad systemu.
  - Serwisant wylogowuje się.
