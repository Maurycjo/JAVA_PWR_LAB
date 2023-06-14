apisz aplikację, która umożliwi przeglądanie danych pomiarowych przechowywanych na dysku w plikach csv (w wersji minimum).
Zakładamy, że pliki danych będą składowane w folderach o nazwach reprezentujących daty kampanii pomiarowych (np. nazwą folderu może być 07.03.2023), zaś nazwy samych plików będą odpowiadały identyfikatorowi stanowiska pomiarowego oraz godzinie rozpoczęcia pomiarów (np. nazwą pliku może być 0001_10:00). 
Zawartość plików powinna odpowiadać następującemu schematowi:

# godzina pomiaru; ciśnienie [hPa];  temperatura [stopnie C]; wilgotność [%]
10:00; 960,34; -1,2; 60;
10:02; 960,34; -1,2; 60;
....

Pliki danych można stworzyć do testów posługując się generatorami losowymi czy innymi narzędziami.

Interfejs graficzny aplikacji powinien składać się z dwóch paneli - jednego, przeznaczonego do nawigacji po folderach i plikach, oraz drugiego, służącego do wyświetlania podglądu zawartości aktualnie wybranego pliku z danymi (wyświetlanych może być kilka pierwszych linijek) oraz wyników przetworzenia danych (wartości średnich dla kolejnych kolumn, poza kolumną z godziną pomiaru).

Aplikację należy zaprojektować z wykorzystaniem słabych referencji (ang. weak references). Zakładamy, że podczas przeglądania folderów z plikami danych pomiarowych zawartość aktualnie wybranego pliku będzie ładowana do odpowiedniej struktury oraz zostanie przetworzona (celem wyliczenia odpowiednich wartości). Słabe referencje powinny pozwolić na ominięcie konieczności wielokrotnego ładowania i przetwarzania tej samej zawartości - co może nastąpić podczas poruszanie się wprzód i wstecz po liście plików w folderach.

Aplikacja powinna wskazywać, czy zawartość pliku została załadowana ponownie, czy też została pobrana z pamięci. Wskazanie to może być zrealizowane za pomocą jakiegoś znacznika prezentowanego na interfejsie.

W celu oceny poprawności działania aplikację należy uruchamiać przekazując wirtualnej maszynie parametry ograniczające przydzielaną jej pamięć. Na przykład -Xms512m (co oznacza minimalnie 512 MB pamięci), -Xmx1024m (co oznacza maksymalnie 1GB).
Należy też przetestować możliwość regulowania zachowania się algorytmu odśmiecania, do czego przydają się opcje -XX:+ShrinkHeapInSteps, -XX:-ShrinkHeapInSteps. Proszę przestudiować, jakie inne atrybuty można przekazać do wirtualnej maszyny, w tym selekcji algorytmu -XX:+UseSerialGC, -XX:+UseParNewGC (deprecated), -XX:+UseParallelGC, -XX:+UseG1GC.

Architektura aplikacji powinna umożliwiać dołączanie różnych algorytów przetwarzania danych, jak również algorytmów renderujących fragment zawartości przeglądanego pliku (zakładamy, że aplikację będzie można rozbudować w celu przeglądania danych zapisanych w plikach o innym schemacie zawartości czy też innym formacie danych).
