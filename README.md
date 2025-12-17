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
│   │     • 0 ≤ RAP ≤ 0.4 (intact or transitional reserve)
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
├── 4. Core Comparative Visualization
│   ├── Generate comparative distribution plots across RAP states
│   └── Produce figures for core variables
│
├── 6. Statistical Comparison Across RAP States
│ ├── Apply non-parametric group comparison tests
│ │       • Across RAP-defined states
  │       • Across other parameter thresholds
│ ├── Assess statistical significance of distributional differences
│ └── Report p-values for physiological parameters
│
├── 5. Temporal Burden Analysis (Part 2)
│ └── Compute percentage of monitoring time spent:
│ │     • Within each RAP state
│ │     • Within other parameter thresholds (reverse %time spent)

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

### Piecewise Linear Regression

#### RAP vs Different Parameters

<table>
  <tr>
    <td><img src="plots/Piece_wise_linear_regression/M RAP and ICP.png"></td>
    <td><img src="plots/Piece_wise_linear_regression/M RAP and PRx.png"></td>
  </tr>
  <tr>
    <td align="center">RAP vs ICP</td>
    <td align="center">RAP vs PRx</td>
  </tr>
</table>

#### Lower Resolutions (RAP vs ICP)

<table>
  <tr>
    <td><img src="plots/Piece_wise_linear_regression/H RAP and ICP.png"></td>
    <td><img src="plots/Piece_wise_linear_regression/D RAP and ICP.png"></td>
  </tr>
  <tr>
    <td align="center">1-hour</td>
    <td align="center">1-day</td>
  </tr>
</table>

### Boxplots

#### RAP vs Different Parameters

<table>
  <tr>
    <td><img src="plots/Boxplots/M RAP and ICP.png"></td>
    <td><img src="plots/Boxplots/M RAP and PRx.png"></td>
  </tr>
  <tr>
    <td align="center">RAP vs ICP</td>
    <td align="center">RAP vs PRx</td>
  </tr>
</table>

#### Lower Resolutions (RAP vs ICP)

<table>
  <tr>
    <td><img src="plots/Boxplots/H RAP and ICP.png"></td>
    <td><img src="plots/Boxplots/D RAP and ICP.png"></td>
  </tr>
  <tr>
    <td align="center">1-hour</td>
    <td align="center">1-day</td>
  </tr>
</table>

---

### Median physiology measures across the RAP states with formal comparison 

| Parameter        | RAP < 0 (IQR)           | 0 ≤ RAP ≤ 0.4 (IQR)     | RAP > 0.4 (IQR)          | p-value  |
| ---------------- | ----------------------- | ----------------------- | ------------------------ | -------- |
| RAP              | -0.234 (-0.458 – -0.10) | 0.239 (0.134 – 0.326)   | 0.873 (0.722 – 0.949)    | 3.05e-19 |
| ICP              | 12.03 (7.70 – 17.30)    | 12.06 (7.89 – 16.75)    | 13.71 (9.70 – 18.14)     | 0.021    |
| AMP              | 0.913 (0.362 – 1.822)   | 1.081 (0.506 – 2.119)   | 1.93 (1.174 – 3.052)     | 3.94e-09 |
| MAP              | 90.06 (79.64 – 100.10)  | 89.66 (80.11 – 98.90)   | 89.46 (81.44 – 97.85)    | 0.008    |
| CPP              | 76.69 (66.38 – 87.20)   | 76.63 (67.04 – 86.90)   | 75.07 (67.58 – 83.53)    | 0.638    |
| PRx              | 0.271 (-0.078 – 0.638)  | 0.233 (-0.064 – 0.548)  | 0.047 (-0.238 – 0.360)   | 0.035    |
| PAx              | -0.147 (-0.423 – 0.107) | -0.015 (-0.250 – 0.200) | -0.030 (-0.314 – 0.272)  | 0.184    |
| RAC              | -0.060 (-0.364 – 0.214) | -0.103 (-0.336 – 0.126) | -0.485 (-0.739 – -0.131) | 1.00e-04 |
| rSO₂_L           | 69.29 (62.67 – 76.49)   | 69.03 (62.54 – 76.39)   | 68.02 (62.08 – 74.94)    | 0.093    |
| rSO₂_R           | 71.01 (64.33 – 78.32)   | 71.96 (64.53 – 78.16)   | 71.29 (64.57 – 77.71)    | 0.152    |
| COx_L            | 0.076 (-0.172 – 0.350)  | 0.058 (-0.159 – 0.298)  | 0.009 (-0.215 – 0.234)   | 0.170    |
| COx_R            | 0.085 (-0.166 – 0.352)  | 0.066 (-0.150 – 0.301)  | 0.013 (-0.206 – 0.233)   | 0.508    |
| COxA_L           | 0.115 (-0.140 – 0.402)  | 0.085 (-0.140 – 0.323)  | 0.065 (-0.150 – 0.280)   | 0.669    |
| COxA_R           | 0.110 (-0.141 – 0.395)  | 0.084 (-0.138 – 0.320)  | 0.059 (-0.146 – 0.268)   | 0.827    |
| PbtO<sub>2</sub> | 24.00 (17.31 – 30.56)   | 21.66 (15.01 – 29.00)   | 24.67 (17.24 – 32.00)    | 0.819    |

