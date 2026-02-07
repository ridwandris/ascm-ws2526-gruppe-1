# ASCM WS25/26 – Gruppe 1

Dieses Repository enthält die Jupyter-Notebooks und Daten für die Übungsaufgaben der Wahlmodul **Algorithms im Supply Chain Management** (Prof. Dr.-Ing. Jens Heger: Wintersemester 2025/26, Leuphana Universität Lüneburg).

## Projektstruktur

```
├── Einfuehrung/                        # Einführungsbeispiele
│   ├── Bierproduktion-Einfuehrung.ipynb
│   └── Transportproblem-Einfuehrung.ipynb
├── ASCM-ws2526-Gruppe_1/               # Aufgaben
│   ├── 01-Produktion/
│   │   └── Bierproduktion.ipynb
│   ├── 02-Transportproblem/
│   │   └── Transportproblem.ipynb
│   └── 03-Bedarfsprognose/
│       ├── Bedarfsprognose_Aufgabe.ipynb
│       ├── Bedarfsprognose_Beispiele.ipynb
│       ├── Bedarfsprognose_Theorie.ipynb
│       └── *.csv                        # Datensätze
├── pyproject.toml                       # Projektabhängigkeiten
├── uv.lock                             # Lock-Datei (exakte Versionen)
└── .python-version                      # Python-Version (3.13)
```

## Voraussetzungen

- **Python 3.13** oder höher
- **[uv](https://docs.astral.sh/uv/)** – Schneller Python-Paketmanager

### uv installieren

```bash
# macOS / Linux
curl -LsSf https://astral.sh/uv/install.sh | sh

# Windows
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

## Projekt reproduzieren

### 1. Repository klonen

```bash
git clone <repository-url>
cd ASCM-ws2526-Gruppe-1
```

### 2. Abhängigkeiten installieren

```bash
uv sync
```

Dieser Befehl:
- erstellt automatisch eine virtuelle Umgebung (`.venv/`)
- installiert die korrekte Python-Version (falls nötig)
- installiert alle Abhängigkeiten in den exakten Versionen aus `uv.lock`

### 3. Notebooks ausführen

Öffne das Projekt in **VS Code** und wähle den Python-Interpreter aus der virtuellen Umgebung (`.venv/bin/python`) als Kernel für die Notebooks.

Alternativ kannst du Jupyter im Terminal starten:

```bash
uv run jupyter notebook
```

## Abhängigkeiten

| Paket | Beschreibung |
|---|---|
| `pulp` | Lineare Optimierung (Produktion, Transport) |
| `pandas` | Datenverarbeitung und -analyse |
| `numpy` | Numerische Berechnungen |
| `matplotlib` | Visualisierung / Plots |
| `scikit-learn` | Machine Learning & Metriken |
| `statsmodels` | Statistische Modelle & Zeitreihenanalyse |
| `pmdarima` | Auto-ARIMA Zeitreihenprognose |

## Neue Abhängigkeiten hinzufügen

```bash
uv add <paketname>
```

Die `pyproject.toml` und `uv.lock` werden automatisch aktualisiert.
