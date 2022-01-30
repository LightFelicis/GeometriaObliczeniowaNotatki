## Obszar Voronoi

Obszar na płaszczyźnie, dla którego dany punkt jest najbliższy

Podział płaszczyzny na takie obszary tworzą **diagram Voronoi**

**Tiangulacja Delauny** - graf dualny do diagramu Voronoi

Właściwości diagramu Voronoi:
- planarny
- n ścian
- O(n) krawędzi
- punkt lężacy na brzegu 3 lub więcej obszarów jest środkiem okręgu przechodzącego przez sąsiednie punkty

Właściwości triangulacji Delaunay:
- każdy trójkąt odpowiada wierzchołkowi w diagramie Voronoi
- każda krawędź odpowiada krawędzi diagramu
- w R^2 maksymalizuje minimalny kąt triangulacji
- Triangulacja w R^d zawiera O(n^{\ceil{d/2}}) sympleksów (?)

Minimalne Drzewo Rozpinające (MST) wykorzystuje krawędzie z triangulacji Delaunay i  można
je znaleźć w czasie O(nlogn)

| Algorytm na znalezienia diagramu Voronoi| Czas | Pamięć |
| -------- | ---- | ---- |
| przyrostowy | O(n^2) | --- |
| dziel i zwyciężaj | O(nlogn) | --- |
| Zamiatanie parabol (Fortune) | O(nlogn) | O(n) |
| Rzutowanie na paraboloidę | O(nlogn) | --- |
| Rzutowanie na paraboloidę w k wymiarach | O(n^{\ceil{d/2}}) | --- |

## Diagramy w metrykach L_p

Odległość definiowana jak (a^p + b^p)^(1/p)

Obszary Voronoi nie muszą być wypukłe bo granice są krzywe a nie prostą.

W metrykach L_1 i L_inf granica może być łamaną lub połączonymi klinami

| Algorytm | Czas | Pamięć |
| -------- | ---- | ---- |
| dziel i zwyciężaj | O(nlogn) | --- |

## Diagramy potęgowe
Wzorek odległości od środka okręgu = x^2 + y^2 - r^2, czyli kwadrat długości stycznej

Własności:
- Krawędziami są odcinki, półproste lub proste
- Obszarami są ograniczone lub nieograniczone wielokąty wypukłe
- Gdy okręgi kół przecinają się to wspólna krawędż przechodzi przez ich punkty przecięcia
- Przecięcie obszaru z generatorem może być puste
- Mogą istnieć generatory bez odpowiadającego mu obszaru Voronoi

| Algorytm | Czas | Pamięć |
| -------- | ---- | ---- |
| dziel i zwyciężaj | O(nlogn) | --- |

## Diagram ważony - addytywny

Każdy punkt w S ma wagę

Szukamy p_i \in S, że minimalizuje dist(p_i, x) - w_i

Własności:
- Krawędzie diagramu są kawałkami hiperbol lub prostych,
- Wspólny brzeg dwóch obszarów może być niespójny
- Mogą nie istnieć obszarydla niektórych centrów

| Algorytm | Czas | Pamięć |
| -------- | ---- | ---- |
| dziel i zwyciężaj | O(nlogn) | --- |

## Diagramy Voronoi dla odcinków w R^2

Odległóść punktu p od odcinka definiujemy jako odległość od najbliżej punktu na odcinku

Własności:
- Krawędzie diagramu są odcinki, półproste, fragmenty parabol
- Każdy generator należy do swojego obszaru

| Algorytm | Czas | Pamięć |
| -------- | ---- | ---- |
| dziel i zwyciężaj | O(nlogn) | --- |

## Triangulacja Delaunay dla zbioru odcinków

???

## Szkielet

Podział wnętrza na obszary Voronoi wyznaczane przez krawędzie wielokąta, który jest 
miejscem geometrycznym środków okręgów stycznych do co najmniej 2 punktów na brzegu wielokąta

Własności:
- Krawędzie szkieletu prostego są odcinki
- Szkielet prosty dzieli wielokąt na wielokąty monotoniczne
- Szkielet prosty ma 2n-3 krawędzi

| Algorytm | Czas | Pamięć |
| -------- | ---- | ---- |
| wielokąta prostego | O(n) | --- |
| n-kąt prostego z r kątami rozwartymi | O(nlog^2 n + r^(3/2) log r | --- |
| n-kąt monotoniczny | O(nlogn) | --- |

## Diagramy Voronoi wyższych rzędów

VD_k - diagramy Voronoi k-tego rzędu

Dla kazdego podzbioru T szukamy obszaru, w którym **wsszystkie** punkty z T są bliżej niż z S/T

Diagram Voronoi k-tego rzędu można wyznaczyć w czasie O(k^2 n logn)

Tym algorytmem można znaleźć diagramy Voronoi wszystkich rzędów w czasie O(n^3 logn)

Istnieje algorytm (Edelsbrunner-Seidel) znajdujący diagramy Voronoi wszystkich rzędów
w czasie O(n^3)

Złożoność VD_k wynosi O(k(n-k))  i można to znaleźć w czasie O(nlog^3 n + k(n-k))

VD_(n-1) - **diagram najdalszych punktów**, ma rozmiar liniowy i można znaleźć w czasie O(nlogn)

## Beta szkielety

Dwa punkty x, y na płaszczyźnie są połączone krawędzią jeżeli w danym obszarze R(x,y,beta) nie ma innych punktów

Beta:
- 0 - R(x,y,beta) jest odcinkiem x-y
- 0 < beta < 1 - R(x,y,beta) jest przecięciem kul o promieniu d(x,y)/2beta, które zawierają na brzegu
punkty x i y
- 1 <= beta < inf - R(x,y,beta) jest przecięciem kul o promieniu beta * d(x, y)/2
- inf - R(x,y,beta) jest pasem rozciągniety miedzy punktami x i y

Beta = 1 -- graf Gabierla (GG)
beta = 2 -- graf relatywnego sąsiedztwa (RNG)

DT -- ??

MST \subseteq RNG \subseteq GG \subseteq DT

| Algorytm | Czas | Pamięć |
| -------- | ---- | ---- |
| RNG w R^2 | O(nlogn) | --- |
| GG w R^2 | O(nlogn) | --- |
| beta-szkielety dla 1 <= B <= 2 w R^2 | O(n) | --- |

GG w R^3 może mieć Omega(n^2) krawędzi
RNG w R^m może mieć Omega(n^2) krawędzi

**Współczynnik rozpięcie** to maksymalny iloraz odległości w grafie przez rzeczywistą odległość

| Algorytm | Współczynnik rozpięcie |
| -------- | ---------------------- |
| DT | O(1) |
| RNG | Omega(n) |
| GG | O(n^(1/2)) |