<div id="top"></div>

<br>

<!-- Header Badges -->

<p align="center">
  <a href="https://github.com/soph-k">
    <img src="https://img.shields.io/badge/Made%20by-soph--k-d9a07e?style=for-the-badge&amp;labelColor=123b3d" alt="Made by soph-k" />
  </a>
  <a href="https://www.python.org/">
    <img src="https://img.shields.io/badge/Python-123b3d?style=for-the-badge&amp;logo=python&amp;logoColor=white" alt="Python" />
  </a>
  <a href="https://jupyter.org/">
    <img src="https://img.shields.io/badge/Jupyter-d9a07e?style=for-the-badge&amp;logo=jupyter&amp;logoColor=white" alt="Jupyter Notebook" />
  </a>
  <a href="https://github.com/soph-k/ammonia-shock-analysis">
    <img src="https://img.shields.io/github/last-commit/soph-k/ammonia-shock-analysis?style=for-the-badge&amp;labelColor=123b3d&amp;color=d9a07e" alt="Last commit" />
  </a>
  <a href="https://github.com/soph-k/ammonia-shock-analysis">
    <img src="https://img.shields.io/github/repo-size/soph-k/ammonia-shock-analysis?style=for-the-badge&amp;labelColor=123b3d&amp;color=d9a07e" alt="Repository size" />
  </a>
</p>

<br>

<!-- Header -->

<div align="center">

<a href="https://github.com/soph-k">
  <img src="https://raw.githubusercontent.com/soph-k/logo/main/logo.png" width="105" alt="soph-k logo" />
</a>

<h2>『 U.S. Ammonia Shock Analysis 』</h2>

<p>
  Exploring how natural gas prices and geopolitical disruptions influenced
  U.S. ammonia-related producer prices—and when green ammonia became more competitive.
</p>

<p>────── ♡ ──────</p>

<p>
  <a href="https://github.com/soph-k/ammonia-shock-analysis/blob/main/ammonia_notebook.ipynb">
    <strong>View Notebook »</strong>
  </a>
  &nbsp; • &nbsp;
  <a href="https://colab.research.google.com/github/soph-k/ammonia-shock-analysis/blob/main/ammonia_notebook.ipynb">
    <strong>Open in Colab »</strong>
  </a>
</p>

</div>

<br>

<!-- Table of Contents -->

## ❐ Table of Contents

<details>
<summary><strong>Quick Links</strong></summary>

<ol>
  <li><a href="#about-the-project">About the Project</a></li>
  <li><a href="#project-overview">Project Overview</a></li>
  <li><a href="#analysis-workflow">Analysis Workflow</a></li>
  <li><a href="#key-findings">Key Findings</a></li>
  <li><a href="#built-with">Built With</a></li>
  <li><a href="#data">Data</a></li>
  <li><a href="#getting-started">Getting Started</a></li>
  <li><a href="#limitations">Limitations</a></li>
  <li><a href="#acknowledgments">Acknowledgments</a></li>
</ol>

</details>

<br>

<!-- About -->

<div id="about-the-project"></div>

## ❐ About the Project

This project analyzes the relationship between U.S. natural gas prices and
ammonia-related producer prices before and after major geopolitical disruptions.

The notebook combines statistical analysis and machine learning to explore:

- How ammonia-related prices changed across major market periods
- Whether ammonia prices became more closely tied to natural gas during disruptions
- Whether unsupervised learning could identify high-price market regimes
- Which months showed statistically unusual price behavior
- When estimated conventional ammonia costs approached published green-ammonia costs

> **Why it matters:** ammonia production is closely tied to energy costs, so disruptions in natural gas markets can influence fertilizer prices and the relative competitiveness of green ammonia.

<p align="right">(<a href="#top">back to top</a>)</p>

<br>

<!-- Project Overview -->

<div id="project-overview"></div>

## ❐ Project Overview

<p align="center">
  <a href="https://github.com/soph-k/ammonia-shock-analysis/blob/main/ammonia_notebook.ipynb">
    <img src="https://raw.githubusercontent.com/soph-k/logo/main/ammonia.png" width="72%" alt="Natural gas and ammonia prices across disruption periods" />
  </a>
</p>

<p align="center">
  <sub>Natural gas and ammonia-related prices across major geopolitical disruption periods</sub>
</p>

