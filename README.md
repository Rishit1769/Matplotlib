# Matplotlib Data Visualization Project

A comprehensive data visualization project demonstrating the use of **Matplotlib** for analyzing and visualizing **Indian Premier League (IPL)** cricket data. This project covers five fundamental chart types used in data science and analytics workflows.

---

## Project Overview

| Aspect | Details |
|---|---|
| **Language** | Python 3.14 |
| **Libraries** | Matplotlib, NumPy, Pandas, Seaborn |
| **Domain** | IPL Cricket Data Visualization |
| **Format** | Jupyter Notebooks (.ipynb) |

---

## Repository Structure

```
Matplotlib/
├── README.md                      # Project documentation
├── .gitignore                     # Git ignore rules
├── .vscode/
│   └── settings.json              # VS Code Python interpreter config
│
├── ── Jupyter Notebooks ──
├── 2D-Plots.ipynb                 # Line plots and basic 2D plotting
├── BarChart.ipynb                 # Vertical and horizontal bar charts
├── Histogram.ipynb                # Frequency distribution histograms
├── Pie-Chart.ipynb                # Pie charts for proportional data
├── ScatterPlots.ipynb             # Scatter plots for correlation analysis
│
├── ── CSV Data Files ──
├── batter.csv                     # IPL batsman statistics (606 players)
├── batsman_season_record.csv      # Season-wise runs for 5 top batsmen
├── fours-sixes.csv                # Season-wise fours and sixes count
├── gayle-175.csv                  # Chris Gayle's historic 175-run innings
├── sharma-kohli.csv               # Yearly comparison: Sharma vs Kohli
├── vk.csv                         # Virat Kohli's match-by-match scores
│
└── ── Generated / Binary Files ──
    ├── big-array.npy              # NumPy binary array (large dataset)
    └── pie-chart.png              # Saved pie chart output (300 DPI)
```

---

## Notebooks

### 1. `2D-Plots.ipynb` — Line Plots

Demonstrates fundamental line plotting with Matplotlib, progressing from basic to fully customized plots.

| Cell | Topic | Description |
|------|-------|-------------|
| 1 | Imports | Loads `numpy`, `pandas`, `matplotlib.pyplot`, `seaborn` |
| 2 | Basic Line Plot | Simple `plt.plot()` with hardcoded price/year data |
| 3 | CSV Data Plot | Reads `sharma-kohli.csv` and plots V Kohli's yearly runs |
| 4 | Single Batsman | Plots RG Sharma's runs over the years |
| 5 | Multi-Series Plot | Overlays both Kohli and Sharma on a single chart |
| 6 | Axis Labels & Title | Adds `plt.title()`, `plt.xlabel()`, `plt.ylabel()` |
| 7 | Line Customization | Customizes `color` for each line (red/black) |
| 8 | Line Style | Adds `linestyle='dashdot'` for visual distinction |
| 9 | Markers | Adds `marker='+'` at each data point |
| 10 | Legend | Adds `plt.legend()` using `label` parameter |
| 11 | Axis Limits | Demonstrates `plt.xlim()` and `plt.ylim()` with outlier data |
| 12 | Grid Lines | Adds `plt.grid()` for readability |
| 13 | Final Output | Calls `plt.show()` to display the complete chart |

**Key Functions Covered:**
- `plt.plot()` — Line plotting with color, linestyle, marker, and label parameters
- `plt.title()`, `plt.xlabel()`, `plt.ylabel()` — Chart annotations
- `plt.legend()` — Legend display
- `plt.grid()` — Grid overlay
- `plt.xlim()`, `plt.ylim()` — Axis range control
- `plt.show()` — Render display

---

### 2. `BarChart.ipynb` — Bar Charts

Demonstrates vertical and horizontal bar charts, grouped bars, and stacked bar visualizations.

