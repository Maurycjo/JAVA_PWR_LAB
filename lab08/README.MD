Napisz program, w którym wykorzystane zostanie JNI. Zadanie do wykonania polegać ma na zadeklarowaniu klasy Java z dwiema metodami służącymi do obliczania dyskretnej dwuwymiarowej funkcji splotu  (ang. 2D discrete convolution function): natywną oraz normalną, a następnie przetestowaniu ich działania.

Metoda do obliczania splotu powinna przyjmować na wejście dwie tablice dwuwymiarowe (jądro splotu oraz macierz przetwarzaną) oraz produkować na wyjściu wynik (macierz wynikową). O tym, czym jest funkcji splotu, poczytać sobie można w wielu tutorialach, np. w dokumencie https://staff.uz.zgora.pl/agramack/files/conv/Splot.pdf 

Podczas testowania należy wygenerować odpowiednio duży problem obliczeniowy, a potem spróbować go rozwiązać korzystająć z obu zaimplementowanych metod. Testowanie powinno dać odpowiedź na pytanie, która z implementacji jest wydajniejsza. Stąd uruchamianiu metod powinno towarzyszyć mierzenie czasu ich wykonania (czyli coś na kształt testów wydajnościowych). Sposób wykonania takich testów jest dowolny, jednak warto spróbować wykorzystać do tego np. framework Mockito.

Jako wynik zadania, oprócz kodów źródłowych Java oraz kodu zaimplementowanej natywnej biblioteki, należy dostarczyć również raport z omówieniem wyników testowania. Proszę zwrócić uwagę na to, czy podczas testów nie uwidoczniło się działanie JIT.
