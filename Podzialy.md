# Triangulacje i inne podziały

## Triangulacja

Podział wielokąta na trójkąty przez maksymalny zbiór nieprzecinających
się przekątnych nazywamy **triangulacją** wielokąta.

W każdym wielokącie istnieje wierzchołek, w
którym kąt ma rozwartość mniejszą niż pi.

| Założenia | Złożoność |
| --------- | --------- |
| Brak      | O(n^2)    |
| Wielokąt ściśle monotoniczny | O(n) |
| Ważone wielokąty wypukłe | O(n^3) |

Wielokąt prosty nazywamy **ściśle monotonicznym** względem prostej k (wyznaczającej kierunek monotoniczności), gdy jego brzeg można podzielić na dwa
spójne łańcuchy takie, że dowolna prosta prostopadła do k przecina każdy z łańcuchów w co najwyżej jednym
punkcie. Wielokąt jest **monotoniczny**, gdy przecięcie dowolnej prostej prostopadłej do k
z dowolnym łańcuchem jest spójne.

## Podział wielokąta prostego na wielokąty monotoniczne

Prosty wielokąt o n wierzchołkach można powyższym algorytmem
podzielić na y-monotoniczne wielokąty w czasie ```O(n log n)``` używając
```O(n)``` pamięci.

### Chazelle

Dowolny wielokąt prosty można striangulować w czasie O(n).

### Minimalna liczba wielokątów w podziale 

Niech X oznacza minimalną liczbę wielokątów wypukłych, na które moż-
na podzielić dany wielokąt odcinkami (niekoniecznie przekątnymi). Niech
r będzie liczbą kątów wewnętrznych wielokąta o rozwartości większej niż
PI. Wtedy: sufit(r/2) + 1 <= X <= r +1.


### Algorytm Hertela-Mehlhorna

Liczba wielokątów wypukłych otrzymanych z pomocą algorytmu
Hertela-Mehlhorna jest co najwyżej czterokrotnie (4) większa niż
minimalna liczba takich wielokątów.

### Pary przecinających się odcinków

| Algorytm | Złożoność | Output sensitive |
| -------- | --------- | ---------------- |
| Brutalny | O(n^2)    | NIE              |
| Metoda zamiatania | O((n+k) log n) gdzie k to wynik | TAK |
| Czy istnieje | O(nlogn) | NIE |
| Algorytmu Balabana | O(nlogn + k), gdzie k to wynik | TAK |


### Znajdowanie pary najbliższych punktów na płaszczyźnie.

| Algorytm | Złożoność |
| -------- | --------- | 
| Brutalny | O(n^2)  |
| Metoda zamiatania | O(nlogn) |
