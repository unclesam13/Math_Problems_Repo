# LISTA ZADAŃ NR 11: Wstęp do teorii decyzji statystycznych

## Zadanie 1
Rozważamy partię towaru (np. procesorów), w której badamy wadliwość. Testujemy hipotezę $H_0: p = 0,02$ (partia dobra) przeciwko $H_1: p = 0,10$ (partia wadliwa). Zbudowano test, który odrzuca partię, jeśli liczba wadliwych sztuk w próbce o liczebności $n=50$ przekroczy $k=3$.

Obliczyć:

1. Prawdopodobieństwo błędu I rodzaju $\alpha$ (odrzucenie dobrej partii – ryzyko producenta).
2. Prawdopodobieństwo błędu II rodzaju $\beta$ (przyjęcie złej partii – ryzyko konsumenta).

## Zadanie 2
Dla testu z Zadania 1 wyznaczyć moc testu ($1-\beta$) dla kilku alternatywnych wartości parametru $p$. Sporządzić wykres krzywej mocy testu (funkcji mocy). Co ten wykres mówi nam o „czułości” algorytmu decyzyjnego na odchylenia od normy?

## Zadanie 3
Dla testu średniej $H_0: \mu = 100$ przy znanym $\sigma=5$ i $n=25$:

1. Wyznaczyć wzór na funkcję operacyjno-charakterystyczną (OC): $L(\mu) = P(\text{akceptacja } H_0 | \mu)$.
2. Jak zmiana liczebności próby na $n=100$ wpłynie na stromość tej krzywej (zdolność rozróżniania)?
Rozważamy test jednostronny przy poziomie istotności ( \alpha = 0.05 ).

## Zadanie 4

Chcemy skonstruować **jednostronny test średniej** dla populacji o rozkładzie normalnym 
z **znanym odchyleniem standardowym** $\sigma = 5$.

Testujemy hipotezy:

$$
H_0: \mu = \mu_0 
\quad \text{przeciwko} \quad
H_1: \mu = \mu_0 + 2.
$$

Wymagania bezpieczeństwa są następujące:

- Ryzyko błędu I rodzaju (odrzucenie normy, gdy jest spełniona) ma wynosić  $\alpha = 0.01$.
- Ryzyko błędu II rodzaju (przyjęcie normy, gdy rzeczywiste przesunięcie średniej wynosi 2 jednostki) ma nie przekraczać  
  $\beta = 0.05$.

Zakładając, że test oparty jest na statystyce

$$
Z = \frac{\bar{X} - \mu_0}{\sigma/\sqrt{n}},
$$

wyznaczyć **minimalną liczebność próby $n$**, która spełnia powyższe warunki.


## Zadanie 5
Wadliwość produkcji pewnych wyrobów wynosiła do tej pory 10% ($p_0=0,1$). Nowa technologia ma obniżyć wadliwość do 5% ($p_1=0,05$). Zamiast pobierać stałą próbkę, pobieramy elementy po jednym.

Skonstruować test sekwencyjny ilorazu wiarogodności (test Walda), ustalając ryzyka $\alpha=0,05$ i $\beta=0,10$.

1. Wyznaczyć proste decyzyjne (obszar akceptacji, odrzucenia i obszar kontynuacji badania).
2. Przedstawić procedurę w formie algorytmu (pseudokodu).

## Zadanie 6
Dla testu z Zadania 5, przypuśćmy, że wylosowano kolejno:
Dobry, Dobry, Zły, Dobry, Dobry, Dobry, Dobry...

Zaznaczyć te punkty na wykresie testu sekwencyjnego. W którym kroku (jeśli w ogóle) algorytm podejmie decyzję „Nowa technologia jest lepsza”?

## Zadanie 7
Jedną z zalet metod sekwencyjnych jest to, że średnio wymagają mniej danych niż testy klasyczne. Dla testu z Zadania 5 obliczyć oczekiwaną liczbę kroków (próbek) potrzebną do podjęcia decyzji (ASN), zakładając, że prawdziwa jest hipoteza $H_0$.

$$
E(n) \approx \frac{\alpha\ln A + (1-\alpha) \ln B}{E(z)}
$$

gdzie $A, B$ to progi decyzyjne.
Zmienne ( z ) oznacza logarytm ilorazu wiarygodności dla pojedynczej obserwacji.

## Zadanie 8
Automat produkuje detale o średnicy nominalnej $\mu_0$. Podejrzewamy, że maszyna się rozkalibrowała i średnia wzrosła do $\mu_1$. Odchylenie $\sigma$ jest znane.

Skonstruować test sekwencyjny weryfikujący $H_0: \mu = \mu_0$ przeciwko $H_1: \mu = \mu_1$. Napisać warunek „stop” dla tego algorytmu.
Przyjmujemy poziomy błędów ( \alpha = 0.05 ) oraz ( \beta = 0.10 ).

## Zadanie 9
Mamy dwie możliwe decyzje $d_1$ (wdrożenie systemu) i $d_2$ (brak wdrożenia) oraz dwa stany natury $\theta_1$ (system działa poprawnie) i $\theta_2$ (system ma błędy). Macierz strat (kosztów) wygląda następująco:

* Jeśli $d_1$ i $\theta_1$: Koszt = 0
* Jeśli $d_1$ i $\theta_2$: Koszt = 1000 (awaria u klienta)
* Jeśli $d_2$ i $\theta_1$: Koszt = 100 (utracony zysk)
* Jeśli $d_2$ i $\theta_2$: Koszt = 0

Jaką decyzję należy podjąć, stosując kryterium **Minimax** (minimalizacja maksymalnej straty)?

## Zadanie 10
Dla sytuacji z Zadania 9, załóżmy, że z wcześniejszych testów wiemy, iż prawdopodobieństwo wystąpienia błędów wynosi $P(\theta_2) = 0,05$. Obliczyć oczekiwaną stratę (ryzyko Bayesa) dla obu decyzji. Która decyzja jest optymalna w sensie bayesowskim?
