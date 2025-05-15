
Below is a plug‑and‑play template that meets all eight elements, pairs each learning goal with readings from ***An Introduction to Statistical Learning (ISLR, 2e)*** and ***Probabilistic Machine Learning (PML, 2022/23)***, and splits an eight‑week program into **4 weeks of guided learning** and **4 weeks of team implementation**.

---

## 1  Program Snapshot

| Item                   | Specification                                                                                                                                                                                                                                      |
| ---------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Title**              | Statistical Learning & Implementation Internship                                                                                                                                                                                                   |
| **Cohort**             | 5 graduate‑level interns (probability + Python prerequisite)                                                                                                                                                                                       |
| **Calendar**           | 8 weeks (Mon 12 May → Fri 4 Jul 2025), \~30 hrs/week <br> • Morning: 2 h theory + lab (Mon‑Thu) <br> • Afternoon: 4 h project / self‑study                                                                                                         |
| **End‑products**       | Reproducible codebase (GitHub), technical report, slide deck, recorded demo                                                                                                                                                                        |
| **Primary texts**      | ISLR 2e (James et al., 2023) ([An Introduction to Statistical Learning](https://www.statlearning.com/?utm_source=chatgpt.com))  ·  PML Books 1&2 (Murphy, 2022‑23) ([probml.github.io](https://probml.github.io/pml-book/?utm_source=chatgpt.com)) |
| **Stack**              | Python 3.11, conda env, pandas, scikit‑learn, matplotlib, seaborn, PyMC/NumPyro, GitHub Projects, Docker, JupyterHub (on IITM GPU node or Colab)                                                                                                   |
| **Capstone theme**     | “End‑to‑end predictive modelling on a public health‑care cost dataset” (regression + uncertainty quantification)                                                                                                                                   |
| **Mentoring rhythm**   | Daily stand‑up (10 min), Weekly code‑review (Wed), Mid‑term demo (end W4), Final rehearsal (W8‑Wed)                                                                                                                                                |
| **Evaluation weights** | Technical accuracy 30 % · Statistical rigour 20 % · Reproducibility & docs 15 % · Teamwork 15 % · Communication 10 % · Creativity 10 %                                                                                                             |

---

## 2  Eight‑Week Road‑Map

| Wk    | Focus & Objectives                                                                                              | Required Reading†                    | Hands‑on / Deliverables                                                                 |
| ----- | --------------------------------------------------------------------------------------------------------------- | ------------------------------------ | --------------------------------------------------------------------------------------- |
| **1** | *Foundations* – bias‑variance, linear regression, Python/conda, Git basics                                      | ISLR Ch 2‑3; PML 1 §1.1‑1.4          | Notebook: EDA + OLS on Boston Housing; pair‑programming k‑fold CV                       |
| **2** | *Classification* – logistic reg., k‑NN, evaluation metrics (ROC/AUC)                                            | ISLR Ch 4; PML 1 §5.1‑5.3            | Notebook: compare logistic vs. k‑NN on Heart Disease data; write modular pipeline       |
| **3** | *Model Selection & Regularisation* – ridge, lasso, elastic‑net, feature engineering, cross‑validation theory    | ISLR Ch 6; PML 1 §8.1‑8.3            | Script: grid‑search ridge/lasso; blog‑style markdown explaining bias‑variance trade‑off |
| **4** | *Non‑linear & Ensemble Methods* – trees, bagging, RF, boosting; intro to Bayesian linear models                 | ISLR Ch 8‑9; PML 1 §9.1; PML 2 §16.1 | Mini‑project: tune XGBoost vs. RF; Mid‑term group demo (15 min)                         |
| **5** | *Capstone Kick‑off* – define problem, data pipeline, roles (Data, Modelling, Validation, MLOps, Docs)           | PML 1 §2.2 (prob. modelling intro)   | PR #1: data‑cleaning module + schema tests; project plan (Kanban board)                 |
| **6** | *Probabilistic Modelling* – Bayesian linear/logistic regression, Gaussian processes, VI vs. MCMC                | PML 1 §10.1‑10.4; PML 2 §18.1‑18.3   | PR #2: PyMC or NumPyro model; uncertainty plots; peer code‑review                       |
| **7** | *Validation & Refinement* – posterior predictive checks, hyper‑parameter inference, model comparison (WAIC/LOO) | PML 2 §20.1‑20.3                     | PR #3: evaluation report; reproducible Docker image; dry‑run presentation               |
| **8** | *Delivery* – reproducible build, GitHub Actions, slide deck, rehearsed talk                                     | (No new chapters; polish docs)       | Final demo to faculty; 12‑page report; retrospective & feedback survey                  |

†Each reading block is \~40 pages plus one recommended ISLR lab section; interns skim ahead only if time permits.

---

## 3  Project & Role Breakdown

| Role (1 per intern)    | Main Duties                                                    | Key Tools                     |
| ---------------------- | -------------------------------------------------------------- | ----------------------------- |
| **Data Lead**          | Acquire, clean, version raw data; document schemas             | pandas, Great Expectations    |
| **Modelling Lead**     | Implement baseline & advanced models; maintain metrics         | scikit‑learn, PyMC            |
| **Validation Lead**    | Design CV splits, PPCs, diagnostics; ensure statistical rigour | ArviZ, matplotlib             |
| **MLOps Lead**         | CI/CD, Docker image, GitHub Actions, experiment tracking       | Docker, DVC                   |
| **Documentation Lead** | Write user guide, API docstrings, final report & slides        | Sphinx/Markdown, LaTeX Beamer |

Roles rotate weekly for cross‑training.

---

## 4  Mentorship & Checkpoints

| Time‑point  | Activity                                             | Outcome                             |
| ----------- | ---------------------------------------------------- | ----------------------------------- |
| Daily 10:00 | 10‑min stand‑up                                      | Blockers surfaced early             |
| Wed 15:00   | Code‑review & “journal club” (1 paper from ISLR/PML) | Code quality + literature awareness |
| **End W4**  | Mid‑term demo (15 min)                               | Green‑light to proceed              |
| **End W8**  | Final presentation (25 min) + Q\&A to faculty panel  | Summative assessment                |

---

## 5  Assessment Rubric (100 pts total)

| Criterion              | Weight | Indicators                                   |
| ---------------------- | ------ | -------------------------------------------- |
| Technical correctness  | 30     | Working code, passes tests, sound statistics |
| Statistical rigour     | 20     | Proper diagnostics, justified assumptions    |
| Reproducibility & docs | 15     | Clean repo, env.yml, README, API docs        |
| Teamwork               | 15     | PR etiquette, peer reviews, shared ownership |
| Communication          | 10     | Clear slide deck, confident delivery         |
| Creativity             | 10     | Novel features, insightful error analysis    |

---

### How to Deploy this Template

1. **Fill dates/names** in sections above.
2. **Create a GitHub organisation** with a blank project board; pre‑configure issue templates matching each week’s deliverables.
3. **Provision compute** (JupyterHub on IITM GPU node or Colab Pro credits).
4. **Kick‑off meeting (Day 1)**: walk interns through this document, assign initial roles, and clone starter repository.
5. **Iterate**—adjust weekly scope if interns move faster/slower; swap datasets if domain change needed.

This design keeps theory tightly coupled to practice, leverages ISLR for approachable statistical learning, and layers PML’s Bayesian perspective during the project phase—giving interns both classical and probabilistic toolkits within eight focused weeks.
