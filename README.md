# PolicyRenewAI

Projekt systemu Machine Learning dedykowanego dla sektora ubezpieczeń (InsurTech). Narzędzie łączy prognozowanie ryzyka odejścia klientów (**Churn Prediction**) z modułem automatycznej optymalizacji składki ubezpieczeniowej (**Dynamic Pricing**) w celu maksymalizacji retencji i zysku firmy.

## Architektura i Logika Biznesowa

Projekt składa się z trzech głównych modułów zrealizowanych w jednym skrypcie strukturalnym:
1. **Generowanie i Transformacja Danych (ETL)**: Symulacja bazy 5 000 klientów uwzględniająca parametry taryfowe: historię szkód, posiadane zniżki oraz proponowane podwyżki odnowieniowe.
2. **Silnik AI (Predictive Model)**: Wdrożenie klasyfikatora **Random Forest**, który uczy się wzorców zachowań klientów i przewiduje prawdopodobieństwo rezygnacji z polisy.
3. **Moduł Dynamic Pricing (Retention Engine)**: Pętla symulacyjna, która automatycznie identyfikuje klientów zagrożonych odejściem i kalkuluje dla nich, optymalne finansowo rabaty (tj. redukcja podwyżki o 10%, zwiększenie zniżki o 10%), próbując zmienić decyzję klienta z rezygnacji na pozostanie.

## Wykorzystane Technologie

- **Python 3.x**
- **Pandas / NumPy** - inżynieria cech, symulacja zależności biznesowych i manipulacja strukturami danych.
- **Scikit-Learn** - podział zbioru (Train/Test Split), trenowanie modelu `RandomForestClassifier` oraz ewaluacja skuteczności (`accuracy_score`, `classification_report`).

