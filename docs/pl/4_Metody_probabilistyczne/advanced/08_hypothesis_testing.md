# LISTA ZADAŃ NR 8: Weryfikacja hipotez statystycznych

## Zadanie 1
W celu ustalenia, czy dotychczasowa norma okresu użytkowania pewnych podzespołów elektronicznych wynosząca 150 dni nie jest zbyt wysoka, zbadano losowo 65 podzespołów pracujących w normalnych warunkach. Otrzymano średnią długość okresu użytkowania $\bar{x} = 139$ dni oraz odchylenie standardowe $s = 9,8$ dni.

Na poziomie istotności $\alpha=0,01$ zweryfikować hipotezę, że norma jest zawyżona (Hipoteza $H_0: m = 150$ przeciw $H_1: m < 150$).

## Zadanie 2
Porównujemy dwa algorytmy lub dwa urządzenia (np. wagi). Dla pierwszej serii $n_1=10$ pomiarów otrzymano średnią $\bar{x}_1 = 5,25$ i wariancję $s_1^2 = 0,06$. Dla drugiej serii $n_2=5$ pomiarów otrzymano $\bar{x}_2 = 5,58$ i wariancję $s_2^2 = 0,07$.

Zakładając, że wariancje są równe (choć nieznane), zweryfikować na poziomie $\alpha=0,05$ hipotezę, że obie serie pochodzą z populacji o tej samej średniej ($H_0: m_1 = m_2$).

## Zadanie 3
Zbadano rozrzut opóźnień (jitter) w sieci. Oddano 50 strzałów (pomiarów) do tarczy. Okazało się, że wariancja tych odległości jest równa $s^2 = 107,3$.

Zakładając, że rozkład odległości jest normalny, zweryfikować na poziomie $\alpha=0,05$ hipotezę, że wariancja $\sigma^2 = 100$, wobec hipotezy alternatywnej $\sigma^2 > 100$.

## Zadanie 4
W pewnym przedsiębiorstwie (np. serwerowni) opracowano dwie metody obsługi zleceń. Aby sprawdzić, czy obie metody dają tak samo stabilne wyniki (jednakowe wariancje), wykonano pomiary.

* Metoda 1: $n_1=5$, wariancja $s_1^2 = 0,248$.
* Metoda 2: $n_2=5$, wariancja $s_2^2 = 2,172$.

Na poziomie $\alpha=0,05$ zweryfikować hipotezę $H_0: \sigma_1^2 = \sigma_2^2$.

## Zadanie 5
Wadliwość produkcji pewnych wyrobów (np. błędnych pakietów danych) wynosiła 10%. Wprowadzono nową technologię. Wylosowano próbkę $n=900$ sztuk i znaleziono w niej 50 sztuk wadliwych.

Czy na poziomie istotności $\alpha=0,05$ można twierdzić, że nowa technologia zmniejszyła wadliwość?

## Zadanie 6
Obserwowano pod mikroskopem liczbę komórek drożdży w 400 kwadratach (w informatyce: liczba zapytań do serwera w jednostce czasu). Wyniki pogrupowano w poniższej tabeli:

| Liczba komórek ($x_i$) | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Liczba kwadratów ($n_i$) | 20 | 43 | 53 | 86 | 70 | 54 | 37 | 21 | 10 | 4 | 2 |

Na poziomie $\alpha=0,05$ zweryfikować hipotezę, że rozkład liczby komórek jest rozkładem Poissona.

## Zadanie 7
Wynikami 5-elementowej próby są: $0,18; 0,56; 0,87; 1,37; 2,46$.

Na poziomie istotności $\alpha=0,05$ zweryfikować hipotezę, że próba ta pochodzi z populacji o rozkładzie wykładniczym $f(x) = e^{-x}$ dla $x>0$.

## Zadanie 8
Pobrano próbkę $n=20$ pewnej cechy (np. czas reakcji aplikacji). Wartości uporządkowano rosnąco:

$$121.3, 124.1, 128.8, 134.8, 136.4, 141.6, 143.0, 143.0, 143.0, 146.5,$$

$$146.5, 147.9, 153.6, 154.7, 157.5, 158.1, 159.7, 161.5, 172.8, 173.7$$

Zweryfikować hipotezę o normalności rozkładu na poziomie $\alpha=0,10$, stosując test Shapiro-Wilka.

## Zadanie 9
Zmierzono czasy wykonania pewnego zadania. Uporządkowano wyniki w kolejności otrzymywania (w czasie). Pełny ciąg reszt dla $n=20$ pomiarów wygląda następująco:

$$
+, +, -, -, +, +, +, -, -, -, -, +, +, -, -, +, +, -, +, -
$$

Parametry do weryfikacji:

* Liczba plusów ($n_1$): 10
* Liczba minusów ($n_2$): 10
* Liczba serii ($k$): 10

Zweryfikować hipotezę o losowości na poziomie $\alpha=0,05$.

## Zadanie 10
Dla 7 par pomiarów (np. wydajność przed i po aktualizacji sterownika) odnotowano, czy wynik się poprawił (+), czy pogorszył (-). Otrzymano sekwencję:
$+, -, +, +, +, +, -$.

Zweryfikować hipotezę, że aktualizacja nie ma wpływu na wydajność (prawdopodobieństwo poprawy $p=0,5$).