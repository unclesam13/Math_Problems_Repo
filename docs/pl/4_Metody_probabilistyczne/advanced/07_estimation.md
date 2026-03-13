# LISTA ZADAŃ NR 7: Estymacja punktowa i przedziałowa

## Zadanie 1
Znaleźć przedział ufności dla nieznanej wartości przeciętnej $\mu$ populacji, w przypadku gdy $\sigma$ jest znane, na podstawie $n$-elementowej próby prostej $X_1, ..., X_n$.

Dane: Z populacji o odchyleniu standardowym $\sigma=0,14$ pobrano próbkę $n=100$ elementową (np. pomiarów napięcia na procesorze). Średnia z próby wyniosła $\bar{x}=2,5$. Wyznaczyć 95%-owy przedział ufności dla średniej (przyjąć $1-\alpha = 0,95$, co daje $u_{\alpha} = 1,96$).

## Zadanie 2
Zmierzono wytrzymałość 10 losowo wybranych elementów konstrukcji (lub np. czas pracy na baterii 10 laptopów). Otrzymano wyniki: $383, 284, 339, 340, 305, 386, 378, 335, 344, 346$.

Zakładając, że rozkład cechy jest normalny, wyznaczyć 95%-owy przedział ufności dla średniej wytrzymałości.

*Wskazówka: Ponieważ $n=10$ jest małe ($n<30$) i nie znamy $\sigma$, należy obliczyć $s$ z próby i skorzystać z rozkładu t-Studenta*.

## Zadanie 3
W celu wyznaczenia ładunku elektronu wykonano 26 pomiarów metodą Millikana. Otrzymano średnią $\bar{x} = 1,574 \cdot 10^{-19}$ oraz odchylenie standardowe $s = 0,043 \cdot 10^{-19}$.

Wyznaczyć przedział ufności dla średniego ładunku na poziomie ufności $0,99$.

## Zadanie 4
Z populacji włókien bawełny pobrano 300-elementową próbkę i zmierzono ich długości. Obliczono średnią $\bar{x}=27,43$ mm oraz wariancję $s^2=51,598$.

Znaleźć 95%-ową realizację przedziału ufności dla nieznanej wartości przeciętnej długości włókna.

*Wskazówka: Przy tak dużym $n$ ($n=300$), rozkład t-Studenta jest praktycznie tożsamy z rozkładem normalnym, więc można użyć statystyki $u_{\alpha}$*.

## Zadanie 5
Wykonuje się pomiary głębokości morza (lub np. opóźnienia w sieci) w pewnym określonym miejscu.

Ilu niezależnych pomiarów należy dokonać, aby przyjąć z poziomem ufności $0,95$, że błąd bezwzględny szacowania średniej nie przekroczy $10$ m, jeśli rozkład błędów jest normalny o wariancji $\sigma^2 = 180$ $m^2$? 

## Zadanie 6
Spośród 120 wylosowanych pracowników pewnego zakładu, 17 nie wykonywało normy wydajności pracy (w IT: 17 na 120 serwerów nie spełniło wymogów SLA).

Wyznaczyć 95%-ową realizację przedziału ufności dla frakcji $p$ pracowników niewykonujących normy w całym zakładzie.

## Zadanie 7
Wykonano 15 pomiarów czasu likwidowania zrywów przędzy na krosnach. Obliczono wariancję z próby $s^2 = 134,2$. Zakładając, że czas ten ma rozkład normalny, wyznaczyć 90%-owy przedział ufności dla wariancji $\sigma^2$ oraz odchylenia standardowego $\sigma$. Wariancja próbkowa ( s^2 ) została obliczona z dzieleniem przez ( n-1 ).

*Wskazówka: Należy skorzystać z tablic rozkładu chi-kwadrat ($\chi^2$)*.

## Zadanie 8
Dla pewnej cechy o rozkładzie normalnym wylosowano dwie próbki:

* Próbka 1: $n=25$, średnia $\bar{x}=15$, odchylenie $s=5$.
* Próbka 2: $n=100$, średnia $\bar{x}=15$, odchylenie $s=5$.

Obliczyć długości 95%-owych przedziałów ufności dla obu prób. Jak czterokrotne zwiększenie liczebności próby wpływa na precyzję (szerokość przedziału)? 

## Zadanie 9
Dana jest próbka prosta o liczebności $n=5$: $\{2, 4, 6, 8, 10\}$. Obliczyć wartość estymatora nieobciążonego wartości oczekiwanej ($\bar{x}$) oraz estymatora nieobciążonego wariancji ($s^2$).

Wyjaśnić, dlaczego przy wariancji dzielimy przez $n-1$, a nie przez $n$.

## Zadanie 10
Zbadano procentową zawartość skrobi w 80 ziemniakach. Średnia z próby wyniosła $\bar{x}=17,525\%$, a odchylenie standardowe $s=1,84\%$.

Przyjmując poziom ufności 0,95, oszacować średnią zawartość skrobi w całej partii.
