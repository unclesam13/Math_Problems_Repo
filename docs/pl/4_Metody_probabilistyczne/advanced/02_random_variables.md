# LISTA ZADAŃ NR 2: Zmienne losowe (jednowymiarowe i dwuwymiarowe)

## Zadanie 1
W grupie studenckiej przeprowadzono sprawdzian. Niech $X$ oznacza ocenę (na skali ocen 2–5) losowo wybranego studenta. Czy $X$ jest zmienną losową?

Jeżeli przyjmiemy, że grupę stanowi 10 osób, a ich oceny to zbiór $\{5, 4, 3, 3, 4, 5, 3, 3, 4, 2\}$, to jak zdefiniować tę zmienną losową i jakie jest prawdopodobieństwo uzyskania poszczególnych ocen?

## Zadanie 2
Zakładając, że stosunek ocen bardzo dobrych, dobrych, dostatecznych i niedostatecznych ma się tak, jak $1:3:4:2$, wyznaczyć dla określonej tam zmiennej losowej $X$:

1. funkcję prawdopodobieństwa i jej wykres,
2. dystrybuantę i jej wykres,
3. prawdopodobieństwo $P(X < 3,5)$.

## Zadanie 3
Miesięczny koszt $u$ prowadzenia przykładowego laboratorium jest zależny od liczby $x$ zatrudnionych w nim pracowników. Załóżmy, że zależność ta jest postaci:

$$
u = 15000x + 10000\sqrt{x}
$$

Liczbę pracowników traktujemy jako zmienną losową $X$ o rozkładzie:

| $x_i$ | 2 | 3 | 4 | 5 |
| :--- | :--- | :--- | :--- | :--- |
| $p_i$ | 0,10 | 0,25 | 0,40 | 0,25 |

Wyznaczyć funkcję prawdopodobieństwa kosztów (zmienna losowa $U$).

## Zadanie 4
W wielu sytuacjach (np. w informatyce i elektronice) można przyjąć, że czas $X$ bezawaryjnej pracy badanego urządzenia jest zmienną losową ciągłą o gęstości:

$$
f(x) = \begin{cases}\frac{1}{\lambda} \exp\left(-\frac{x}{\lambda}\right) & \text{dla } x > 0 \\0 & \text{dla pozostałych } x\end{cases}
$$

(jest to tzw. rozkład wykładniczy). Niech parametr $\lambda = 10$ (np. godzin).

1. Obliczyć prawdopodobieństwo, że urządzenie będzie działać bezawaryjnie od 5 do 10 godzin: $P(5 \leqslant X \leqslant 10)$.
2. Wyznaczyć dystrybuantę tej zmiennej losowej.

## Zadanie 5
Dobrać tak stałe $A$ i $B$, by funkcja określona wzorem:

$$
F(x) = A + B \arctan x \quad \text{dla } -\infty < x < \infty
$$

była dystrybuantą pewnej zmiennej losowej ciągłej $X$. Następnie wyznaczyć gęstość tej zmiennej.

## Zadanie 6
Pewien mechanizm składa się z dwóch kół zębatych: dużego i małego. Warunki techniczne przy montażu urządzenia zostają naruszone, jeśli w obu kołach występują dodatnie odchylenia grubości zębów („plusowe”) lub w obu kołach ujemne („minusowe”). Rozważmy zero-jedynkowe zmienne losowe $X$ i $Y$:

* $X=1$, jeśli duże koło jest „plusowe”, $X=0$ jeśli „minusowe”.
* $Y=1$, jeśli małe koło jest „plusowe”, $Y=0$ jeśli „minusowe”.

Prawdopodobieństwa wystąpienia tych zdarzeń są następujące:
$P(X=0, Y=0) = P(X=1, Y=1) = \frac{1}{4}$ (awaria/zły montaż)
$P(X=0, Y=1) = P(X=1, Y=0) = \frac{1}{4}$ (dobry montaż)

Wyznaczyć tabelę rozkładu łącznego tej zmiennej dwuwymiarowej oraz obliczyć prawdopodobieństwo, że montaż jest prawidłowy.

## Zadanie 7
Dwuwymiarowa zmienna losowa $(X, Y)$ ma rozkład określony w tabelce:

| $Y \backslash X$ | 1 | 2 | 3 |
| :--- | :--- | :--- | :--- |
| **2** | 0,1 | 0,2 | 0,3 |
| **4** | 0,1 | 0,1 | 0,2 |

Wyznaczyć dystrybuantę rozkładu brzegowego zmiennej losowej $Y$.

## Zadanie 8
Dwie osoby z miasta A usiłują nawiązać połączenie telefoniczne z miastem B. Niech $X$ oznacza liczbę prób pierwszej osoby, a $Y$ – liczbę prób drugiej osoby. Zakładamy, że każda z osób łączy się niezależnie. Wiadomo, że rozkłady prawdopodobieństwa liczby prób dla obu osób są następujące:

* Dla osoby 1 ($X$): $P(X=1)=0,6$, $P(X=2)=0,4$
* Dla osoby 2 ($Y$): $P(Y=1)=0,5$, $P(Y=2)=0,5$

Wyznaczyć rozkład łączny zmiennej dwuwymiarowej $(X, Y)$ (tabelkę), zakładając niezależność prób obu osób.

## Zadanie 9
Dobrać tak stałą $c$, by funkcja:

$$
f(x, y) = \begin{cases}cxy & \text{dla } 0 \leqslant x \leqslant 2 \land 0 \leqslant y \leqslant 1 \\0 & \text{dla pozostałych } (x, y)\end{cases}
$$

była gęstością dwuwymiarowej zmiennej losowej $(X, Y)$.

## Zadanie 10
Dla funkcji gęstości z Zadania 9 (po wyznaczeniu $c$), wyznaczyć gęstości brzegowe $f_1(x)$ oraz $f_2(y)$. Sprawdzić, czy zmienne $X$ i $Y$ są niezależne (czy $f(x,y) = f_1(x) \cdot f_2(y)$).
