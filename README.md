# Statistical Analysis of Uniaxial Tensile and Fatigue Data of Ti-685 Alloy

A probabilistic machine learning and reliability analysis project focused on evaluating the mechanical behavior and fatigue life of **Ti-685 alloy** under varying thermal conditions for aerospace gas turbine applications.

Developed using **Python**, **Jupyter Notebook**, and **Streamlit** under the guidance of **Dr. Surajit Kumar Paul**.

---

# Overview

This project performs **statistical and probabilistic analysis** on experimental tensile and fatigue datasets of **Ti-685 alloy**, with the objective of assessing its suitability as a substitute for conventional **α-Ti alloys** used in jet engine structures.

The study combines:

* Statistical distribution fitting
* Probabilistic life prediction
* Reliability engineering concepts
* Fatigue bound curve estimation
* Temperature dependent material behavior analysis
* Interactive visualization through Streamlit

The project aims to provide an engineer-friendly framework for:

* Reliability assessment
* Safety factor optimization
* Material comparison
* Failure probability estimation
* Fatigue life prediction under thermal loading

---

# Project Objectives

* Analyze uniaxial tensile and fatigue data of Ti-685 alloy
* Model fatigue life variability using probabilistic distributions
* Quantify uncertainty and failure risk
* Compute confidence and bound curves for engineering design
* Compare Ti-685 alloy with standard alpha titanium alloys
* Develop a reusable reliability analysis workflow
* Create an interactive Streamlit application for engineers

---

# Key Features

## Statistical Distribution Modeling

Implemented and compared multiple statistical distributions:

* Weibull Distribution
* 3-Parameter Weibull Distribution
* Gamma Distribution
* Gumbel Distribution
* Lognormal Distribution
* Power-Law based probabilistic models

These models were used to characterize:

* Tensile strength variability
* Fatigue life distribution
* Reliability trends
* Failure probability behavior

---

## Temperature Dependent Analysis

Developed models for:

* Arrhenius temperature dependence
* Linear temperature dependence
* Thermal degradation trends
* Fatigue behavior under varying operating temperatures

This helps simulate real-world gas turbine operating environments.

---

## Reliability & Risk Quantification

The project estimates:

* Probability of failure
* Reliability curves
* Confidence intervals
* Fatigue bound curves
* Safety margins
* Life prediction uncertainty

These analyses are critical in aerospace structural design.

---

## Interactive Streamlit Application

Built a user-friendly web application that allows engineers to:

* Upload fatigue/tensile datasets
* Select statistical models
* Visualize fitted distributions
* Generate reliability plots
* Compare probabilistic models dynamically
* Analyze thermal effects interactively

---

# Tech Stack

| Technology       | Purpose                    |
| ---------------- | -------------------------- |
| Python           | Core programming           |
| Jupyter Notebook | Research & experimentation |
| Streamlit        | Interactive dashboard      |
| NumPy            | Numerical computation      |
| Pandas           | Data handling              |
| SciPy            | Statistical modeling       |
| Matplotlib       | Visualization              |
| Plotly           | Interactive plots          |
| Scikit-learn     | ML utilities               |

---

# Repository Structure

```bash
├── 3_param_weibull_dist_const_shape_param.ipynb
├── fcgr2-only_temp_dependent-arrhenius.ipynb
├── fcgr2-only_temp_dependent-linear.ipynb
├── Gamma_dist.ipynb
├── Gumbel_distribution.ipynb
├── lognormal_dist_const_var.ipynb
├── lognormal_dist_const_var_PowerLaw.ipynb
├── weibull_dist_const_shape_param.ipynb
├── weibull_dist_const_shape_param-PowerLaw.ipynb
├── FCGR-NML.xlsx
├── app.py
├── requirements.txt
└── README.md
```

---

# Statistical Models Used

# Statistical Distributions & Models in Fatigue Analysis

## Weibull Distribution
Widely used in **reliability engineering** and **fatigue analysis**.

**Applications:**
- Failure probability estimation  
- Reliability prediction  
- Fatigue life modeling  

**Probability Density Function (PDF):**

$$
f(x) = \frac{\beta}{\eta} \left(\frac{x}{\eta}\right)^{\beta - 1} e^{-\left(\frac{x}{\eta}\right)^\beta}
$$

Where:  
- $\beta$ = shape parameter  
- $\eta$ = scale parameter  

---

## Lognormal Distribution
Used to model **multiplicative fatigue variability** and **crack growth behavior**.

**Probability Density Function (PDF):**

$$
f(x) = \frac{1}{x\sigma\sqrt{2\pi}} \exp\left(-\frac{(\ln x - \mu)^2}{2\sigma^2}\right)
$$

Where:  
- $\mu$ = mean of log values  
- $\sigma$ = standard deviation of log values  

---

## Arrhenius Temperature Model
Used to study **thermal dependency of fatigue behavior**.

$$
k = A e^{-\frac{E_a}{R T}}
$$

Where:  
- $E_a$ = activation energy  
- $R$ = gas constant  
- $T$ = absolute temperature

# Probabilistic Models for Fatigue Life Prediction

This repository implements several probabilistic models for analyzing tensile and fatigue data of Ti-685 alloy.

