# Projekt z przedmiotu: Modelowanie i analiza procesow biznesowych

## Organizacja i konsultacje

- Konsultacje projektowe odbywaja sie co dwa tygodnie, zgodnie z rozpiska w USOS.
- Termin konsultacji: poniedzialki, 15:00-16:30 (C2 426).
- Projekty mozna realizowac w grupach (preferowane 2-4 osoby).
- Postepy projektu nalezy konsultowac co najmniej raz w miesiacu.
- Zapisy na konsultacje beda prowadzone przez arkusz slotow.
- Gdy zabraknie slotow, mozliwe sa konsultacje poza godzinami zajec lub pierwszenstwo w kolejnym terminie.

## Dane

Kazda grupa powinna wybrac co najmniej jeden zestaw danych z:
- https://zenodo.org/communities/iopt/

## Kamienie milowe

### Milestone 1: Zrozumienie zbioru danych

Zakres:
- opis zbioru danych i jego kontekstu (system, typ zdarzen, liczba przypadkow),
- identyfikacja kluczowych atrybutow logu zdarzen (case id, activity, timestamp, resource - ktore sa, ktorych brakuje),
- analiza jakosci danych (brakujace wartosci, duplikaty, niespojne timestampy, niespojne typy danych itp.),
- eksploracyjna analiza danych,
- podstawowe statystyki (liczba eventow, cases, activities),
- podstawowe wizualizacje (timeline, distribution, frequency).

Wynik:
- raport + Jupyter Notebook (np. Google Colab).

### Milestone 2: Eksploracja danych i analiza cech

Zakres:
- przygotowanie lub wybor logu zdarzen,
- czyszczenie i normalizacja danych,
- wykrywanie wartosci odstajacych (outlierow),
- redukcja wymiarowosci: PCA / t-SNE / UMAP,
- klasteryzacja i inne wizualizacje,
- analiza relacji miedzy zdarzeniami,
- identyfikacja ciekawych wzorcow czasowych (pory dnia, dni tygodnia, sezonowosc),
- analiza czestosci sciezek i najczestszych wariantow,
- identyfikacja nietypowych zachowan i anomalii.

Wynik:
- raport + Jupyter Notebook (np. Google Colab).

### Milestone 3: Odkrywanie procesu i regul

Zakres:
- wygenerowanie modelu DFG (Directly-Follows Graph),
- odkrycie modelu procesu co najmniej dwoma roznymi algorytmami,
- stworzenie koncowego modelu BPMN i propozycja ulepszen,
- odkrycie regul decyzyjnych,
- analiza zasobow (sieci wspolpracy, obciazenie pracownikow),
- identyfikacja problemow i waskich gardel procesu.

W raporcie koncowym nalezy takze uwzglednic:
- co model mowi o analizowanym systemie,
- jakie sa najczestsze sciezki procesu,
- gdzie pojawiaja sie opoznienia,
- jakie moga byc potencjalne usprawnienia i wnioski biznesowe.

Wynik:
- raport z modelami procesu (ewentualnie Jupyter Notebook).

## Opcjonalna sciezka badawcza

W ramach projektu mozliwa jest takze sciezka naukowa, polegajaca na opracowaniu badan i przygotowaniu krotkiego artykulu:
- https://www.yorku.ca/events/bpm2026/calls/call-for-responsible-bpm-forum/
- https://www.yorku.ca/events/bpm2026/workshops/
