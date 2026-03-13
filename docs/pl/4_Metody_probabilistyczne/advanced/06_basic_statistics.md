# LISTA ZADAŃ NR 6: Podstawowe statystyki i ich rozkłady

## Zadanie 1 (Szereg rozdzielczy)
Z populacji generalnej pobrano $n=50$-elementową próbkę (wyniki pomiarów). Otrzymano następujące wyniki surowe:

$$3.6, 5.0, 4.0, 4.7, 5.2, 5.9, 4.5, 5.3, 5.5, 3.9,$$

$$5.6, 3.5, 5.4, 5.2, 4.1, 5.0, 3.1, 5.8, 4.8, 4.4,$$

$$4.6, 5.1, 4.7, 3.0, 5.5, 6.1, 3.8, 4.9, 5.6, 6.1,$$

$$5.9, 4.2, 6.4, 5.3, 4.5, 4.9, 4.0, 5.2, 3.3, 5.4,$$

$$4.7, 6.4, 5.1, 3.4, 5.2, 6.2, 4.4, 4.3, 5.8, 3.7.$$

Na podstawie tych danych:

1. Sporządzić szereg rozdzielczy, przyjmując liczbę klas $k=7$.
2. Wyznaczyć rozstęp $R$ oraz długość klasy $b$.

## Zadanie 2 (Miary położenia)
Dla próbki z Zadania 1, po uporządkowaniu wyników rosnąco wyznaczyć:

1. **Medianę** ($m_e$) – wartość środkową.
2. **Modę** ($m_o$) – wartość najczęstszą.
3. Porównać, czy w tym przypadku $m_e \approx \bar{x}$ (gdzie $\bar{x} = 4.844$).


## Zadanie 3
W pewnym eksperymencie chemicznym (lub procesie produkcji procesorów) badano ilość czystej substancji. Dla 5 pomiarów otrzymano wyniki: $3.5, 3.4, 2.1, 5.4, 1.1$.

Obliczyć:

1. Średnią arytmetyczną z próby $\bar{x}$.
2. Wariancję z próby $s^2$ (używając wzoru dla małej próby).
3. Odchylenie standardowe $s$.

## Zadanie 4
Pojazd (lub pakiet danych w sieci) przebył drogę złożoną z trzech odcinków o tej samej długości, ale z różnymi prędkościami: $v_1=50, v_2=60, v_3=70$ km/h. Obliczyć średnią prędkość na całej trasie.

*Wskazówka: Należy użyć średniej harmonicznej, a nie arytmetycznej.*

## Zadanie 5
Dane są dwie sześcioelementowe próbki (np. czasy dostępu do dwóch różnych dysków):

* Próbka I: $80, 40, 40, 80, 40, 80$
* Próbka II: $40, 80, 120, 80, 120, 40$

Obliczyć współczynniki zmienności $v = \frac{s}{\bar{x}}$ dla obu próbek. Który dysk działa bardziej stabilnie (ma mniejszy rozrzut względny)?

## Zadanie 6
Z populacji o rozkładzie normalnym $N(\mu, \sigma)$ pobrano próbę o liczebności 36. Średnia z próby wyniosła $\bar{x} = 150$, a odchylenie standardowe populacji jest znane i wynosi $\sigma = 12$. Wyznaczyć dwustronny przedział ufności dla średniej w populacji $\mu$ na poziomie ufności 0.95. W tym celu należy wykorzystać fakt, że statystyka:

$$
U = \frac{\bar{X} - \mu}{\sigma} \sqrt{n}
$$

ma rozkład $N(0,1)$.

## Zadanie 7
Wylosowano małą próbkę (10 elementów) z populacji o rozkładzie normalnym. Ponieważ nie znamy odchylenia standardowego populacji $\sigma$, musimy użyć odchylenia z próby $S$ (liczonego ze wzoru z dzieleniem przez $n$). Statystyka:

$$
t = \frac{\bar{X} - \mu}{S} \sqrt{n-1}
$$

podlega rozkładowi t-Studenta. Odczytać z tablic wartości krytyczne do zbudowania dwustronnego przedziału ufności na poziomie ufności 0.95.

## Zadanie 8
Dla badania wariancji (rozrzutu) próby stosuje się statystykę:

$$
\chi^2 = \frac{nS^2}{\sigma^2}
$$

> *Uwaga: Symbol $S^2$ oznacza wariancję z próby liczoną ze wzoru z dzieleniem przez $n$ (zgodnie z definicją w podręczniku Krysickiego).*

Wykonano 15 pomiarów. Odczytać z tablic rozkładu chi-kwadrat wartości krytyczne odcinające symetryczne obszary w ogonach rozkładu (po 5% prawdopodobieństwa na każdy ogon), między którymi z prawdopodobieństwem 0.90 znajdzie się ta statystyka.

## Zadanie 9
Dana jest 3-elementowa populacja o wartościach {2, 4, 6}. Wypisać wszystkie możliwe 2-elementowe próby (przy losowaniu ze zwracaniem), obliczyć średnią dla każdej z nich, a następnie pokazać, że wartość oczekiwana tych średnich z prób jest równa średniej całej populacji. W ten sposób wykażesz liczbowo, że średnia z próby jest estymatorem nieobciążonym.

## Zadanie 10
Dla małej próbki: $0.18, 0.56, 0.87, 1.37, 2.46$ wyznaczyć wartości dystrybuanty empirycznej $S_n(x)$.