---

## Three-Parameter Weibull Distribution
**CDF:**

$$
F(x) = 1 - \exp\left[-\left(\frac{x-\theta}{\eta}\right)^\beta\right]
$$

**PDF:**
$$
f(x) = \frac{\beta}{\eta}\left(\frac{x-\theta}{\eta}\right)^{\beta-1}
       \exp\left[-\left(\frac{x-\theta}{\eta}\right)^\beta\right]
$$

**Significance:** Used in [reliability prediction](ca://s?q=Weibull_distribution_in_reliability) and fatigue life modeling.

---

## Weibull Distribution with Power Law
**CDF:**
$$
F(x) = 1 - \exp\left[-\left(\frac{x}{\eta}\right)^\beta\right]
$$

**Fatigue Life Model:**
$$
N_f = \exp\left(Ut + W_t \ln(T) + \frac{1}{\beta}\ln\ln\frac{1}{1-F(x)}\right)
$$

**Significance:** Captures [power-law scaling](ca://s?q=Power_law_in_fatigue) in crack growth.

---

## Lognormal Distribution
**PDF:**
$$
f(x) = \frac{1}{(x-\gamma)\sigma\sqrt{2\pi}}
       \exp\left[-\frac{\big(\ln(x-\gamma)-\mu\big)^2}{2\sigma^2}\right]
$$

**Significance:** Models [multiplicative variability](ca://s?q=Lognormal_distribution_in_fatigue) in fatigue and crack growth.

---

## Gumbel Distribution
**CDF:**
$$
F(x) = \exp\left[-\exp\left(-\frac{x-\mu}{\beta}\right)\right]
$$

**Significance:** Useful for [extreme value analysis](ca://s?q=Gumbel_distribution_in_reliability), predicting weakest-link failures.

---

## Gamma Distribution
**PDF:**
$$
f(x) = \frac{1}{\Gamma(k)\theta^k} \, x^{k-1} e^{-x/\theta}
$$

**Significance:** Applied in [lifetime modeling](ca://s?q=Gamma_distribution_in_reliability) when failure rates vary over time.



## 2. Data Preprocessing

* Missing value handling
* Outlier analysis
* Normalization
* Temperature categorization
* Feature extraction

---

## 3. Distribution Fitting

Each dataset is fitted against multiple probability distributions to determine:

* Best fit behavior
* Reliability trends
* Material uncertainty characteristics

Metrics used:

* RMSE
* Log-likelihood
* Goodness-of-fit
* Visual comparison

---

## 4. Reliability Analysis

Computed:

* Survival probability
* Hazard functions
* Reliability curves
* Failure distributions
* Bound curves

---

## 5. Comparative Material Analysis

Compared Ti-685 alloy performance against:

* Conventional alpha titanium alloys
* Industry fatigue standards
* Aerospace material reliability benchmarks

---

# Streamlit Dashboard

The Streamlit app provides:

## Features

* Interactive dataset upload
* Statistical model selection
* Dynamic curve fitting
* Reliability visualization
* Thermal condition comparison
* Fatigue life estimation

## Run Locally

```bash
streamlit run app.py
```

---

# Installation

## Clone Repository

```bash
git clone https://github.com/your-username/ti685-fatigue-analysis.git
cd ti685-fatigue-analysis
```

## Install Dependencies

```bash
pip install -r requirements.txt
```

---

# Requirements

Example dependencies:

```txt
numpy
pandas
scipy
matplotlib
plotly
streamlit
scikit-learn
openpyxl
```

---

# Sample Outputs

The project generates:

* Weibull probability plots
* Reliability curves
* Fatigue life distributions
* Confidence bound curves
* Temperature dependent trend plots
* Interactive dashboards

---

# Engineering Applications

This work is relevant for:

* Aerospace structural design
* Jet engine reliability
* Fatigue life prediction
* Material qualification
* Reliability-centered maintenance
* Safety factor optimization
* Failure risk assessment

---

# Results & Insights

* Ti-685 alloy demonstrated promising fatigue reliability characteristics under varying thermal conditions.
* Probabilistic modeling improved understanding of uncertainty in fatigue life prediction.
* Weibull and Lognormal models provided effective fitting for fatigue datasets.
* Thermal effects significantly influenced crack growth behavior and life prediction.
* The developed framework can support aerospace material selection and reliability engineering workflows.

---

## Data Confidentiality Notice
The datasets used in this project (Ti-685 alloy tensile and fatigue data) are **confidential** and are **NOT included** in this repository.  
They are proprietary to the research group and cannot be shared, copied, or redistributed.  

This repository provides **code, models, and documentation only**.  
Users may run the code with their own datasets, but the original data is restricted.


# Future Improvements

* Integration of deep learning based life prediction
* Bayesian reliability analysis
* Monte Carlo simulation for uncertainty propagation
* Real time sensor data integration
* Digital twin integration for aerospace systems
* Deployment on cloud platforms

---

# Author

**Chiranjeeb Debata**
B.Tech Mechanical Engineering
---

# Acknowledgment

Special thanks to **Dr. Surajit Kumar Paul** for guidance and mentorship throughout the project.

---

# License

This project is intended for academic and research purposes.
