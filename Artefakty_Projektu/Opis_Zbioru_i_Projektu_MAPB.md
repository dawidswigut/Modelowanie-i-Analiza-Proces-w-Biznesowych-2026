# Projekt MAPB - o co chodzi i co to za zbior danych

## Cel projektu

Celem projektu z przedmiotu "Modelowanie i analiza procesow biznesowych" jest praktyczna analiza logow zdarzen procesowych.
Grupa projektowa wybiera zestaw danych (lub podzbior) i przechodzi przez kolejne kamienie milowe, od zrozumienia danych po modelowanie i ocene procesu.

W pierwszym etapie (Milestone 1) nacisk jest na:
- zrozumienie struktury danych,
- identyfikacje atrybutow process mining,
- ocene jakosci danych,
- wykonanie EDA i wizualizacji.

## Co zawiera ten zbior (Dataset_8087219)

Zbior zawiera dane ze srodowiska produkcyjnego (automatyka przemyslowa), opisane jako sygnatury zdarzen i wzorce aktywnosci.
W praktyce sa tu trzy typy artefaktow:

1. `Signature_*.txt`
- sekwencje zdarzen JSON w czasie,
- kazdy rekord zawiera `station`, `timestamp` i slownik `events` z sygnalami,
- pliki reprezentuja wybrane aktywnosci procesu (np. Burn, Mill, Transport).

2. `Visual_Signature_*.png`
- wykresy przebiegow sygnalow,
- ulatwiaja reczna interpretacje momentow zmiany stanu i granic aktywnosci.

3. `Detect*App.siddhi`
- reguly CEP (Siddhi) do wykrywania wzorcow low-level i high-level,
- mapowanie sygnalow czujnikow/aktuatorow na aktywnosci procesowe,
- publikowanie wykrytych zdarzen na MQTT.

Aktualna organizacja repozytorium:
- folder `Dataset_8087219` zawiera dane zrodlowe (`Signature_*.txt` i `Visual_Signature_*.png`),
- folder `Artefakty_Projektu` zawiera notebook, raport i aplikacje CEP (`Detect*App.siddhi`).

## Jak to sie laczy z process mining

Ten zbior jest dobry do przejscia od surowych sygnalow sterowania do logu procesowego:
- surowe sygnaly -> eventy techniczne,
- eventy techniczne -> aktywnosci procesu (CEP/Siddhi),
- aktywnosci + czas -> log do analizy procesu.

To odpowiada typowemu pipeline'owi process mining w systemach cyber-fizycznych.

## Najwazniejsze ograniczenia danych

- brak jawnego `case_id` w pojedynczym rekordzie,
- brak jawnego `activity` w pojedynczym rekordzie (dla sygnatur odtwarzane z nazwy pliku),
- brak klasycznego `resource` (uzytkownik/rola); dostepny jest zasob techniczny (`station`).

W analizie trzeba wiec jawnie opisac zalozenia rekonstrukcji logu.

## Co oddac jako wynik projektu (na tym etapie)

Dla Milestone 1 najlepiej oddac:
- raport markdown/pdf z opisem danych i wynikami analizy,
- notebook Jupyter z kodem i wykresami,
- jasne zalozenia dot. identyfikacji case/activity/resource,
- krotka sekcje o ryzykach danych i planie dalszych krokow.

Ten opis i notebook w folderze sa przygotowane dokladnie pod ten cel.