<br>

<p align="center">
  <img src="https://img.shields.io/badge/Observations-136-d9a07e?style=for-the-badge&amp;labelColor=123b3d" alt="136 observations" />
  <img src="https://img.shields.io/badge/Pearson%20Correlation-0.72-d9a07e?style=for-the-badge&amp;labelColor=123b3d" alt="0.72 Pearson correlation" />
  <img src="https://img.shields.io/badge/Market%20Regimes-2-d9a07e?style=for-the-badge&amp;labelColor=123b3d" alt="2 market regimes" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Anomalous%20Months-26-d9a07e?style=for-the-badge&amp;labelColor=123b3d" alt="26 anomalous months" />
  <img src="https://img.shields.io/badge/Competitive%20Months-6-d9a07e?style=for-the-badge&amp;labelColor=123b3d" alt="6 competitive months" />
</p>

### Market Periods

| Period | Description |
|---|---|
| **Pre-War** | Baseline market conditions before February 2022 |
| **2022 Russia–Ukraine** | Major energy and fertilizer disruption period |
| **2024–2025 Tension** | Intermediate post-shock market period |
| **2026 Hormuz** | Early observations during a second disruption period |

<p align="right">(<a href="#top">back to top</a>)</p>

<br>

<!-- Analysis Workflow -->

<div id="analysis-workflow"></div>

## ❐ Analysis Workflow

```mermaid
flowchart LR
    A["Raw Price Data"] --> B["Clean & Align Dates"]
    B --> C["Explore Market Trends"]

    C --> D["Correlation & Regression"]
    C --> E["K-Means Clustering"]
    C --> F["Anomaly Detection"]

    D --> G["Green Ammonia Cost Comparison"]
    E --> G
    F --> G

    G --> H["Interpret Results"]

    classDef teal fill:#123b3d,stroke:#d9a07e,color:#fffaf4,stroke-width:2px;
    classDef cream fill:#f7efe7,stroke:#d9a07e,color:#123b3d,stroke-width:2px;
    classDef rose fill:#d9a07e,stroke:#123b3d,color:#123b3d,stroke-width:2px;
    classDef final fill:#123b3d,stroke:#f2c5aa,color:#fffaf4,stroke-width:3px;

    class A,B teal;
    class C,D cream;
    class E,F rose;
    class G,H final;

    linkStyle default stroke:#d9a07e,stroke-width:2px;
```

### Methods

<p align="center">
  <code>Exploratory Data Analysis</code>
  &nbsp; • &nbsp;
  <code>Correlation</code>
  &nbsp; • &nbsp;
  <code>Regression</code>
  &nbsp; • &nbsp;
  <code>Lag Analysis</code>
</p>

<p align="center">
  <code>K-Means Clustering</code>
  &nbsp; • &nbsp;
  <code>Anomaly Detection</code>
  &nbsp; • &nbsp;
  <code>Cost Comparison</code>
</p>

<p align="right">(<a href="#top">back to top</a>)</p>

<br>

<!-- Key Findings -->

<div id="key-findings"></div>

## ❐ Key Findings

### 1. Prices increased sharply during the 2022 disruption

Both natural gas and ammonia-related producer prices rose substantially compared
with the pre-war period. The ammonia-related price index showed an especially
large increase.

### 2. The gas–ammonia relationship became stronger during disruption

Natural gas and ammonia-related prices had a strong overall positive relationship.
The period-specific analysis indicated that this relationship became stronger
during the 2022 market shock.

### 3. Elevated ammonia prices remained after gas prices declined

During 2024–2025, average natural gas prices moved closer to their earlier level,
while the ammonia-related producer-price index remained elevated.

### 4. Machine learning identified a high-price market regime

K-means clustering selected a two-cluster solution that separated typical market
conditions from observations associated with elevated prices.

### 5. Green ammonia became more competitive during price shocks

Estimated conventional ammonia costs remained below the green-ammonia range for
most of the analysis, but the gap narrowed during the highest-price periods.

<p align="right">(<a href="#top">back to top</a>)</p>

<br>

<!-- Built With -->

<div id="built-with"></div>

## ❐ Built With