---

### % time spent within the thresholds of the parameters (Example: ICP) across the RAP states

#### ICP Threshold: 20 mmHg

| RAP State     | ICP < 20                 | ICP ≥ 20               |
| ------------- | ------------------------ | ---------------------- |
| RAP < 0       | 91.29% (75.06% – 99.03%) | 8.71% (0.97% – 24.94%) |
| 0 ≤ RAP ≤ 0.4 | 94.11% (79.50% – 99.14%) | 5.89% (0.86% – 20.50%) |
| RAP > 0.4     | 95.07% (80.42% – 99.38%) | 4.93% (0.62% – 19.58%) |

#### ICP Threshold: 22 mmHg

| RAP State     | ICP < 22                  | ICP ≥ 22               |
| ------------- | ------------------------- | ---------------------- |
| RAP < 0       | 95.50% (84.62% – 100.00%) | 4.50% (0.00% – 15.38%) |
| 0 ≤ RAP ≤ 0.4 | 96.98% (89.06% – 99.69%)  | 3.02% (0.31% – 10.94%) |
| RAP > 0.4     | 97.92% (89.57% – 99.80%)  | 2.08% (0.20% – 10.43%) |

---

# Quick Start

Clone the repository and run the main script:

```bash
git clone https://github.com/Abrar-Islam-Oitijjho/Descriptive-Relationships-Between-Time-series-Variables.git
cd Time-Series-Covariance-Pattern-Analysis
pip install -r requirements.txt
jupyter notebook covariance_pattern_analysis_main(with_sub_group_resolution).ipynb
```

## Installation

### 🛠 Requirements

The notebook is written in Python and relies on standard scientific libraries:

* Python ≥ 3.7
* NumPy
* Pandas
* SciPy
* Matplotlib
* Seaborn

Exact versions can be adapted to local environments.

## Project Structure

```
Descriptive-Relationships-Between-Time-series-Variables/
├── code/
    ├── descriptive_relationships_part1.ipynb       # core variables, basic descriptive analysis          
    └── descriptive_relationships_part2.ipynb       # extended variables, advancced descriptive analysis     
├── plots/
    ├── Piece_wise_linear_regression        
    ├── Boxplots
    └── Contour_plots
├── README.md              
└── requirements.txt                 
```

### ▶️ Usage

1. Clone the repository:

```bash
git clone https://github.com/your-username/your-repo-name.git
```

2. Open the notebook:

```bash
jupyter notebook descriptive_relationships_part1.ipynb
```

3. Execute cells sequentially to reproduce analyses and figures.

---

## Associated Publication

For more information please visit: [Relationship Between RAP and Multi-Modal Cerebral Physiological Dynamics in Moderate/Severe Acute Traumatic Neural Injury: A CAHR-TBI Multivariate Analysis](https://www.mdpi.com/2306-5354/12/9/1006)

#### 📄 Citation

If you use or build upon this work, please cite the associated publications on RAP and multimodal cerebral monitoring by the author.

---

## Contributing

Contributions are welcome!

### Quick Contribution Steps
1. 🍴 Fork the repository
2. 🌟 Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. ✅ Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. 📤 Push to the branch (`git push origin feature/AmazingFeature`)
5. 🔃 Open a Pull Request

## Support

- 📧 **Email**: abraroitijjho35@gmail.com
- 🐛 **Issues**: [GitHub Issues](https://github.com/Abrar-Islam-Oitijjho/Descriptive-Relationships-Between-Time-series-Variables/issues)

## Acknowledgments

- 📚 **Libraries used**:
  - [NumPy](https://numpy.org/) - Numerical computing library
  - [Pandas](https://pandas.pydata.org/) - Data analysis library
  - [Matplotlib](https://matplotlib.org/) - Visualization library
  - [Statsmodels](https://www.statsmodels.org/stable/index.html) - Statistical modeling library
  - [Scikit-learn](https://scikit-learn.org/stable/) - Machine learning library
    
🌟 Special thanks: to the Main-Hub Laboratory, University of Manitoba, for their great support.
