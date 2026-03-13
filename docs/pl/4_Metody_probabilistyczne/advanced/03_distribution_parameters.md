# LISTA ZADAŃ NR 3: Parametry rozkładu zmiennych losowych
(Wartość oczekiwana, wariancja, momenty, korelacja)

## Zadanie 1
Dla zmiennej losowej $X$ o funkcji prawdopodobieństwa danej tabelką:

| $x_i$ | -2 | 2 | 4 |
| :--- | :--- | :--- | :--- |
| $p_i$ | 0,5 | 0,3 | 0,2 |

Wyznaczyć:

1. Wartość oczekiwaną $E(X)$ (średnią).
2. Wariancję $D^2(X)$ (korzystając ze wzoru $D^2(X) = E(X^2) - (EX)^2$).
3. Odchylenie standardowe $\sigma$.
4. Medianę $x_{0,5}$ (wartość środkową).

## Zadanie 2
Miesięczny koszt $U$ prowadzenia pewnego systemu zależy od liczby $X$ aktywnych użytkowników (pracowników) według wzoru:

$$
U = 15000X + 10000\sqrt{X}
$$

Liczba pracowników $X$ jest zmienną losową o rozkładzie:

| $x_i$ | 2 | 3 | 4 | 5 |
| :--- | :--- | :--- | :--- | :--- |
| $p_i$ | 0,10 | 0,25 | 0,40 | 0,25 |

Obliczyć przewidywany średni miesięczny koszt, czyli wartość oczekiwaną zmiennej $U$.

*Wskazówka: Oblicz $u_i$ dla każdego $x_i$, a następnie zastosuj wzór na wartość oczekiwaną.*

## Zadanie 3
Zmienna losowa $X$ (np. błąd pomiarowy) ma rozkład o gęstości:

$$
f(x) = \begin{cases}6x(1-x) & \text{dla } 0 < x < 1 \\0 & \text{dla pozostałych } x\end{cases}
$$

Obliczyć wartość przeciętną (oczekiwaną) oraz wariancję tej zmiennej. Następnie obliczyć wariancję zmiennej liniowo zależnej $Y = 2X - 1$ (skorzystać z własności wariancji: $D^2(aX+b) = a^2 D^2(X)$).

## Zadanie 4
Zmienna losowa $X$ ma rozkład o gęstości:

$$
f(x) = \begin{cases}\frac{1}{2}x & \text{dla } 0 \leqslant x \leqslant 2 \\0 & \text{poza tym}\end{cases}
$$

Wyznaczyć modę (wartość, dla której gęstość jest największa) oraz medianę (wartość, która dzieli pole pod wykresem gęstości na dwie równe połowy).

## Zadanie 5
Wzrost ludzi w pewnej grupie jest zmienną losową $X$ o średniej $EX = 170$ cm i odchyleniu $\sigma_X = 5$ cm. Masa tych ludzi to zmienna $Y$ o średniej $EY = 65$ kg i odchyleniu $\sigma_Y = 5$ kg.

Która cecha (wzrost czy waga) jest bardziej "stabilna" (ma mniejszy rozrzut względny)?

*Wskazówka: Oblicz współczynnik zmienności $v = \frac{\sigma}{EX}$ dla obu zmiennych.*

## Zadanie 6
Prawdopodobieństwo nieprzekroczenia w ciągu doby limitu zużycia energii elektrycznej przez pewien zakład wynosi $p=0,8$. Obserwujemy ten zakład przez $n=5$ dni. Niech $X$ oznacza liczbę dni, w których nie przekroczono limitu.

1. Jaki to typ rozkładu? Podać wzór na prawdopodobieństwo $P(X=k)$.
2. Obliczyć wartość oczekiwaną i wariancję zmiennej $X$, korzystając z gotowych wzorów dla tego rozkładu ($EX=np$, $D^2X=npq$).

## Zadanie 7
Czas (w minutach) między kolejnymi zgłoszeniami abonentów w centrali telefonicznej jest zmienną losową o rozkładzie wykładniczym z parametrem (wartością oczekiwaną) $\lambda = 2$.

1. Obliczyć średni czas oczekiwania na zgłoszenie ($EX$).
2. Obliczyć prawdopodobieństwo, że czas między zgłoszeniami będzie krótszy niż 3 minuty ($P(X<3)$).

## Zadanie 8
Automat produkuje odważniki. Błędy pomiarów masy mają rozkład normalny o wartości oczekiwanej $\mu=0$ g i odchyleniu standardowym $\sigma=0,01$ g. Obliczyć prawdopodobieństwo, że błąd pomiaru (co do modułu) nie przekroczy $0,02$ g.

*Wskazówka: Skorzystać z dystrybuanty standaryzowanego rozkładu normalnego $\Phi(u)$. Zauważ, że $P(|X|<a) = P(-a < X < a)$.*

## Zadanie 9
Dana jest dwuwymiarowa zmienna losowa $(X, Y)$ o rozkładzie podanym w tabeli (reprezentująca np. wyniki testów w dwóch różnych momentach czasu):

| $y_k \backslash x_i$ | 8 | 9 | 10 | 11 |
| :--- | :--- | :--- | :--- | :--- |
| **1,2** | 0,10 | 0,04 | 0 | 0 |
| **1,3** | 0,05 | 0,11 | 0,20 | 0 |
| **1,4** | 0 | 0,10 | 0,15 | 0,10 |
| **1,5** | 0 | 0 | 0,05 | 0,10 |

Obliczyć współczynnik korelacji liniowej $\rho$ między zmiennymi $X$ i $Y$.

*Wskazówka: Należy obliczyć kolejno: średnie $EX, EY$, wariancje $D^2X, D^2Y$ oraz moment mieszany $E(XY) = \sum x_i y_k p_{ik}$. Kowariancja to $cov(X,Y) = E(XY) - EX \cdot EY$.*

## Zadanie 10

Niech $X$ i $Y$ będą niezależnymi zmiennymi losowymi o zerowych wartościach oczekiwanych ($EX=0, EY=0$). Wykazać, że zachodzi równość:

$$E(X^3 Y) = E(X^3)E(Y)$$

Czy zmienna $Z = X^3 Y$ ma wartość oczekiwaną równą 0? Co to oznacza w kontekście sygnałów losowych (szum)?