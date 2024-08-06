# Program do Klasyfikacji Gwiazd

## Opis

Program klasyfikuje gwiazdy na podstawie ich właściwości: temperatury, jasności, promienia i wielkości bezwzględnej. Wykorzystuje algorytm K-Nearest Neighbors (KNN) z metryką euklidesową. Program umożliwia również analizę wpływu liczby sąsiadów na wyniki algorytmu.

## Instrukcja Uruchomienia

1. Skopiuj kod źródłowy do powłoki Pythona i upewnij się, że masz zainstalowane biblioteki: `pandas`, `seaborn`, `matplotlib`.
2. Alternatywnie, uruchom plik `.ipynb` w Jupyter Notebook (lokalnie lub online).
3. Upewnij się, że plik z danymi wejściowymi znajduje się w tym samym katalogu co skrypt lub zmień ścieżkę w zmiennej `data` w kodzie źródłowym.

## Opis Działania

### Algorytm KNN:
1. **Faza Treningowa**: Przechowuje wszystkie dane treningowe.
2. **Faza Przewidywania**:
   - Oblicza odległość między nowym punktem a danymi treningowymi.
   - Wybiera `k` najbliższych sąsiadów.
   - Przypisuje nowemu punktowi najczęstszą klasę spośród sąsiadów.

### Algorytm Normalizacji:
1. Odczyt danych.
2. Usunięcie kolumny `Star color`.
3. Normalizacja wartości za pomocą wzoru: `(wartość - min) / (max - min)`.
4. Podział danych na zestawy treningowy i testowy.

### Uczenie:
1. Dla każdego punktu testowego oblicza odległości do punktów treningowych.
2. Sortuje odległości i wybiera `k` najbliższych.
3. Przypisuje klasę na podstawie większości.

## Wymagane Biblioteki

- pandas
- seaborn
- matplotlib

## Instalacja

Aby zainstalować wymagane biblioteki, uruchom:
```sh
pip install pandas seaborn matplotlib
