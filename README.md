# Klasyfikacja choroby serca – projekt uczenia maszynowego

## Opis projektu
Celem projektu było zbudowanie i porównanie modeli uczenia maszynowego służących do predykcji ryzyka choroby serca na podstawie danych medycznych pacjentów.

Projekt obejmuje pełny pipeline analizy danych: od ich przygotowania i eksploracji, przez analizę statystyczną i redukcję wymiarów, aż po budowę modeli klasyfikacyjnych oraz sieci neuronowej.

---

## Zbiór danych
Dane zawierają informacje medyczne o pacjentach, m.in.:
- wiek i płeć,
- typ bólu w klatce piersiowej,
- ciśnienie spoczynkowe,
- poziom cholesterolu,
- poziom cukru na czczo,
- wyniki EKG,
- maksymalne tętno,
- dusznica wysiłkowa,
- depresja odcinka ST (Oldpeak),
- nachylenie ST,
- zmienna docelowa: choroba serca (0/1).

Zbiór zawiera dane liczbowe, kategoryczne oraz brakujące wartości.

---

## Przebieg analizy
W projekcie wykonano:

- przygotowanie i oczyszczenie danych,
- skalowanie cech do przedziału [0,1],
- analizę statystyczną (średnie, min, max),
- analizę korelacji,
- PCA (redukcja wymiarów),
- t-SNE (wizualizacja danych),
- ranking istotności cech,
- budowę modeli klasyfikacyjnych:
  - regresja logistyczna,
  - k-NN,
  - SVM,
- budowę i trening sieci neuronowej,
- ocenę modeli (Accuracy, F1-score, Recall),
- analizę macierzy pomyłek.

---

## Wyniki modeli
- **k-NN (z selekcją cech)** – najlepszy wynik (ok. 90% dokładności),
- **SVM** – stabilne wyniki (ok. 87–88,7%),
- **Regresja logistyczna** – solidny model bazowy (ok. 86,7%),
- **Sieć neuronowa (32–16–8)** – najwyższa czułość (Recall), najmniejsza liczba False Negative.

---

## Wnioski
W przypadku diagnostyki medycznej najważniejszą metryką jest **Recall (czułość)**, ponieważ minimalizacja przypadków False Negative ma kluczowe znaczenie.

Najlepszy model sieci neuronowej osiągnął najwyższą czułość, co czyni go najbardziej odpowiednim do zastosowań wspierających diagnozę chorób serca.

---

## Struktura projektu
- `notebook.ipynb` – pełna analiza danych i modele
- `README.md` – opis projektu

---

## Technologie
- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn

Projekt realizowany w ramach przedmiotu „Wstęp do uczenia maszynowego”