| Cell | Topic | Description |
|------|-------|-------------|
| 1 | Imports | Standard library imports |
| 2 | Basic Bar Chart | Vertical bar chart with categorical x-axis (favorite colors) |
| 3 | Horizontal Bar | Uses `plt.barh()` for horizontal bar chart |
| 4 | CSV Data | Reads `batsman_season_record.csv`, plots 2015 season runs |
| 5 | Grouped Bars | Overlapping bar charts using `np.arange()` with width offsets |
| 6 | Custom X-Ticks | Uses `plt.xticks()` to replace numeric indices with batsman names |
| 7 | Stacked Bars | Uses `bottom` parameter to stack multiple bar layers |

**Key Functions Covered:**
- `plt.bar()` — Vertical bar chart
- `plt.barh()` — Horizontal bar chart
- `plt.xticks()` — Custom tick labels
- `np.arange()` — Array indexing for bar positioning
- `bottom` parameter — Stacked bar construction

---

### 3. `Histogram.ipynb` — Histograms

Demonstrates frequency distribution visualization using histograms with both simple and CSV-based data.

| Cell | Topic | Description |
|------|-------|-------------|
| 1 | Imports | Standard library imports |
| 2 | Basic Histogram | Plots frequency distribution with custom bin edges `[10, 25, 40, 55, 70]` |
| 3 | Load CSV Data | Reads `vk.csv` containing Virat Kohli's match scores |
| 4 | Score Distribution | Histogram with 12 bins (0–120) showing score frequency ranges |
| 5 | Large Dataset | Loads `big-array.npy` and plots with `log=True` for y-axis scale |

**Key Functions Covered:**
- `plt.hist()` — Histogram creation with `bins` and `log` parameters
- `np.load()` — Loading NumPy binary arrays
- Logarithmic scaling for handling skewed distributions

---

### 4. `Pie-Chart.ipynb` — Pie Charts

Demonstrates proportional data visualization with pie charts, including styling and export.

| Cell | Topic | Description |
|------|-------|-------------|
| 1 | Imports | Standard library imports |
| 2 | Basic Pie Chart | Simple pie chart with subject-wise data and labels |
| 3 | CSV Data Pie | Reads `gayle-175.csv`, shows run distribution with percentage labels |
| 4 | Styled Pie Chart | Adds custom `colors`, `explode`, and `shadow` for visual emphasis |
| 5 | Save Figure | Exports chart to `pie-chart.png` at 300 DPI resolution |

**Key Functions Covered:**
- `plt.pie()` — Pie chart with `labels`, `autopct`, `colors`, `explode`, `shadow`
- `plt.savefig()` — Export chart to PNG with DPI control

---

### 5. `ScatterPlots.ipynb` — Scatter Plots

Demonstrates scatter plots for correlation analysis with real-world and synthetic datasets.

| Cell | Topic | Description |
|------|-------|-------------|
| 1 | Imports | Standard library imports |
| 2 | Synthetic Data | Generates `x` (linspace) and `y` (linear + noise) using NumPy |
| 3 | Basic Scatter | Plots the synthetic noisy linear relationship |
| 4 | Load CSV Data | Reads `batter.csv` (top 50 IPL batsmen with stats) |
| 5 | Avg vs Strike Rate | Scatter plot with black '+' markers, title, and axis labels |
| 6 | Bubble Plot | Loads seaborn `tips.csv` from GitHub; scatter with `size` parameter for bubble chart |

**Key Functions Covered:**
- `plt.scatter()` — Scatter plot with `color`, `marker`, and `size` parameters
- `np.linspace()`, `np.random.randint()` — Synthetic data generation
- Online data loading via `urlopen()` with SSL context

---

## CSV Data Files

### `batter.csv`
IPL career statistics for **606 batsmen**. Columns:

| Column | Type | Description |
|--------|------|-------------|
| `batter` | string | Batsman's full name |
| `runs` | int | Total career runs |
| `avg` | float | Batting average |
| `strike_rate` | float | Strike rate (runs per 100 balls) |

### `batsman_season_record.csv`
Season-wise run totals for **5 top batsmen** across 3 IPL seasons.

| Column | Type | Description |
|--------|------|-------------|
| `batsman` | string | Batsman's name |
| `2015` | int | Runs scored in 2015 season |
| `2016` | int | Runs scored in 2016 season |
| `2017` | int | Runs scored in 2017 season |

