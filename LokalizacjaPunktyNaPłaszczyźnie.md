Dany jest podział D płaszczyzny i chcemy szybko określić w jakiś obszarze znajduje się dany punkt

## Metoda warstwowa

Podziel przestrzeń na wartswy równoległe do osi prostymi przechodzącymi przez wierzchołki podziału.
Ztablicuj warstwy oraz podziały w nich.

Lokalizacja punktu: Binsearch na warstwę, binsearch na podział w danej warstwie

| Czas | Pamięć | Zapytanie |
| ---- | ------ | --------- |
| O(n^2) | O(n^2) | O(logn) |

## Metoda trapezów

Posortuj wierzchołki względem y. Znajdź ich medianę i rozdziel zbiór względem tej medianej.

| Czas | Pamięć | Zapytanie |
| ---- | ------ | --------- |
| O(nlogn) | O(nlogn) | O(logn) |

## Metoda separatorów

Separator - monotoniczna względem danego kierunku łamana rozdzielająca podział i tworzoną przez jej krawędzie

| Metoda | Czas | Pamięć | Zapytanie |
| ------ | ---- | ------ | --------- |
| Ztablicowanie | O(n^2) | O(n^2) | O(log^2 n) |
| BST | O(nlogn) | O(n) | O(log^2 n) |

## Metoda doskonalenia triangulacji

| Czas | Pamięć | Zapytanie |
| ---- | ------ | --------- |
| O(n) | O(n) | O(logn) |