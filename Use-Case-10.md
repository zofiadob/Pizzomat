Use case 10: Okresowy przegląd Pizzomatu
=====================

**Aktor podstawowy:** Serwisant

Główni odbiorcy i oczekiwania względem systemu:
-----------------------------------------------

- Serwisant: Chce pomyślnie przeprowadzić konserwacje Pizzomatu by doprowadzić i utrzymać go w stanie używalności.
- Przedsiębiorstwo: Chce sprawnie działających automatów.

Warunki wstępne:
----------------

Automat jest w stanie umożliwiającym autoryzacje Serwisanta.

Warunki końcowe:
----------------

Przegląd został pomyślnie przeprowadzony i zajerestrowany w systemie. Pizzomat jest zdatny do dalszego użytkowania przez potencjalnych klientów.

Scenariusz główny (ścieżka podstawowa):
---------------------------------------

1. Serwisant autoryzuje się w systemie Pizzomatu.
2. Serwisant zdejmuje wszelkie blokady.
3. Serwisant skutecznie dostaje się do wszystkich podsystemów.
4. Serwisant sprawdza stan i działanie wszystkich podsystemów.
5. Serwisant wykonuje wszystkie niezbędnę prace konserwacyjne.
6. Serwisant zakłada z powrotem wszystkie blokady.
7. Serwisant wpisuje w systemie date, w którą przegląd został wykonany.
8. Serwisant wpisuje w systemie swój identyfikator.
9. Serwisant potwierdza w systemie, że przegląd został wykonany.
10. System informuje serwisanta, że podane dane zostały zapisane.

Rozszerzenia (ścieżki alternatywne):
------------------------------------

 *a. W dowolnym czasie, dotyczy sytuacji kiedy system zawiesza się:
Dla zapewnienia poprawnego zapisywania konserwacji, niezbędne jest aby wszystkie kluczowe dane dotyczące sesji mogły zostać odtworzone w dowolnym momencie ścieżki podstawowej.

1. Serwisant restartuje system.
2. System przywraca wszystkie stracone dane.
3. Serwisant przechodzi do dalszych kroków.

1a. Błędny kod podany przez serwisanta podczas autoryzacji.

1. System rejestruje błędnie podany kod.
2. System wyświetla komunikat o błędzie.
3. Serwisant dokonuje ponownej próby wpisania kodu.

 2a. Serwisant nie może przejść do dalszych ktoków z powodu uszkodzenia blokad.

1. Serwisant usuwa wadliwe blokady.
2. Serwisant zakłada nowe blokady bądź naprawia i zakłada stare blokady.

7a. Serwisant podał błędną date.

1. Serwisant wybiera opcje edycji daty.
2. Serwisant podaje poprawną date.
3. Serwisant zapisuje zmiany.

8a. Serwisant podaje błędny indetyfikator (do 3 razy).

1. System rejestruje błędnie podany indetyfikator.
2. System wyświetla komunikat o błędzie.
3. System wyświetla komunikat o ilości pozostałych prób.
4. Serwisant dokonuje poprawnego podania identyfikatora.

8b. Serwisant podaje błędny indetyfikator (więcej niż 3 razy).
1. System wyświetla komunikat o przekroczonej liczbie prób dostępu. 
2. System prosi o ponowne podanie kodu autoryzacyjnego. 
3. Serwisant podaje poprawny kod autoryzacyjny.
4. System wyświetla komunikat o poprawnie podanym kodzie. 
5. System daje Serwisantowi możliwość ponownego wpisania identyfikatora. (3 próby)
6. Serwisant podaje poprawny identyfikiator.

Wymagania specjalne:
--------------------

- Pizzomat musi posiadać ekran dotykowy
- Możliwość interfejsu wielojęzykowego
- Autoryzacja Serwisanta musi być dokonana w czasie 30 sekund.

Wymagania technologiczne oraz ograniczenia na wprowadzane dane:
---------------------------------------------------------------

1a. Serwisant autoryzuje się poprzez wpisanie specjalnego 10-cyfrowego kodu.

8a.  Indentyfikator Serwisanta składa się z 8-cyfrowego ciągu znaków i liczb oraz musi istnieć w systemie.

Kwestie otwarte:
----------------

- Czy jest momżliwość wprowadzenia czytnika np. do skanowania kodów ze zniżkami.

- Czy autoryzacja Serwisanta może przebiegać za pomocą specjalnej karty zamiast wpisywanego kodu? (Jeżeli istaniałby czytnik do kart.)

