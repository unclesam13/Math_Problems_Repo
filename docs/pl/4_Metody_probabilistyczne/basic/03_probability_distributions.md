# Lista zadań 03 — Rozkłady prawdopodobieństwa (wybrane modele)

> **Uwaga:** Ta lista zadań jest w trakcie rozwoju. Na razie prosimy jej jeszcze nie robić. :)

## Wprowadzenie

W wielu losowych sytuacjach interesuje nas liczba wystąpień pewnych zdarzeń: liczba wadliwych produktów w partii, liczba błędów w tekście, czas oczekiwania na pierwsze zdarzenie albo liczba zgłoszeń w systemie. Do opisu takich zjawisk teoria prawdopodobieństwa używa modeli probabilistycznych, nazywanych również rozkładami prawdopodobieństwa.

Każdy rozkład opisuje inny typ doświadczenia losowego i odpowiada innym założeniom o sposobie występowania zdarzeń.

W tej liście zadań wykorzystujemy pięć ważnych modeli:

- **Rozkład dwumianowy (próby Bernoulliego)** – modeluje liczbę sukcesów w ustalonej liczbie niezależnych prób o dwóch wynikach (sukces/porażka).
- **Rozkład hipergeometryczny** – stosowany, gdy losujemy elementy **bez zwracania** z populacji skończonej zawierającej elementy różnych typów.
- **Rozkład geometryczny** – opisuje liczbę prób potrzebnych do uzyskania **pierwszego sukcesu** w ciągu niezależnych prób.
- **Rozkład Poissona** – modeluje liczbę zdarzeń zachodzących w danym przedziale czasu lub przestrzeni.
- **Rozkład wielomianowy** – uogólnienie modelu dwumianowego na sytuacje, w których każda próba może dać **więcej niż dwa możliwe wyniki**.

Analiza tych modeli pozwala formalnie opisać doświadczenia losowe i obliczać prawdopodobieństwa zdarzeń w wielu praktycznych sytuacjach.

---

## Zadanie 1 — Model dwumianowy (kontrola jakości)

W fabryce produkowane są śruby. Każda śruba może być **dobra** albo **wadliwa**.  
Prawdopodobieństwo, że losowo wybrana śruba jest wadliwa, wynosi \(p\).

Rozważamy doświadczenie polegające na sprawdzeniu **3 kolejnych śrub**.

**Polecenia**

1. Opisz doświadczenie losowe.  
2. Wyznacz przestrzeń prób \( \Omega \).  
3. Podaj prawdopodobieństwa elementów przestrzeni prób.  
4. Zdefiniuj, co uznajesz za **sukces** w tym modelu.

---

## Zadanie 2 — Model hipergeometryczny (pobieranie z partii)

Magazyn zawiera **20 komponentów**, z czego **5 jest wadliwych**, a **15 sprawnych**.

Losowo wybieramy **4 komponenty bez zwracania** do kontroli.

**Polecenia**

1. Opisz doświadczenie losowe.  
2. Zdefiniuj przestrzeń prób \( \Omega \) jako liczbę wadliwych elementów w próbie.  
3. Wyznacz możliwe wartości zmiennej losowej.  
4. Podaj rozkład prawdopodobieństwa.  
5. Wyjaśnij, co oznacza **sukces** w tym modelu.

---

## Zadanie 3 — Model geometryczny (oczekiwanie na pierwsze zdarzenie)

W drukarni każda wydrukowana strona może zawierać **błąd druku** z prawdopodobieństwem \(p\).

Doświadczenie polega na obserwowaniu kolejnych stron aż do pojawienia się **pierwszego błędu**.

**Polecenia**

1. Opisz doświadczenie losowe.  
2. Wyznacz przestrzeń prób \( \Omega \).  
3. Podaj rozkład prawdopodobieństwa.  
4. Określ, co uznajesz za sukces.

---

## Zadanie 4 — Model Poissona (napływ zdarzeń)

Usługa internetowa otrzymuje średnio **3 zgłoszenia błędów na godzinę**.

Zakładamy, że liczba zgłoszeń w danym przedziale czasu ma **rozkład Poissona**.

**Polecenia**

1. Opisz doświadczenie losowe.  
2. Wyznacz przestrzeń prób \( \Omega \).  
3. Podaj wzór na rozkład prawdopodobieństwa.  
4. Zinterpretuj parametr \( \lambda \).

---

## Zadanie 5 — Model wielomianowy (kategorie wyników)

Gracz rzuca **kostką 5 razy**.

Wyniki grupujemy w trzy kategorie:

- małe liczby (1–2)  
- średnie liczby (3–4)  
- duże liczby (5–6)

**Polecenia**

1. Opisz doświadczenie losowe.  
2. Zdefiniuj przestrzeń prób.  
3. Zapisz rozkład wielomianowy.  
4. Wyjaśnij interpretację parametrów.

---

## Zadanie 6 — Model dwumianowy

Prawdopodobieństwo wyprodukowania wadliwej części wynosi **0.04**.

Kontroler sprawdza **10 części**.

Oblicz prawdopodobieństwo, że:

- dokładnie **2 części są wadliwe**,  
- **co najmniej jedna część** jest wadliwa.

---

## Zadanie 7 — Model hipergeometryczny

Pudełko zawiera:

- 12 sprawnych żarówek  
- 3 wadliwe

Losujemy **5 żarówek bez zwracania**.

Oblicz prawdopodobieństwo, że w próbie będą **dokładnie 2 wadliwe żarówki**.

---

## Zadanie 8 — Model geometryczny

Prawdopodobieństwo błędu podczas kompilacji programu wynosi **0.1** dla każdej kompilacji.

Programista wykonuje kolejne kompilacje aż do wystąpienia **pierwszego błędu**.

Oblicz prawdopodobieństwo, że:

- pierwszy błąd pojawi się przy **4. kompilacji**,  
- pojawi się **najpóźniej przy 3. kompilacji**.

---

## Zadanie 9 — Model Poissona

Centrum obsługi klienta otrzymuje średnio **5 zgłoszeń na godzinę**.

Oblicz prawdopodobieństwo, że w ciągu jednej godziny:

- wystąpią dokładnie **3 zgłoszenia**,  
- wystąpi **co najmniej jedno zgłoszenie**.

---

## Zadanie 10 — Model wielomianowy

Pudełko zawiera cukierki trzech smaków:

- truskawkowe – 40%  
- cytrynowe – 35%  
- miętowe – 25%

Losowo wybieramy **6 cukierków niezależnie**.

Oblicz prawdopodobieństwo, że otrzymamy:

- 3 truskawkowe  
- 2 cytrynowe  
- 1 miętowy
