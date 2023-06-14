Zaimplementuj aplikację z graficznym interfejsem pozwalającą przeprowadzić analizę statystyczną wyników klasyfikacji zgromadzonych w tzw. tabelach niezgodności (ang. confusion matrix). Obliczać należy współczynnik kappa oraz przynajmniej trzy inne miary (np. miary opisane w artykule:
https://arxiv.org/pdf/2008.05756.pdf).
Aplikacja powinna pozwalać na:
- wyświetlanie/edytowanie danych tabelarycznych;
- wybranie algorytmu, jakim będą one przetwarzane;
- wyświetlenie wyników przetwarzania (obliczonej miary).
W trakcie implementacji należy wykorzystać interfejs dostarczyciela serwisu (ang. Service Provider Interface, SPI). Dokładniej, stosując podejście SPI należy zapewnić aplikacji możliwość załadowania klas implementujących zadany interfejs już po zbudowaniu samej aplikacji. 
Klasy te (z zaimplementowanymi algorytmami wyliczającymi miary służące do oceny wyników klasyfikacji) mają być dostarczane w plikach jar umieszczanych w ścieżce. Należy stworzyć dwie wersje projektu: standardową oraz modularną.