- Czy system może sam wypełniać datę przeglądu?.

Use case 10: Okresowy przegląd Pizzomatu
=====================

**Aktor podstawowy:** Serwisant

Główni odbiorcy i oczekiwania względem systemu:
-----------------------------------------------

- Serwisant: Chce pomyślnie przeprowadzić konserwacje Pizzomatu by doprowadzić i utrzymać go w stanie używalności.
- Przedsiębiorstwo: Chce sprawnie działających automatów.

Warunki wstępne:
----------------

Automat jest w stanie umożliwiającym autoryzacje Serwisanta.

Warunki końcowe:
----------------

Przegląd został pomyślnie przeprowadzony i zajerestrowany w systemie. Pizzomat jest zdatny do dalszego użytkowania przez potencjalnych klientów.

Scenariusz główny (ścieżka podstawowa):
---------------------------------------

1. Serwisant autoryzuje się w systemie Pizzomatu.
2. Serwisant zdejmuje wszelkie blokady.
3. Serwisant skutecznie dostaje się do wszystkich podsystemów.
4. Serwisant sprawdza stan i działanie wszystkich podsystemów.
5. Serwisant wykonuje wszystkie niezbędnę prace konserwacyjne.
6. Serwisant zakłada z powrotem wszystkie blokady.
7. Serwisant wpisuje w systemie date, w którą przegląd został wykonany.
8. Serwisant wpisuje w systemie swój identyfikator.
9. Serwisant potwierdza w systemie, że przegląd został wykonany.
10. System informuje serwisanta, że podane dane zostały zapisane.

Rozszerzenia (ścieżki alternatywne):
------------------------------------

 *a. W dowolnym czasie, dotyczy sytuacji kiedy system zawiesza się:
Dla zapewnienia poprawnego zapisywania konserwacji, niezbędne jest aby wszystkie kluczowe dane dotyczące sesji mogły zostać odtworzone w dowolnym momencie ścieżki podstawowej.

1. Serwisant restartuje system.
2. System przywraca wszystkie stracone dane.
3. Serwisant przechodzi do dalszych kroków.

1a. Błędny kod podany przez serwisanta podczas autoryzacji.

1. System rejestruje błędnie podany kod.
2. System wyświetla komunikat o błędzie.
3. Serwisant dokonuje ponownej próby wpisania kodu.

 2a. Serwisant nie może przejść do dalszych ktoków z powodu uszkodzenia blokad.

1. Serwisant usuwa wadliwe blokady.
2. Serwisant zakłada nowe blokady bądź naprawia i zakłada stare blokady.

7a. Serwisant podał błędną date.

1. Serwisant wybiera opcje edycji daty.
2. Serwisant podaje poprawną date.
3. Serwisant zapisuje zmiany.

8a. Serwisant podaje błędny indetyfikator (do 3 razy).

1. System rejestruje błędnie podany indetyfikator.
2. System wyświetla komunikat o błędzie.
3. System wyświetla komunikat o ilości pozostałych prób.
4. Serwisant dokonuje poprawnego podania identyfikatora.

8b. Serwisant podaje błędny indetyfikator (więcej niż 3 razy).
1. System wyświetla komunikat o przekroczonej liczbie prób dostępu. 
2. System prosi o ponowne podanie kodu autoryzacyjnego. 
3. Serwisant podaje poprawny kod autoryzacyjny.
4. System wyświetla komunikat o poprawnie podanym kodzie. 
5. System daje Serwisantowi możliwość ponownego wpisania identyfikatora. (3 próby)
6. Serwisant podaje poprawny identyfikiator.

Wymagania specjalne:
--------------------

- Pizzomat musi posiadać ekran dotykowy
- Możliwość interfejsu wielojęzykowego
- Autoryzacja Serwisanta musi być dokonana w czasie 30 sekund.

Wymagania technologiczne oraz ograniczenia na wprowadzane dane:
---------------------------------------------------------------

1a. Serwisant autoryzuje się poprzez wpisanie specjalnego 10-cyfrowego kodu.

8a.  Indentyfikator Serwisanta składa się z 8-cyfrowego ciągu znaków i liczb oraz musi istnieć w systemie.

Kwestie otwarte:
----------------

- Czy jest momżliwość wprowadzenia czytnika np. do skanowania kodów ze zniżkami.

- Czy autoryzacja Serwisanta może przebiegać za pomocą specjalnej karty zamiast wpisywanego kodu? (Jeżeli istaniałby czytnik do kart.)

- Czy system może sam wypełniać datę przeglądu?.

