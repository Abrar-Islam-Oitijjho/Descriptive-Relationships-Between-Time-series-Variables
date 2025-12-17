# Descriptive Relationships Between RAP and Cerebral Physiological Variables

This repository presents a descriptive analysis of the relationships between the EEG time series variables, the Compensatory Reserve Index (RAP) and multiple key cerebrovascular physiological parameters derived from multimodal neuromonitoring data. The analysis focuses on characterizing how physiological variables behave across distinct RAP-defined states of cerebral compensatory reserve.

---

## 📌 Objective

The primary objective of this work is to quantitatively and visually characterize physiological trends across RAP regimes, providing insight into how cerebral dynamics evolve as compensatory reserve deteriorates.

This repository emphasizes **descriptive and relational analysis**, serving as a foundation for subsequent inferential and multivariate modeling.

---

## 🧠 RAP-Based Physiological Stratification

Physiological data are stratified into three RAP regimes:

* **RAP < 0**
  Preserved or optimal cerebral compensatory reserve

* **0 ≤ RAP ≤ 0.4**
  Transitional or intermediate compensatory reserve

* **RAP > 0.4**
  Impaired cerebral compensatory reserve

These regimes are treated as **ordered physiological states**, reflecting progressive impairment rather than independent categories.

---

## 📊 Data and Parameters

The analysis includes RAP alongside multiple intracranial pressure (ICP) and arterial blood pressure (ABP)-derived variables, including but not limited to:

* ICP
* MAP
* CPP
* AMP
* Cerebrovascular reactivity indices (e.g., PRx, PAx, RAC)
* Additional multimodal parameters where available

All data are assumed to be **preprocessed and artifact-managed prior to analysis**.

---

## 🔍 Methodology

The notebook implements the following analytical steps:

1. **Data Loading and Cleaning**

   * Import preprocessed physiological datasets
   * Handle missing values and filtering

2. **RAP-Based Segmentation**

   * Partition observations into three RAP regimes

3. **Descriptive Statistical Analysis**

   * Compute central tendency (mean, median)
   * Quantify dispersion (IQR, variance, standard deviation)
   * Report sample sizes per RAP regime

4. **Visualization**

   * Distribution and comparative plots across RAP regimes
   * Visual assessment of directional trends and variability

5. **Physiological Interpretation**

   * Qualitative interpretation of observed trends
   * Identification of parameters showing monotonic or destabilizing behavior with increasing RAP

---

## 📈 Key Observations

* Several physiological variables demonstrate **progressive shifts** across RAP regimes.
* Dispersion of key parameters often increases in the **RAP > 0.4** state, consistent with impaired autoregulatory control.
* Not all parameters exhibit monotonic behavior, highlighting the complexity of multimodal cerebral physiology.

These findings motivate **formal trend testing and multivariate analysis** in downstream work.

---

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
