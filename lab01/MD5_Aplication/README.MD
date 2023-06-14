Napisz aplikację, która pozwoli na sprawdzania wskazanych katalogów pod kątem wystąpienia zmian w zawartych w nich plikach. Sprawdzenie zmian odbywać się ma poprzez wyliczanie funkcji skrótu MD5. 

Na początek alikacja powinna wyliczyć funkcję skrótu MD5 dla każdego badanego pliku i gdzieś ją zapamiętać. W ten sposób powstać ma "snapshot" bieżącej sytuacji. Następnie, podczas sprawdzania zmian, aplikacja powinna ponownie wyliczyć funkcję skrótu MD5 dla każdego badanego pliku i porównać ją z wartością wcześniej zapamiętaną. W ten sposób powstać ma "nowy snapshot". Na podstawie różnić między zapamiętanym "snapshotem" a "nowym snapshotem" można określić, czy w badanych plikach wprowadzono jakieś zmiany. Oczywiście po sprawdzeniu "snapshot" powinien być zastąpiony "nowym snapshotem".

Można przyjąć różne strategie co do sposobu zapamiętywania "snapshotu". Zalecane jest, by aplikacja składowała snapshoty w katalogu domowym użytkownika (np. w katalogu ".snapshot"). 
W ten sposób można zapamiętywać skróty plików w katalogach, które można "czytać", ale nie można w nich "pisać".

Innym sposób mógłby polegać na wstawianiu w przeglądanych katalogach dodatkowych plików ze skrótami o nazwach odpowiadających przeglądanym plikom (np. "oryginalna_nazwa_pliku.md5"). Jednak ten sposób nie pozwoli na przeglądanie katalogów tylko do "odczytu".

Aplikacja powinna być napisana z wykorzystaniem modułów (wprowadzonych w Javie od jdk 9). Powstać ma moduł biblioteki oraz moduł samej aplikacji (korzystający z modułu biblioteki). 

Powstałe moduły należy wyeksportować do plików jar.

Używając jlink należy przygotować minimalne środowisko uruchomieniowe, do którego podpięte zostaną wymienione wyżej moduły.

Aplikację powinno dać się uruchomić z linii komend, korzystając tylko z wygenerowanego środowiska uruchomieniowego. Sama aplikacja powinna oferować interfejs użytkownika (najlepiej graficzny, minimum - tekstowy).

Do operacji na plikach i katalogów należy wykorzystać pakiet klas java.nio. Ponadto zalecane jest napisanie programu w stylu funkcjonalnym.
