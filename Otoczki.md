# Otoczki, lokalizacja punktu, punkty dominujące

## Lokalizacja punktu wewnątrz wielokąta prostego

| Założenia | Złożoność | 
| --------- | --------- |
| Brak      | O(n)      |
| 3D        | O(n)      |
| W wielokącie wypukłym | O(logn) |

## Otoczka wypukła

Co najmniej nlogn -> można sprowadzić do sortowania

| Nazwa | Złożoność | Output sensitive |
|------ |-----------| -----------------|
| Algorytm Jarvisa (gift wrapping, marsz Jarvisa)  |  O(n^2), lub O(cn), gdzie c to liczba wierzchołków w otoczce | TAK |
| Algorytm Jarvisa 3D | O(n^2) | TAK |
| Dziel i rządź (podnoszenie mostów, Preparata i Hong) | O(n) łączenie mostów, całość O(nlogn) | NIE |
| Dziel i rządź 3D | O(nlogn) | NIE |
| Algorytm Kirkpatricka i Seidela | O(nlogc), gdzie c to maksymalny rozmiar zbioru z F | TAK |
| Algorytm zamiatania | O(nlogn) sortowanie punktów, O(n) badanie stycznych i usuwanie | NIE |
| Algorytm zamiatania 3D | O(n^2) | NIE |
| Algorytm Grahama | O(nlogn) sortowanie biegunowe punktów, O(n) szukanie otoczki | NIE |
| Algorytm przyrostowy | O(nlogn) -- szukanie w BST O(logn), dodawanie/usuwanie zamortyzowane O(n) | NIE |
| Algorytm przyrostowy 3D | O(n^2) | NIE |
| Algorytm Quickhull | O(nc), gdzie c to liczba elementów otoczki | TAK | 
| Algorytm Quickhull 3D | O(nc), gdzie c to liczba elementów otoczki | TAK |
| Algorytm Chana | O(nlogc), gdzie c to rozmiar otoczki | TAK |
| Algorytm Chana 3D | O(nlogc), gdzie c to rozmiar otoczki | TAK |
| Przybliżona otoczka wypukła **HEURA** | O(n+k), gdzie k to liczba pasów (rozmiar otoczki / 2) | TAK |
| Przybliżona otoczka wypukła 3D **HEURA** | O(n+k^2logk), gdzie k to liczba pasów | TAK |
| Dynamiczna otoczka wypukła (Overmars i van Leeuwen) | Wstawienie/Usunięcie O(log^2(n)), czyli wszystko O(nlog^2(n)) | NIE |
| Otoczka wypukła wielokąta prostego | O(n) pamięć i czas | NIE | 

## Rozmiar otoczki 

| Założenia | Rozmiar |
| --------- | ------- |
| Równomierne wewnątrz wielokąta wypukłego | O(logn) |
| Równomierne na kole | O(n^(1/3)) |
| Rozkład normalny na płaszczyźnie | O(log^(1/2)n) |

## Punkty dominujące

Punkt p1 dominuje nad punktem p2 względem współrzędnej x, gdy x(p1) > x(p2).
W pierwszej ćwiartce układu współrzędnych R2 punkt p jest dominujący w zbiorze 
S, gdy żaden punkt z S nie dominuje nad nim względem obu współrzędnych.
Inaczej: punkt p jest dominujący w zbiorze S, gdy można dosunąć do p nieograniczony
prostokąt o bokach równoległych do osi współrzędnych, który nie zawiera w
swoim wnętrzu punktów z S. Podobnie możemy zdefiniować punkty dominujące w innych 
ćwiartkach i dla wyższych wymiarów.

### Szukanie punktów dominujących 

| Algorytm | Złożoność |
| -------- | --------- |
| Algorytm zamiatania | O(nlogn) |

