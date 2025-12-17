# Descriptive Relationships Between Time-series Variables

A quantitative, visually characterized analysis of physiological trends across EEG time-series variables.

![GitHub stars](https://img.shields.io/github/stars/Abrar-Islam-Oitijjho/Descriptive-Relationships-Between-Time-series-Variables?style=social)
![GitHub forks](https://img.shields.io/github/forks/Abrar-Islam-Oitijjho/Descriptive-Relationships-Between-Time-series-Variables?style=social)
![GitHub issues](https://img.shields.io/github/issues/Abrar-Islam-Oitijjho/Descriptive-Relationships-Between-Time-series-Variables)
![GitHub pull requests](https://img.shields.io/github/issues-pr/Abrar-Islam-Oitijjho/Descriptive-Relationships-Between-Time-series-Variables)
![GitHub last commit](https://img.shields.io/github/last-commit/Abrar-Islam-Oitijjho/Descriptive-Relationships-Between-Time-series-Variables)

<p>
  <img src="https://img.shields.io/badge/language-Jupyter%20Notebook-orange" alt="Jupyter Notebook Badge">
  <img src="https://img.shields.io/badge/library-scikit--learn-blue" alt="scikit-learn Badge">
  <img src="https://img.shields.io/badge/library-numpy-blue" alt="NumPy Badge">
  <img src="https://img.shields.io/badge/library-pandas-blue" alt="Pandas Badge">
  <img src="https://img.shields.io/badge/library-matplotlib-11557c" alt="Matplotlib Badge">
  <img src="https://img.shields.io/badge/library-seaborn-4c72b0" alt="Seaborn Badge">
</p>

## Table of Contents

- [About](#about)
- [Features](#features)
- [Data](#data)
- [Method](#method)
- [Result](#result)
- [Quick Start](#quick-start)
- [Installation](#installation)
- [Project Structure](#project-structure)
- [Associated Publication](#associated-publication)
- [Contributing](#contributing)
- [Support](#support)
- [Acknowledgments](#acknowledgments)

## About

This repository presents a descriptive analysis of the relationships between the time series signals, Compensatory Reserve Index (RAP) and multiple intracranial and cerebrovascular physiological parameters derived from multimodal neuromonitoring data. The analysis focuses on characterizing how physiological variables behave across distinct RAP-defined states of cerebral compensatory reserve.

Physiological data are stratified into ordered RAP regimes representing preserved, transitional, and impaired compensatory reserve. Descriptive statistics and comparative visualizations are used to examine shifts in central tendency, dispersion, and distributional behavior across these regimes, providing insight into how cerebral dynamics evolve with worsening compensatory capacity.

The analysis is implemented in a Jupyter Notebook environment using standard scientific Python libraries, including NumPy, Pandas, SciPy, and Matplotlib. This work is intended as a descriptive and exploratory foundation for downstream statistical testing, multivariate analysis, and time-series modeling of cerebral physiological dynamics.

## Features

* 📊 **RAP-Based Stratification**: Segments physiological data into ordered compensatory reserve states using RAP thresholds.
* 📈 **Descriptive Statistical Analysis**: Computes central tendency and dispersion metrics across RAP regimes for multiple physiological variables.
* 🔍 **Comparative Distribution Analysis**: Examines shifts in distributions and variability as cerebral compensatory reserve deteriorates.
* 🧠 **Multimodal Physiological Integration**: Analyzes RAP alongside intracranial and cerebrovascular parameters derived from multimodal neuromonitoring.
* 🎨 **Clear Visualizations**: Generates clear comparative plots for physiological interpretation and reporting.
* 🧩 **Extensible Analytical Framework**: Designed to support downstream trend testing, multivariate analysis, and time-series modeling.


## Data

The Canadian High-Resolution Traumatic Brain Injury (CAHR-TBI) Research Collaborative Data was utilized.

#### 📊 Parameters

The analysis includes RAP alongside multiple intracranial pressure (ICP) and arterial blood pressure (ABP)-derived variables, including but not limited to:

* ICP
* MAP
* CPP
* AMP
* Cerebrovascular reactivity indices (e.g., PRx, PAx, RAC)
* Additional multimodal parameters where available

## Method

#### Descriptive Analysis Workflow

```text

Descriptive and Extended Characterization of RAP–Physiology Relationships
│
├── 1. Data Preparation
│   ├── Load preprocessed multimodal neuromonitoring datasets
│   └── Handle missing values and apply basic filtering
│
├── 2. RAP-Based Stratification
│   ├── Segment data into ordered compensatory reserve states:
│   │     • RAP < 0 (preserved reserve)
│   │     • 0 ≤ RAP ≤ 0.4 (transitional reserve)
│   │     • RAP > 0.4 (impaired reserve)
│
├── 3. Core Descriptive Analysis (Part 1)
│   ├── Compute central tendency metrics:
│   │     • Mean
│   │     • Median
│   ├── Quantify dispersion:
│   │     • Interquartile range (IQR)
│   │     • Variance / standard deviation
│   ├── Report sample sizes per RAP state
│   └── Establish baseline RAP-dependent physiological trends
│
├── 4. Core Comparative Visualization (Part 1)
│   ├── Generate comparative distribution plots across RAP states
│   ├── Identify directional shifts and changes in variability
│   └── Produce figures for core variables
│
├── 5. Extended Variable Analysis (Part 2)
│   ├── Incorporate additional intracranial and cerebrovascular parameters
│   ├── Maintain consistent preprocessing and RAP stratification
│   └── Expand multimodal physiological coverage
│
├── 6. Extended Descriptive and Comparative Analysis (Part 2)
│   ├── Recompute descriptive statistics for extended variable set
│   ├── Perform refined distributional comparisons across RAP states
│   └── Identify parameter-specific deviations or amplifications
│
├── 7. Extended Visualization Suite (Part 2)
│   ├── Generate additional comparative plots for extended variables
│   ├── Enable cross-variable visual assessment of RAP effects
│   └── Improve resolution of RAP-dependent physiological behavior

```

#### 🧠 RAP-Based Physiological Stratification

Physiological data are stratified into three RAP regimes:

* **RAP < 0**
  Preserved or optimal cerebral compensatory reserve

* **0 ≤ RAP ≤ 0.4**
  Transitional or intermediate compensatory reserve

* **RAP > 0.4**
  Impaired cerebral compensatory reserve



## Result

#### 📈 Key Observations

* Several physiological variables demonstrate **progressive shifts** across RAP regimes.
* Dispersion of key parameters often increases in the **RAP > 0.4** state, consistent with impaired autoregulatory control.
* Not all parameters exhibit monotonic behavior, highlighting the complexity of multimodal cerebral physiology.

These findings motivate formal trend testing and multivariate analysis in downstream work.

### AHC Dendrogram of Full Data (NIRS measures)
<p align="center">
  <img src="plots/ahc/M RAP and ICP.png" width="480">
</p>

---


## 📊 Data and Parameters


## 📁 Repository Structure

```text
.
├── Report4_corresponding_v1(descriptive_relationships).ipynb
├── README.md
```

---

## 🛠 Requirements

The notebook is written in Python and relies on standard scientific libraries:

* Python ≥ 3.7
* NumPy
* Pandas
* SciPy
* Matplotlib
* Seaborn

Exact versions can be adapted to local environments.

---

## ▶️ Usage

1. Clone the repository:

```bash
git clone https://github.com/your-username/your-repo-name.git
```

2. Open the notebook:

```bash
jupyter notebook Report4_corresponding_v1(descriptive_relationships).ipynb
```

3. Execute cells sequentially to reproduce analyses and figures.

---

## 🔗 Relation to Broader Work

This repository represents a **descriptive component** of a larger research framework investigating cerebral compensatory reserve in acute neural injury. It complements:

* Trend-based statistical testing (e.g., Jonckheere–Terpstra)
* Multivariate clustering and subgroup discovery
* Time-series and causal response modeling

---

## 📄 Citation

If you use or build upon this work, please cite the associated publications on RAP and multimodal cerebral monitoring by the author.

---

## 📬 Contact

**Abrar Islam**
Graduate Research Assistant, University of Manitoba
Research focus: Cerebral physiology, RAP analysis, time-series modeling, and artifact management
