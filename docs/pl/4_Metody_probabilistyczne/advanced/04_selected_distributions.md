# LISTA ZADAŃ NR 4: Wybrane rozkłady zmiennych losowych

## Zadanie 1
Prawdopodobieństwo awarii aparatury doświadczalnej w jednym doświadczeniu wynosi $p=0,02$. Doświadczenia można przeprowadzać dowolną liczbę razy. Obliczyć prawdopodobieństwo, że druga z kolei awaria:

1. zdarzy się przy dziesiątym doświadczeniu,
2. nie zdarzy się w pierwszych dziesięciu doświadczeniach.

## Zadanie 2
Prawdopodobieństwo, że produkt poddawany próbie nie wytrzyma tej próby wynosi $p=0,01$. Obliczyć prawdopodobieństwo, że wśród 200 takich produktów (niezależnie poddanych próbie) co najwyżej 2 nie wytrzymają próby.

*Wskazówka: Ponieważ $n=200$ jest duże, a $p=0,01$ małe, należy zastosować przybliżenie rozkładem Poissona z parametrem $\lambda = np$.*

## Zadanie 3
Czas (w minutach) między kolejnymi zgłoszeniami abonentów w pewnej centrali telefonicznej jest zmienną losową o rozkładzie wykładniczym z parametrem (wartością oczekiwaną) $\lambda=2$. Obliczyć średni czas między kolejnymi zgłoszeniami oraz prawdopodobieństwo, że przed upływem 3 minut nastąpi zgłoszenie.

## Zadanie 4
Czas bezawaryjnej pracy $X$ pewnego urządzenia ma rozkład wykładniczy z parametrem (wartością oczekiwaną) $\lambda=5$. Obliczyć:

1. wartość przeciętną bezawaryjnego czasu pracy urządzenia,
2. medianę,
3. prawdopodobieństwo, że bezawaryjny czas pracy urządzenia wynosi co najmniej 5 godzin.

## Zadanie 5
Odstęp między kolejnymi podziałkami skali stopera wynosi $0,1$ s. Czas na tym stoperze odczytuje się z dokładnością do całej podziałki. Zakładając jednostajny rozkład błędu odczytu czasu, obliczyć prawdopodobieństwo, że zmierzono czas z błędem przekraczającym $0,02$ s.

*Wskazówka: Gęstość rozkładu jednostajnego jest stała w przedziale $(-0,05; 0,05)$.*

## Zadanie 6
Automat produkuje odważniki 10-gramowe. Błędy pomiarów masy tych odważników mają rozkład normalny o wartości oczekiwanej $\mu=0$ g i odchyleniu standardowym $\sigma=0,01$ g. Znaleźć prawdopodobieństwo tego, że pomiar masy będzie przeprowadzony z błędem nie przekraczającym $0,02$ g.

## Zadanie 7
Niech zmienna losowa $X$ ma rozkład $N(\mu, \sigma)$. Obliczyć prawdopodobieństwo $P(|X-\mu| < k\sigma)$ dla:

1. $k=1,96$ (poziom ufności 0,95),
2. $k=2,58$ (poziom ufności 0,99).

## Zadanie 8
Pewien przyrząd pomiarowy robi błąd systematyczny $1$ m w stronę zawyżenia pomiaru i błąd losowy o rozkładzie $N(0; 0,5)$.

1. Obliczyć wartość przeciętną błędu pomiaru.
2. Wyznaczyć prawdopodobieństwo tego, że błąd z jakim mierzone jest badane przedmioty nie przekracza $2$ m.

## Zadanie 9
Wytrzymałość stalowych lin pochodzących z produkcji masowej jest zmienną losową o rozkładzie $N(1000 \text{ kg/cm}^2, 50 \text{ kg/cm}^2)$. Obliczyć jaki procent lin ma wytrzymałość mniejszą od $900 \text{ kg/cm}^2$.

## Zadanie 10
Wyznaczyć i naszkicować dystrybuantę rozkładu Rayleigha, którego gęstość dana jest wzorem:

$$
f(x) = \begin{cases} \frac{2}{\lambda} x \exp(-\frac{x^2}{\lambda}) & \text{dla } x > 0 \\ 0 & \text{dla } x \leqslant 0 \end{cases}
$$

(gdzie parametr lambda jest związany z wariancją szumu)

Następnie obliczyć medianę tego rozkładu.

*Wskazówka: Rozkład ten stosuje się często w telekomunikacji do modelowania zaników sygnału.*