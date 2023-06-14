Napisz program, który pozwoli zasymulować działanie narzędzia do obsługi klientów firmy będącej dostawcą Internetu (zakładamy, że program będzie działał w kontekście dostawcy Internetu).

Zadanie należy zrealizować wykorzystując relacyjną bazę danych. 
Zalecane jest użycie sqlite (jest to baza danych w pliku, nie ma potrzeby istalowania żadnego dodatkowego serwisu). 

Podczas realizacji zadania należy skorzystać z mapowania ORM (technologia JPA, do czego można użyć framework Hibernate). Wtedy jednak należy zastosować wzorzec projektowy z użyciem serwisów. Generalnie projekt może być zrealizowany z użyciem frameworka Spring Boot.

Zakładamy, że w bazie danych będą przechowywane następujące informacje (jest to model mocno uproszczony w porównaniu do modeli spotykanych w rzeczywistości):
    Kient - imię, nazwisko, numer klienta
    Instalacja - adres, numer routera, typ usługi
    Naliczone należności - termin płatności, kwota do zapłaty
    Dokonane wpłaty - termin wpłaty, kwota wpłaty
    Cennik - typ usługi, cena 

Dla jednego klienta może być założonych wiele instalacji. 
Należności i wpłaty dotyczą danej instalacji. 
Należności naliczane są w trybie miesięcznym. 
Cennik dotyczy wszystkich typów usługi (aktywnych, wygasłych, nowych).


Program powinien:
    - umożliwiać ręczne zarządzanie danymi klientów, danymi instalacji oraz cennikiem
    - automatycznie naliczać należności i wysyłać monity o kolejnych płatnościach (wystarczy, że będzie pisał do pliku z logami monitów, upływ czasu należy zasymulować).
    - automatycznie eskalować monity w przypadku braku terminowej wpłaty (wystarczy, że będzie pisał do pliku z logami ekalowanych monitów, upływ czasu należy zasymulować)
    - umożliwiać ręczne rejestrowanie wpłat oraz nanoszenie korekt
    - umożliwiać przeglądanie należności i wpłat
**************************************************************************************
Zamień aplikację napisaną podczas poprzedniego labotatorium na usługę sieciową. Niech ta usługa będzie oferowała restowy interfejs pozwalający na wykonanie wszystkich operacji związanych z obsługą klientów firmy będącej dostawcą Internetu, a jej implementacja niech będzie wykonana z pomocą frameworka Spring Boot.

Implementacja może odbywać się według podejścia top-down (czyli najpierw definicja interfejsu wykonana w Swagger Editor, a potem wygenerowanie kodu źródłowego interfejsów i ich implementacja), albo według podejścia bottom-up (czyli najpierw redagowanie kodu źródłowego interfejsów i ich implementacja, a potem wygenerowanie swaggerowego opisu).

Efektem ma być tzw. backend, którego działanie będzie można:
* przetestować za pomocą swaggerowego interfejsu (automatycznie wygenerowanej strony internetowej, dającej możliwość sparametryzowania zapytań protokołu HTTP, ich wysłania na endpoint oraz wyświetlenia wyniku);
* przetestować za pomocą zewnętrznych narzędzi jak: Postman
