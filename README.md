# EstEst Evaluation

Projekt przeznaczony do automatyzacji procesu oceny i prognozowania udziałów oglądalności telewizyjnej (TV audience share) oraz generowania podsumowań estymacji **EstEst**.

## Opis projektu

Narzędzie wykorzystuje Python, biblioteki `pandas` i `numpy` oraz połączenia z bazami danych do przetwarzania wewnętrznych danych telemetrycznych. Główna funkcjonalność obejmuje:

- Ekstrakcję, mapowanie i czyszczenie danych z systemów zewnętrznych (TechEdge, Provys).
- Wyznaczanie metryk błędu (np. RMSE) oraz ewaluację efektywności estymatorów.
- Generowanie miesięcznych raportów podsumowujących.

---

## Instrukcja aktualizacji danych i generowania raportu

Poniższy przewodnik opisuje procedurę krok po kroku niezbędną do zaktualizowania danych oraz wygenerowania nowego podsumowania estymacji za poprzedni miesiąc.

### Wymagania wstępne

- Upewnij się, że masz aktywne połączenie z **dyskiem sieciowym W**.
- W przypadku wystąpienia błędów związanych z niezgodnością typów nazw, zaktualizuj słownik `directory`, uzupełniając strukturę o odpowiednie nazwy z systemów **TechEdge** oraz **Provys**.

### Instrukcja krok po kroku

1. **Eksport danych z TechEdge:**
   - Przejdź do ścieżki: `Rafał Daszuta` $\rightarrow$ `Time` $\rightarrow$ `est_est_evaluaion shr monthly`.
   - Wyeksportuj wymagany raport.

2. **Zapis pliku:**
   - Zapisz pobrany plik w **folderze roboczym projektu**.
   - Nadaj plikowi następującą nazwę (format `.csv`):
     ```text
     Time est_est_evaluaion shr monthly.csv
     ```

3. **Uruchomienie skryptu:**
   - Wykonaj skrypt generujący podsumowanie estymacji w swoim środowisku roboczym.

> **Wskazówka:** Plik wynikowy oraz pliki robocze projektu powinny być zawsze zapisywane w głównym folderze roboczym.
