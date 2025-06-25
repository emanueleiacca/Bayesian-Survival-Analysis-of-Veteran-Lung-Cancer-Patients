# Bayesian Survival Analysis of Veteran Lung Cancer Patients

This project presents a comprehensive Bayesian survival analysis of the Veteran's Administration Lung Cancer Trial dataset using parametric models. The work was completed as a final project for the SMDS-2-2024-2025 course.

---

## 📊 Dataset

The data used is from the `survival` R package (`veteran` dataset), originally from a clinical trial studying the survival of male patients with advanced inoperable lung cancer. It includes:

- **Time-to-event** data (in days)
- **Censoring indicator** (1 = event, 0 = censored)
- **Covariates**: cell type, treatment type, Karnofsky score, age, time since diagnosis, prior therapy

---

## 🎯 Objectives

- Apply fully Bayesian methods to model survival data with censoring
- Compare the exponential and Weibull AFT models using DIC
- Perform posterior inference on covariate effects
- Conduct posterior predictive checks to assess model fit
- Validate model performance via parameter recovery simulations
- Compare Bayesian results with frequentist survival models (Cox PH, parametric AFT)

---

## 🧠 Methods

- **Bayesian MCMC estimation** using JAGS via `rjags`
- **Exponential and Weibull AFT models** fit to the full dataset
- **Model comparison** via Deviance Information Criterion (DIC)
- **Posterior predictive checks** using simulated survival curves
- **Parameter recovery experiments** to evaluate identifiability
- **Frequentist comparison** using `survreg()` and `coxph()` from the `survival` package

---

## 📌 Key Results

- **Weibull AFT model** provided the best fit (lowest DIC)
- Cell type significantly impacted survival:
  - Adenocarcinoma and small-cell types showed markedly worse prognosis
- **Treatment effect** was not significant
- Posterior predictive checks confirmed good model calibration
- Recovery experiments demonstrated that β parameters are identifiable; shape is moderately harder to recover

---

## 📦 File Structure

- `main.Rmd` — complete RMarkdown analysis script
- `exponential_aft.jags`, `weibull_aft.jags` — JAGS model definitions
- `plots/` — folder for all generated figures (KM curves, posterior checks, etc.)
- `README.md` — project summary

---

## 🧾 Reproducibility

To reproduce the analysis:

1. Open the `.Rmd` file in RStudio
2. Run all chunks sequentially (requires packages: `survival`, `rjags`, `coda`, `mcmcplots`, `ggplot2`, `bayesplot`)
3. JAGS must be installed and available in your system path

---

## 📚 References

- Gelman et al. (2013). *Bayesian Data Analysis*
- Ntzoufras (2010). *Bayesian Modeling Using WinBUGS*
- Kalbfleisch and Prentice (2002). *The Statistical Analysis of Failure Time Data*

---

## 🧑‍🏫 Author

**Author**: [Emanuele Iaccarino]
