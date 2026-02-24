# Bachelorarbeit: Vergleich numerischer Verfahren zur Eigenwertbestimmung

Dieses Repository enthält den vollständigen Quellcode zu meiner Bachelorarbeit **"Vergleich numerischer Verfahren zur Eigenwertbestimmung"** (Alexander Averdunk, Februar 2026). 

Das Ziel dieses Repositories ist es, die vollständige **Reproduzierbarkeit** aller numerischen Experimente, Laufzeitanalysen und Abbildungen aus Kapitel 6 der Arbeit zu gewährleisten.

## Inhalt des Repositories

In diesem Projekt werden klassische iterative Verfahren mit rekursiven High-Performance-Ansätzen zur Eigenwertbestimmung (insbesondere für symmetrische Tridiagonalmatrizen) verglichen. 

Folgende Kernalgorithmen wurden von Grund auf in Python implementiert:
* **QR-Zerlegungen:** Klassisches (KGS) und modifiziertes (MGS) Gram-Schmidt-Verfahren.
* **Iteratives QR-Verfahren:** Inklusive Rayleigh-Quotienten-Shift und Deflation zur Konvergenzbeschleunigung.
* **Divide-and-Conquer-Verfahren:** Rekursiver Algorithmus für hermitesche Tridiagonalmatrizen inklusive Lösung der Säkulargleichung (via `scipy.optimize.brentq`).

Zusätzlich enthält der Code die vollständige Logik zur **Generierung synthetischer Testmatrizen** mit exakt vordefinierten Spektralkonditionen $\kappa(A)$ sowie die Skripte zur Auswertung und Visualisierung der Ergebnisse.

## Systemvoraussetzungen & Bibliotheken

Der Code wurde in **Python 3.12** geschrieben. Zur Ausführung der Skripte und Notebooks werden folgende Standard-Bibliotheken aus dem wissenschaftlichen Python-Ökosystem benötigt:

* `numpy` (für Vektor- und Matrixoperationen)
* `scipy` (für die Nullstellensuche der Säkulargleichung)
* `matplotlib` (für das Plotten der Graphen)

Die Abhängigkeiten können ganz einfach über das Terminal installiert werden:
```bash
pip install numpy scipy matplotlib
