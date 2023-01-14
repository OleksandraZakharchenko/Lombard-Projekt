# Lombard-Projekt

Funkcjonalność

Strona – „Katalog”.
W kartach można umieszczać i usuwać Polubienia.
Wyświetlanie tabel według kategorii produktów.
Produkty można dodawać do koszyka.
Zaimplementowano Paginację po kliknięciu przycisku „Pokaż więcej”.
Polubienia i zawartość koszyka są zapisywane w LocalStorage.

Po załadowaniu strony żądanie trafia do serwera z katalogiem produktów. Jeśli błąd zostanie zwrócony po pierwszym żądaniu, aplikacja wysyła kolejne trzy dodatkowe żądania do serwera w dynamicznych odstępach czasu. Między żądaniami renderowany jest minutnik do następnego żądania. Jeśli po trzecim dodatkowym zapytaniu zostanie zwrócony błąd,
następnie renderowany jest komunikat o problemach na serwerze.

Pop-upy:
W pop-up polubień można: usunąć polubienie lub przejść do strony produktu
W wyskakującym koszyku możesz: usunąć produkt, zmienić ilość produktu, przejść do strony produktu lub strony kasy.
Karta towaru: możesz dodać produkt do koszyka, umieścić lub polubić
Strona kasy
Możesz usunąć produkt, zmienić ilość produktu lub przejść do strony produktu

Dla wysyłki do wyboru opcje Pickup lub Wysyłki. 
Koszty wysyłki opcji są różne i są brane pod uwagę w zamówieniu.

Po wybraniu opcji Wysyłki aplikacja określa kraj i miasto użytkownika za pomocą interfejsu API Geolocation. Jeśli użytkownik potwierdzi swoją lokalizację, w formularzu zamówienia pole „Region dostawy” zostanie zastąpione wartością.
Zestaw pól w formularzu zależy od opcji wysyłki. Brak pól Region dostawy i Adres wysyłki dla opcji Odbioru osobistego
Wymagane jest wypełnienie wszystkich pól, które zawiera formularz z wyjątkiem „Komentarz”.
 Zaimplementowano walidację tych pól „Imię i nazwisko” oraz „Numer telefonu" dla minimalnej liczby znaków. 
Błędy oraz sugestie ich poprawy są wyświetlane przed zatwierdzeniem.

Przy udanym zakupie:
Po załadowaniu strony zostanie uruchomione kilku sekundowe odliczanie, a następnie użytkownik zostanie przekierowany na Stronę Główną.

Błąd 404:
Przejście do nieistniejącego routa renderuje tak zwany „Error 404” z licznikiem czasu. Po upływie określonego czasu następuje przekierowanie do strony głównej

Wykorzystane przy realizacji projektu narzędzia:

Vue 3 Composition API
Vue Router
Pinia
API towarów: fakestoreapi.com
Geolocation API: BigDataCloud
Układ adaptacyjny

Drobne niedogodności:

Jako, że wykorzystywane przez nas w tym projekcie API napisane jest całkowicie w języku angielskim pobierane z niego produkty i kategorie dla napisanej na potrzeby strony są niestety również w tym języku. W celu zachowania krótkiego czasu reakcji oraz maksymalnej optymalizacji układu strony pozostawiliśmy domyślny język, ponieważ w API wymienione są:

- opis poszczególnych produktów
- nazwy wszystkich produktów
- nazwy kategorii 
- pozostałe informacje takie jak: kwota, grafiki produktów


Projekt powstał na potrzeby zaliczenia przedmiotu z rąk:

Oleksandra Zakharchenko 56863
Mateusz Jutrzenka 56113
