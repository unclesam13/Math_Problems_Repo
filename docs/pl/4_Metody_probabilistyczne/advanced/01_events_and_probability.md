# LISTA ZADAŃ NR 1: Zdarzenia losowe i prawdopodobieństwo

## Zadanie 1
Niech przestrzeń $\Omega$ zdarzeń elementarnych doświadczenia składa się z pięciu zdarzeń elementarnych $\omega_i$: $\Omega=\{\omega_1, \omega_2, \omega_3, \omega_4, \omega_5\}$. Określamy zdarzenia: $A=\{\omega_1, \omega_3, \omega_5\}$, $B=\{\omega_2, \omega_3, \omega_4\}$.

Znaleźć zdarzenia:

1. $A \cup B$ (suma zdarzeń)
2. $A \cap B$ (iloczyn zdarzeń)
3. $B \backslash A$ (różnica zdarzeń)
4. $A \backslash B$

## Zadanie 2
Rozważamy układ elektryczny, w którym element $a_1$ połączony jest szeregowo z blokiem składającym się z dwóch elementów $a_2$ i $a_3$ połączonych równolegle. Niech $A_i, i=1, 2, 3$, oznacza zdarzenie „element $a_i$ będzie sprawny w czasie $t$”.

Za pomocą działań na zdarzeniach $A_i$ oraz symboli sumy ($\cup$) i iloczynu ($\cap$) opisać zdarzenie $A$: „w odcinku czasu $t$ przepływ prądu przez układ nie ulegnie przerwaniu”.

## Zadanie 3
Osoba $X$ wykonuje pewną pracę w ciągu 4, 5 albo 6 godzin i może popełnić przy tym 0, 1 albo 2 błędy. Zakładając jednakowe prawdopodobieństwo dla każdego z 9 możliwych zdarzeń elementarnych (par: czas, liczba błędów), znaleźć prawdopodobieństwo następujących zdarzeń:

1. Praca zostanie wykonana w ciągu 4 godzin.
2. Praca zostanie wykonana bezbłędnie w czasie 6 godzin.
3. Praca zostanie wykonana w czasie co najwyżej 5 godzin.
4. Praca zostanie wykonana w czasie co najwyżej 5 godzin i najwyżej z jednym błędem.

## Zadanie 4
Fragment sieci elektrycznej składa się z dwóch elementów połączonych równolegle: $a_1$ i $a_2$. Niech $A_i, i=1, 2$, oznacza zdarzenie, że element $a_i$ będzie sprawny co najmniej przez czas $t$.

Obliczyć prawdopodobieństwo ciągłego przepływu prądu przez ten układ co najmniej przez czas $t$, jeżeli wiadomo, że $P(A_1)=P(A_2)=p$ oraz prawdopodobieństwo jednoczesnej sprawności obu elementów wynosi $P(A_1 \cap A_2)=p^2$.

## Zadanie 5
Rozpatrujemy ilość (w $dm^3$) wody, jaką może mieć do przeprowadzenia w ciągu sekundy betonowy przepust. Dotychczasowe obserwacje pozwalają przyjąć, że:

* Prawdopodobieństwo, że ilość wody przyjmie wartość z przedziału $\langle 125, 250 \rangle$ wynosi $P(A) = 0,6$.
* Prawdopodobieństwo, że ilość wody przyjmie wartość z przedziału $(200, 300\rangle$ wynosi $P(B) = 0,7$.
* Prawdopodobieństwo sumy tych zdarzeń wynosi $P(A \cup B)=0,8$.

Obliczyć prawdopodobieństwo:

1. $P(A')$ (zdarzenie przeciwne do A)
2. $P(A \cap B)$ (wspólna część przedziałów)
3. $P(A' \cap B')$ (ilość wody nie mieści się w żadnym z tych przedziałów)

## Zadanie 6
Na przenośnik taśmowy trafiają jednakowe produkty wytwarzane przez 2 automaty. Stosunek ilościowy produkcji pierwszego automatu do produkcji drugiego wynosi $3:2$. Pierwszy automat wytwarza średnio $65\%$ produktów w pierwszym gatunku, drugi zaś – $85\%$.

1. Spośród produktów na przenośniku pobieramy losowo jeden produkt. Obliczyć prawdopodobieństwo, że będzie to produkt pierwszego gatunku (zastosować wzór na prawdopodobieństwo całkowite).
2. Losowo pobrany produkt okazał się pierwszej jakości. Obliczyć prawdopodobieństwo, że został wyprodukowany przez pierwszy automat (zastosować wzór Bayesa).

## Zadanie 7
Na linii łączności nadaje się dwa rodzaje sygnałów w postaci kodowych kombinacji 111 albo 000 z prawdopodobieństwami a priori odpowiednio $0,65$ i $0,35$. Sygnały podlegają losowym zakłóceniom, w rezultacie czego symbol 1 może być odebrany jako 0 z prawdopodobieństwem $0,2$ i z takim samym prawdopodobieństwem symbol 0 może być odebrany jako 1. Zakładamy, że symbole 1 i 0 ulegają zakłóceniom niezależnie jeden od drugiego.

Obliczyć prawdopodobieństwo odebrania sygnału:

1. 111
2. 000
3. 010

## Zadanie 8
Kodowa informacja składa się z siedmiu impulsów postaci $A, B, C$ w ilościach: cztery impulsy $A$, dwa impulsy $B$ i jeden impuls $C$. Zakładając losowy układ impulsów, znaleźć prawdopodobieństwo tego, że:

1. pierwszym odebranym impulsem będzie $A$,
2. pierwszym odebranym impulsem będzie $A$ albo $C$,
3. dwoma pierwszymi impulsami będą kolejno $A$ i $C$.

## Zadanie 9
Pewien towar produkują 3 zakłady. Prawdopodobieństwo wyprodukowania przez te zakłady towaru pierwszej jakości wynosi odpowiednio $0,97$; $0,90$; $0,86$.

Znaleźć prawdopodobieństwo tego, że losowo wzięta sztuka towaru — spośród trzech sztuk pochodzących (po jednej) z różnych zakładów — jest pierwszej jakości.

## Zadanie 10
Kanałem łączności nadaje się tylko 3 rodzaje ciągów liter: $AAAA$, $BBBB$, $CCCC$ odpowiednio z prawdopodobieństwami $0,4$; $0,3$; $0,3$. Litery te (sygnały) podlegają niezależnie losowym zakłóceniom (przekłamaniom), w rezultacie czego np. litera $A$ może być odebrana jako $B$ albo $C$. Prawdopodobieństwa poprawnego przesłania albo przekłamania pojedynczej litery podaje tablica:

| Nadany \ Odebrany | A | B | C |
| :--- | :--- | :--- | :--- |
| **A** | 0,8 | 0,1 | 0,1 |
| **B** | 0,1 | 0,8 | 0,1 |
| **C** | 0,1 | 0,1 | 0,8 |

Znaleźć prawdopodobieństwo odebrania na wyjściu sygnału:

1. $AAAA$
2. $ACAA$