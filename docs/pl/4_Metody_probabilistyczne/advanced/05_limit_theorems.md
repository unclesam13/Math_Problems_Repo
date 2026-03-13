# LISTA ZADAŃ NR 5: Twierdzenia graniczne i aproksymacje

## Zadanie 1
**Twierdzenie Poissona – rzadkie zdarzenia**
Wadliwość produkcji pewnego elementu elektronicznego wynosi $p=0,002$. W partii towaru znajduje się $n=1000$ sztuk tych elementów. Obliczyć prawdopodobieństwo, że w tej partii:
1. nie będzie ani jednej sztuki wadliwej,
2. będą co najwyżej 3 sztuki wadliwe.

*Wskazówka: Ponieważ $n$ jest duże ($n \ge 100$), a $p$ małe ($p \le 0,1$) i $np \le 10$, należy zastosować przybliżenie rozkładem Poissona z parametrem $\lambda = np$.*

## Zadanie 2
**Twierdzenie Moivre’a-Laplace’a (całkowe) – rzut monetą**
Rzucamy symetryczną monetą $n=100$ razy. Obliczyć prawdopodobieństwo, że liczba uzyskanych orłów będzie się mieścić w przedziale $\langle 45, 55 \rangle$.

*Cel: Zastosowanie aproksymacji rozkładu dwumianowego rozkładem normalnym dla dużej liczby prób.*

## Zadanie 3
**Dobór liczebności próby (odwrócone CTG)**
Prawdopodobieństwo urodzenia chłopca wynosi $p=0,515$. Ile razy należy powtórzyć doświadczenie (urodzenia), aby z prawdopodobieństwem co najmniej $0,95$ można było twierdzić, że częstość występowania chłopców w próbie będzie się różnić od prawdopodobieństwa $p$ o mniej niż $0,01$?

*Wskazówka: Należy skorzystać z nierówności $P(|\frac{k}{n} - p| < \varepsilon) \ge 1 - \alpha$ przy użyciu dystrybuanty normalnej.*

## Zadanie 4
**Centralne Twierdzenie Graniczne – suma błędów zaokrągleń**
Dodajemy do siebie $n=100$ liczb, z których każda została zaokrąglona do najbliższej liczby całkowitej. Błędy zaokrągleń są niezależnymi zmiennymi losowymi o rozkładzie jednostajnym na przedziale $(-0,5; 0,5)$. Obliczyć prawdopodobieństwo, że błąd sumy tych liczb (co do modułu) nie przekroczy $3$.

*Komentarz: Jest to klasyczny przykład sumowania zmiennych o rozkładzie innym niż normalny (tu: jednostajny), które w sumie dają rozkład normalny.*

## Zadanie 5
**Centralne Twierdzenie Graniczne – obciążenie windy**
Winda towarowa może unieść ciężar do $2000$ kg. Do windy wchodzi $25$ osób. Waga losowego pasażera jest zmienną losową o wartości oczekiwanej $75$ kg i odchyleniu standardowym $10$ kg. Obliczyć prawdopodobieństwo, że waga pasażerów nie przekroczy dopuszczalnego obciążenia windy.

## Zadanie 6
**Aproksymacja czasu pracy – rozkład wykładniczy**
Bateria w laptopie ma czas pracy będący zmienną losową o rozkładzie wykładniczym ze średnią $4$ godziny. Użytkownik planuje dłuższą pracę w terenie i zabiera ze sobą $36$ naładowanych baterii (wymienia je natychmiast po wyczerpaniu). Jakie jest prawdopodobieństwo, że łączny czas pracy na tym zestawie baterii przekroczy $150$ godzin?

## Zadanie 7
**Lokalne Twierdzenie Moivre’a-Laplace’a**
Zdarzenie $A$ występuje w pojedynczym doświadczeniu z prawdopodobieństwem $p=0,6$. Doświadczenie powtarzamy $n=600$ razy. Obliczyć prawdopodobieństwo, że zdarzenie $A$ zajdzie dokładnie $370$ razy.

*Wskazówka: Dla dużych $n$ prawdopodobieństwo punktowe $P(X=k)$ przybliżamy wartością gęstości rozkładu normalnego.*

## Zadanie 8
**Porównanie aproksymacji**
Prawdopodobieństwo sukcesu w pojedynczej próbie wynosi $p=0,1$. Wykonujemy $n=30$ prób. Obliczyć prawdopodobieństwo uzyskania dokładnie 2 sukcesów, stosując:
1. dokładny wzór Bernoulliego,
2. przybliżenie Poissona,
3. lokalne twierdzenie Moivre’a-Laplace’a.
Porównać wyniki.

## Zadanie 9
**Nierówność Czebyszewa**
Zmienna losowa $X$ ma wartość oczekiwaną $E(X)=10$ i wariancję $D^2(X)=4$. Nie znając dokładnego rozkładu tej zmiennej, oszacować (podać ograniczenie dolne) prawdopodobieństwo, że zmienna $X$ przyjmie wartość z przedziału $(4, 16)$.

## Zadanie 10
**Zastosowanie statystyczne – średnia z próby**
Z populacji, w której cecha $X$ ma rozkład (niekoniecznie normalny) o średniej $\mu=100$ i wariancji $\sigma^2=25$, pobrano losową próbę o liczebności $n=100$. Obliczyć prawdopodobieństwo, że średnia arytmetyczna z tej próby $\bar{X}$ będzie mniejsza niż $99$.