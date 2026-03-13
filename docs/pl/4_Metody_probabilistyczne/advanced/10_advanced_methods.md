# LISTA ZADAŃ NR 10: Zaawansowane metody statystyczne

## Zadanie 1 (Test serii - losowość próby)
Pobrano próbkę o liczności $n=20$ pewnej cechy $X$. Wartości uporządkowane według kolejności pobierania (w czasie) są następujące:

$$15.79, 15.84, 16.28, 16.33, 16.38, 16.41, 16.75,$$

$$16.87, 16.98, 17.00, 17.00, 17.35, 17.48, 17.56,$$

$$17.98, 18.12, 18.28, 18.28, 18.32, 18.53.$$

1. Wyznaczyć medianę $m_e$ tej próby.
2. Utworzyć ciąg symboli, wpisując $a$, gdy $x_i < m_e$ oraz $b$, gdy $x_i > m_e$ (elementy równe medianie pomijamy).
3. Zweryfikować hipotezę o losowości pobrania tej próby (brak trendu/cykliczności), stosując **test serii** na poziomie istotności $\alpha=0.05$.
*(Dane pochodzą z Zadania 3.87, Krysicki Cz. II, str. 143)*.

## Zadanie 2
Mamy dwa algorytmy sortowania (A i B). Wykonano po 5 niezależnych pomiarów czasu dla każdego z nich. Wyniki nie mają rozkładu normalnego (występują elementy odstające).

* Algorytm A: $12, 18, 14, 15, 13$
* Algorytm B: $19, 21, 23, 20, 22$

Zweryfikować hipotezę, że algorytm A jest szybszy od B, stosując test sumy rang (Manna-Whitneya-Wilcoxona).

## Zadanie 3
W tabeli (tablicy kontyngencji) zebrano dane o awariach w zależności od producenta sprzętu:

| Producent \ Typ awarii | Przegrzanie | Błąd dysku | Błąd pamięci |
| :--- | :---: | :---: | :---: |
| **Producent X** | 20 | 10 | 15 |
| **Producent Y** | 30 | 50 | 25 |

Sprawdzić na poziomie istotności $\alpha=0.05$, czy rodzaj awarii zależy od producenta.

## Zadanie 4
Testujemy wydajność 3 różnych frameworków (X, Y, Z). Ponieważ dane są mocno asymetryczne, zamiast klasycznej analizy wariancji (ANOVA), stosujemy test nieparametryczny Kruskala-Wallisa.

**Tabela wyników wydajności (punkty w benchmarku):**

| Framework X | Framework Y | Framework Z |
| :---: | :---: | :---: |
| 45 | 52 | 68 |
| 48 | 55 | 70 |
| 42 | 58 | 75 |
| 50 | 60 | 72 |
| 46 | 54 | 78 |
*(Liczebności prób: $n_x=5, n_y=5, n_z=5$.)*

Dla danych rankingowych z tabeli zweryfikować hipotezę, że wszystkie frameworki mają taką samą medianę wydajności.

## Zadanie 5
Mamy dwa zbiory danych o ruchu sieciowym (przed i po wdrożeniu firewalla). Chcemy sprawdzić, czy **cały rozkład** (nie tylko średnia) uległ zmianie.

**Wyniki pomiarów opóźnienia pakietów (w ms):**

**Przed wdrożeniem ($n=10$):**

$$12, 15, 18, 14, 13, 16, 12, 19, 15, 17$$

*(Dane uporządkowane: 12, 12, 13, 14, 15, 15, 16, 17, 18, 19)*

**Po wdrożeniu ($m=10$):**

$$18, 22, 20, 19, 21, 25, 23, 20, 24, 28$$

*(Dane uporządkowane: 18, 19, 20, 20, 21, 22, 23, 24, 25, 28)*

Na podstawie dystrybuant empirycznych obu prób obliczyć statystykę $D_{n,m}$ i zweryfikować hipotezę o identyczności rozkładów (test Kołmogorowa-Smirnowa).
Hipotezę zweryfikować przy poziomie istotności ( \alpha = 0.05 ).

## Zadanie 6
Badamy czas kompilacji kodu ($Y$) w zależności od liczby plików ($X_1$) i liczby linii kodu w pliku ($X_2$).

**Dane z 8 projektów programistycznych:**

| Projekt | Liczba plików ($x_1$) | Tysiące linii kodu ($x_2$) | Czas kompilacji w sek. ($y$) |
| :---: | :---: | :---: | :---: |
| 1 | 2 | 5 | 12 |
| 2 | 4 | 10 | 25 |
| 3 | 3 | 8 | 19 |
| 4 | 6 | 15 | 40 |
| 5 | 8 | 20 | 55 |
| 6 | 2 | 4 | 10 |
| 7 | 5 | 12 | 32 |
| 8 | 7 | 18 | 48 |

Dla podanych danych wyznaczyć równanie płaszczyzny regresji:

$$
y = a x_1 + b x_2 + c
$$

## Zadanie 7
Liczba tranzystorów w procesorach rośnie wykładniczo: $y = a \cdot e^{bx}$. Mając dane historyczne, sprowadzić to zagadnienie do regresji liniowej poprzez logarytmowanie ($\ln y = \ln a + bx$) i wyznaczyć parametry wzrostu.

**Dane historyczne rozwoju procesorów (uproszczone):**

| Rok ($t$) | Zmienna czasowa $x = t - 1970$ | Liczba tranzystorów ($y$) |
| :---: | :---: | :---: |
| 1970 | 0 | 2 000 |
| 1975 | 5 | 8 000 |
| 1980 | 10 | 30 000 |
| 1985 | 15 | 120 000 |
| 1990 | 20 | 500 000 |

## Zadanie 8
Produkcja procesorów generuje pewien procent braków. Zamiast pobierać stałą próbkę 100 sztuk, pobieramy sztuki jedna po drugiej. Po każdym pobraniu decydujemy: „partia dobra”, „partia zła” lub „pobieramy dalej”.

Skonstruować test sekwencyjny (test Walda) dla weryfikacji hipotezy $p=0.01$ przeciw $p=0.10$. Przyjąć ryzyko błędu I rodzaju $\alpha = 0,05$ oraz ryzyko błędu II rodzaju $\beta = 0,10$.

## Zadanie 9
Dla próby prostej $x_1, ..., x_n$ z rozkładu wykładniczego (czas bezawaryjnej pracy) o gęstości $f(x) = \frac{1}{\lambda} \exp\left(-\frac{x}{\lambda}\right)$, gdzie $\lambda$ jest wartością oczekiwaną, wyznaczyć estymator parametru $\lambda$ metodą największej wiarygodności (MNW).

## Zadanie 10
Mamy 3 serwery. Chcemy sprawdzić, czy działają tak samo stabilnie (czy mają taką samą wariancję czasów odpowiedzi), zanim porównamy ich średnie czasy. Wariancje z prób wynoszą: $s_1^2=1.4, \ s_2^2=1.8, \ s_3^2=1.2$.

Liczebności prób dla podanych wariancji są następujące:
* Serwer 1 ($s_1^2 = 1.4$): $n_1 = 20$
* Serwer 2 ($s_2^2 = 1.8$): $n_2 = 20$
* Serwer 3 ($s_3^2 = 1.2$): $n_3 = 20$

Zweryfikować hipotezę $H_0: \sigma_1^2 = \sigma_2^2 = \sigma_3^2$ (np. testem Bartletta) przy $\alpha=0.05$.
