### Szukanie liczby punktów w prostokącie na płaszczyźnie

Zadanie - Znaleźć punktyu należące do prostokąta

k - liczba znalezionych punktów

KD-drzewo -- Od `k-th dimentional tree`, takie wielowymiarowe drzewo przedziałowe naprzemiennie dzielące
płaszczyznę

Range tree -- Jakby zwykłe drzewo przedziałowe posortowane względem x ale dodatkowo węzły mają wskaźnik
na drzewo, gdzie elementy są posortowane względem y.

Kaskadowanie -- Jakby Range tree ale coś pozmieniali i jest w odpowiedzi log szybciej

priority search tree(PST) -- ???

| Wymiary | Czas | Pamięć | Odpowiadanie |
| ------- | ---- | ------ | --- |
| kd 2D | O(nlogn) | O(n) | O(k + sqrt(n)) |
| kd D | O(nlogn) | O(n) | O(k + n^{d-1/d} |
| range 2D | O(nlogn) | O(nlogn) | O(k + log^2 n) |
| range D | O(nlog^{d-1}n) | O(nlog^{d-1}n) | O(k + log^d n |
| Kaskadowanie 2D | O(nlogn) | O(nlogn) | O(k + log n) |
| Kaskadowanie D | O(nlog^{d-1}n) | O(nlog^{d-1}n) | O(k + log^{d-1} n |
| PST 2D | O(nlogn) | O(n) | O(k + logn) |

### Drzewo przedziałów (interval tree)

Drzewo przedziałów (interval tree) -- Jakieś drzewo przedziałowe ale biorące pod uwagę medianę a nie średnią

| Wymiary | Czas | Pamięć |
| ------- | ---- | ------ |
| interval tree | O(nlogn) | O(n) |

Znalezienie wszystkich poziomych odcinków z n-elementowego zbioru przecinanych daną pionową **prostą**
wymaga O(k + logn) czasu

Znalezienie wszystkich poziomych odcinków z n-elementowego zbioru przecinanych danym pionowym **odcinkiem**
wymaga O(k + log^2 n) czasu


### Drzewo odcinków (segment tree)

W n-elementowym zbiorze rozłącznych odcinków chcemy znaleźć te z nich, które przecinają prostokąt

| Wymiary | Czas | Pamięć |
| ------- | ---- | ------ |
| 2d | O(nlogn) | O(nlogn) |

Stosując drzewo odcinków, możemy podać wszystkie odcinki zawierające punkt(jakby przecięcie z prostą?)
zapytania w czasie O(k + logn)

Takie samo zadanie ale dla pionowego odcinka można zrobić w czasie O(k + log^2 n)

### Sprawdzenie istnienia pary przecinających się odcinków w modelu PRAM

Wykorzystując O(nlogn) procesorów można stworzyć drzewo odcinków w czasie O(logn)

W czasie O(logn) można określić czy istnieją co najmniej dwa odcinki, które się przecinają.

### Drzewo czwórkowe

Normalne drzewo przedziałowe ale z dzieleniem na 4, bo płaszczyzna

c - najmniejsza odległość między dwoma dowolnymi punktami

s - długośc boku początkowego

d - głebokość


Wysokość drzewa wynosi co najwyżej log(s/c) + 3/2

| Czas | Pamięć |
| ---- | ------ |
| O((d+1)n) | O((d+1)n) |

Podział kwadratu jest **zrównoważony** gdy długości boków sąsiednych kwadratów róznią się co
najwyżej dwukrotnie. Odpowiadające drzewo czwórkowe jest **zróżnoważone**.

Niech T będzie drzewem czwórkowym o m węzłach i głebokości d. Można je zrównoważyć by miało O(m) węzłów
w czasie O((d+1)m)

### Drzewo Binary Space Partition - BSP

Trochę jak kd-drzewo ale dzieli się względem odcinków a nie prostych równoległych do osi.
Jeżeli dzieli się przed ocinki ze zbioru to to się nazywa **autopodziałem**.

| Wymiary | Oczekiwana liczba fragmentów | Czas | Losowe dane? |
| ------- | ---------------------------- | ---- | ------------ |
| 2 | O(nlogn) | O(n^2 logn) | TAK |
| 3 | O(n^2) | --- | TAK |

Istnieją zbiory n nieprzecinających się trójkątów w R^3, dla których każdy autopodział ma romizar Omega(n^2)

Dla dowolnego zbioru n nieprzecinających się trójkątów w R^3 istnieje drzewo BSP rozmiary O(n^2)

Istnieje konfiguracja n nieprzecinających się trójkątów w R^3, dla której rozmiar każdego drzewo BSP
jest omega(n^2)
