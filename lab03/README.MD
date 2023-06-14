Napisz aplikację, która pozwoli skonsumować dane pozyskiwane z serwisu oferującego publiczne restowe API. Ciekawą listę serwisów można znaleźć pod adresem:
https://rapidapi.com/collection/list-of-free-apis (wymagają klucza API), czy też https://mixedanalytics.com/blog/list-actually-free-open-no-auth-needed-apis/ (te klucza API nie wymagają). W szczególności w tej drugiej grupie istnieje: https://musicbrainz.org/doc/MusicBrainz_API. Właśnie to api ma być użyte w aplikacji.

Bazując na wskazanym api należy zbudować aplikację z graficznym interfejsem użytkownika, pozwalającą na przeprowadzanie testów z ogólnej wiedzy o utworach muzycznych, ich wydaniach i twórcach itp. Renderowanie zapytań i odpowiedzi powinno być tak zaimplementowane, by dało się zmianić ustawienia językowe (lokalizacji) w oparciu o tzw. bundle (definiowane w plikach i klasach - obie te opcje należy przetestować). Wspierane mają być języki: polski i angielski. 

Proszę zapoznać się z api i zaproponować kilka schematów zapytań i pól odpowiedzi. Niech zapytania będą parametryzowane wartościami pochodzącymi z list wyboru wypełnionych treścią pozyskaną z serwisu, a odpowiedzi niech będą uzupełniane wolnym tekstem lub wartościami z list wyboru (jeśli "charakter" pytania jest, odpowiednio, otwarty lub zamknięty). 
Odpowiedzi podanawane przez użytkownika powinny być weryfikowane przez aplikację (aplikacja, po wysłaniu zapytania przez api powinna sprawdzić, czy wynik tego zapytania jest zgodny z odpowiedzią udzieloną przez użytkownika).

 
Proszę pamiętać o obsłudze przynajmniej dwóch języków na interfejsie. Do tego proszę zastosować wariantowe pobieranie tekstów z bundli. Do tego przyda się klasa ChoiceFormat. 

Opcjonalnie można wykorzystać jakieś inne api, jeśli tylko zachowa się przedstawioną wyżej koncepcję (parametryzowane szablony zapytań, do wypełnienia pola odpowiedzi, linijka weryfikacji z odmianą przez liczby/osoby - wszystko przynajmniej z obsługą dwóch języków: polski i angielski).

