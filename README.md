# Predykcja 180 - dniowej śmiertelności (SUPPORT2) - model SVM

Projekt jest odtworzeniem części badania SUPPORT(Study to Understand Prognoses and Preferences for Outcomes and Risks of Treatments) z zastosowaniem współczesnych metod uczenia maszynowego.
Celem jest zbudowanie i ocena binarnego modelu klasyfikacji, który przewiduje 180-dniową śmiertelność u ciężko chorych hospitalizowanych dorosłych pacjentów.

**Zbiór danych**
- Zestaw SUPPORT2 (Faza I badania SUPPORT)
- Zawiera zmienne kliniczne, fizjologiczne i demograficzne związane z ryzykiem zgonu
- Zmienna docelowa: **death** (0 = przeżył, 1 = zmarł)
  
**Użyty model**
- Support Vector Machine (SVM)
  
**Metodologia** 

  Projekt obejmuje pipeline ML:
  - eksploracja danych i analiza braków
  - preprocessing z użyciem ColumnTransformer(dla zmiennych numerycznych - mediana, dla zmiennych kategorycznych - najczęściej występująca wartość)
  - trenowanie modelu i znalezienie najlepszych hiperparametrów
  - końcowa ewaluacja na wydzielonym zbiorze testowym
  
**Finalne metryki testowe**
| Metryka      | Wynik      |
| ------------ | ---------- |
| **Accuracy** | **0.7567** |
| **F1-score** | **0.8054** |
| **ROC-AUC**  | **0.8429** |

**Kluczowe wnioski**

Model SVM z jądrem RBF uzyskał dobrą jakoś predykcji dla 180 - dniowej śmiertelności.
Walidacja krzyżowa wykazała, że najlepszym hiperparametrem okazało się **C = 0.1**
Model cechuje się skutecznym wykrywaniem pacjentów wysokiego ryzyka i bardzo dobrą zdolnością separacji klas, choć nadal występuje pewna liczba błędów klasyfikacji.

**Pliki**
- **support2.ipynb** - pełny kod i analiza