### `fours-sixes.csv`
Season-wise count of fours and sixes hit across **6 IPL seasons**.

| Column | Type | Description |
|--------|------|-------------|
| `season` | int | IPL season year |
| `Fours` | int | Total fours hit in that season |
| `Sixes` | int | Total sixes hit in that season |

### `gayle-175.csv`
Match-level batting data from Chris Gayle's record-breaking **175-run innings** (2013 IPL).

| Column | Type | Description |
|--------|------|-------------|
| `batsman` | string | Batsman's name |
| `batsman_runs` | int | Runs scored in that match |

### `sharma-kohli.csv`
Yearly run comparison between **Rohit Sharma** and **Virat Kohli** (2008–2017).

| Column | Type | Description |
|--------|------|-------------|
| `index` | int | Year (2008–2017) |
| `RG Sharma` | int | Rohit Sharma's annual runs |
| `V Kohli` | int | Virat Kohli's annual runs |

### `vk.csv`
Match-by-match batting scores for **Virat Kohli** across 141 IPL matches.

| Column | Type | Description |
|--------|------|-------------|
| `match_id` | int | Unique match identifier |
| `batsman_runs` | int | Runs scored in that match |

---

## Configuration Files

### `.gitignore`
Excludes the Python virtual environment directory from version control.

### `.vscode/settings.json`
Configures VS Code to use the project's local Python virtual environment:
```json
{
    "python.defaultInterpreterPath": "${workspaceFolder}/.venv/bin/python",
    "python.terminal.activateEnvironment": true
}
```

---

## Getting Started

### Prerequisites

- Python 3.13 or later
- pip package manager

### Installation

1. **Clone the repository:**
   ```bash
   git clone <repository-url>
   cd Matplotlib
   ```

2. **Create and activate a virtual environment:**
   ```bash
   python -m venv .venv
   source .venv/bin/activate  # macOS/Linux
   .venv\Scripts\activate     # Windows
   ```

3. **Install dependencies:**
   ```bash
   pip install matplotlib numpy pandas seaborn jupyter
   ```

4. **Launch Jupyter Notebook:**
   ```bash
   jupyter notebook
   ```

5. **Open any notebook** (e.g., `2D-Plots.ipynb`) and run cells sequentially.

---

## Chart Type Reference

| Chart Type | Notebook | Best Used For | Matplotlib Function |
|---|---|---|---|
| Line Plot | `2D-Plots.ipynb` | Trends over time, comparisons | `plt.plot()` |
| Bar Chart | `BarChart.ipynb` | Categorical comparisons, rankings | `plt.bar()`, `plt.barh()` |
| Histogram | `Histogram.ipynb` | Distribution analysis, frequency | `plt.hist()` |
| Pie Chart | `Pie-Chart.ipynb` | Proportional composition | `plt.pie()` |
| Scatter Plot | `ScatterPlots.ipynb` | Correlation, relationship analysis | `plt.scatter()` |

---

## Matplotlib Functions Reference

### Plot Creation
| Function | Purpose |
|---|---|
| `plt.plot()` | Create line plot |
| `plt.bar()` | Create vertical bar chart |
| `plt.barh()` | Create horizontal bar chart |
| `plt.hist()` | Create histogram |
| `plt.pie()` | Create pie chart |
| `plt.scatter()` | Create scatter plot |

### Chart Customization
| Function | Purpose |
|---|---|
| `plt.title()` | Add chart title |
| `plt.xlabel()` | Add x-axis label |
| `plt.ylabel()` | Add y-axis label |
| `plt.legend()` | Display legend |
| `plt.grid()` | Add grid lines |
| `plt.xticks()` | Customize x-axis tick labels |
| `plt.yticks()` | Customize y-axis tick labels |
| `plt.xlim()` | Set x-axis range |
| `plt.ylim()` | Set y-axis range |
| `plt.show()` | Render and display the chart |
| `plt.savefig()` | Export chart to file (PNG, PDF, SVG) |

---

## License

This project is intended for educational and learning purposes.