<p align="center">
  <img src="https://img.shields.io/badge/Python-123b3d?style=for-the-badge&amp;logo=python&amp;logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/pandas-d9a07e?style=for-the-badge&amp;logo=pandas&amp;logoColor=white" alt="pandas" />
  <img src="https://img.shields.io/badge/NumPy-123b3d?style=for-the-badge&amp;logo=numpy&amp;logoColor=white" alt="NumPy" />
  <img src="https://img.shields.io/badge/SciPy-d9a07e?style=for-the-badge&amp;logo=scipy&amp;logoColor=white" alt="SciPy" />
  <img src="https://img.shields.io/badge/scikit--learn-123b3d?style=for-the-badge&amp;logo=scikitlearn&amp;logoColor=white" alt="scikit-learn" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Jupyter-d9a07e?style=for-the-badge&amp;logo=jupyter&amp;logoColor=white" alt="Jupyter Notebook" />
  <img src="https://img.shields.io/badge/Matplotlib-123b3d?style=for-the-badge" alt="Matplotlib" />
  <img src="https://img.shields.io/badge/Seaborn-d9a07e?style=for-the-badge" alt="Seaborn" />
  <img src="https://img.shields.io/badge/openpyxl-123b3d?style=for-the-badge" alt="openpyxl" />
  <img src="https://img.shields.io/badge/Git%20%26%20GitHub-d9a07e?style=for-the-badge&amp;logo=github&amp;logoColor=white" alt="Git and GitHub" />
</p>

<p align="center">
  <sub>Data analysis • Machine learning • Visualization • Reproducible research</sub>
</p>

<p align="right">(<a href="#top">back to top</a>)</p>

<br>

<!-- Data -->

<div id="data"></div>

## ❐ Data

| File | Description |
|---|---|
| `MHHNGSP.csv` | Monthly Henry Hub natural gas spot prices |
| `WPU0652013A.csv` | Producer Price Index for ammonia and related nitrogen compounds |
| `The importance of dynamic operation...xlsx` | Published green-ammonia production-cost estimates |

### Repository Structure

```text
ammonia-shock-analysis/
├── data/
│   ├── MHHNGSP.csv
│   ├── WPU0652013A.csv
│   └── The importance of dynamic operation and renewable energy source
│       on the economic feasibility of green ammonia.xlsx
├── ammonia_notebook.ipynb
└── README.md
```

<p align="right">(<a href="#top">back to top</a>)</p>

<br>

<!-- Getting Started -->

<div id="getting-started"></div>

## ▹ Getting Started

### ❐ Prerequisites

Make sure you have:

- Python 3.10 or newer
- Git
- Jupyter Notebook or JupyterLab

### ❐ Installation

Clone the repository:

```sh
git clone https://github.com/soph-k/ammonia-shock-analysis.git
cd ammonia-shock-analysis
```

Create a virtual environment:

```sh
python -m venv .venv
```

Activate it on Windows:

```powershell
.venv\Scripts\Activate.ps1
```

Activate it on macOS or Linux:

```sh
source .venv/bin/activate
```

Install the required libraries:

```sh
pip install pandas numpy scipy scikit-learn matplotlib seaborn openpyxl jupyter
```

Open the notebook:

```sh
jupyter notebook ammonia_notebook.ipynb
```

Run the notebook cells from top to bottom to reproduce the analysis.

<p align="right">(<a href="#top">back to top</a>)</p>

<br>

<!-- Limitations -->

<div id="limitations"></div>

## ❐ Limitations

- The producer-price series represents ammonia and related nitrogen compounds rather than a pure ammonia-only spot-price series.
- The conventional ammonia cost comparison is an estimate based on a price-index baseline.
- The early-2026 period contains only a small number of observations.
- Correlation and regression show relationships but do not prove that geopolitical events directly caused the observed price changes.
- Monthly data may hide shorter price movements occurring within each month.

<p align="right">(<a href="#top">back to top</a>)</p>

<br>

<!-- Acknowledgments -->

<div id="acknowledgments"></div>

## ▹ Acknowledgments

This project uses:

- Henry Hub Natural Gas Spot Price data
- U.S. Producer Price Index data
- Published green-ammonia techno-economic cost estimates
- Python’s data-analysis and machine-learning ecosystem

<br>

<div align="center">

<p>────── ♡ ──────</p>

<sub>✦ Analyze carefully • Explain clearly • Build responsibly ✦</sub>

</div>

<p align="right">(<a href="#top">back to top</a>)</p>