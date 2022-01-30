## Duazliacja biegunowa

Punktowi o współrzędnych (a, b) przypisujemy prostą o równaniu ax + by + 1 = 0

Własności:
- Punkty przekształcane są na proste, a proste na punkty
- Jeżeli punkt p jest odległy od środka współrzędnych c o d, to odpowiadająca mu prosta k
jest odległa od punktu c o 1/d a punkty p i c wyznaczają prostą prostopadłą do k, c leży
  między p i k
  
## Dualizacja liniowa
Punktowi o współrzędnych (a, b) przypisujemy prostą o równaniu ax - b.
Dziedzinę przekształcenia nazywamy przestrzenią pierwotną a zbiór obrazów nazywamy przestrzenią dualną.

Własności:
- Przekształcenie jest swoją odwrotnością, to znaczy D(D(x)) = x
- Punkty przekształcane są na proste, a proste na punkty
- Punkt p należy do prostej k <=> Punkt D(k) nalezy do prostej D(p)
- Punkty p_i należa do prostej k <=> Proste D(p_i) przecinają się w punkcjie D(k)
- Jeżeli punkt p leży powyżej prostej k to punkt D(k) leży powyżej prostej D(p) 

## Sortowanie biegunowe

DLa każdego punktu z S chcemy znaleźć porządek biegunowy pozostałych punktów ze zbioru S.

Problem jest równowazny szukaniem przecięć prostych w przestrzeni dualnej i ich uszeregowanie.

Wynik ma rozmiar Omega(n^2), więc nie da się tego zrobić szybciej

Podział płaszczyzny prostymi nazywamy **układem prostych**. Obszary układu
prostych sąsiadujące z daną prostą nazywamy **strefą** tej prostej

Złożonośc strefy dla prostej w układzie o m prostych wynosi O(m)

| Czas |
| ---- |
| O(n^2) |

## Problem prostej przecinającej w R^2

Czy istnieje prosta przecinająca wszystkie odcinki?

| Czas |
| ---- |
| O(nlogn) |

## Szukanie minimalnego trójkąt

Chcecmy znaleźć trójkąt o minimalnym polu i wierzchołkach w S.

| Czas |
| ---- |
| O(n^2) |

## Poziomy

Poziomem punktu w układzie prostych U nazywamy liczbę prostych powyżej niego

| Czas |
| ---- |
| O(n^2) |

## k-zbiory

k-zbiorem nazywamy k elementowy podzbiór T, że istnieje prosta rozdzielająca zbiory T i S - T

Znajdź liczbę k-zbiorów oraz je określ

Maksymalna liczba k-zbiorów wynosi O(nk^(1/3))
Maksymalna liczba k-zbiorów wynosi Omega(n exp(c log^(1/2) k)) dla pewnej stałej c