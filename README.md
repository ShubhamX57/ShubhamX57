<h1 align="center">Shubham Shinde</h1>

<p align="center">
  <b>Scientific computing · numerical linear algebra · Bayesian inference</b><br>
  MSc Scientific Computing with Data Science, University of Bristol (2026)
</p>

<p align="center">
  <a href="https://shubhamx57.github.io/shubhamshinde.github.io/"><img src="https://img.shields.io/badge/Website-222?style=flat-square&logo=githubpages&logoColor=white" alt="Website"></a>
  <a href="mailto:shubham.edu.ms@gmail.com"><img src="https://img.shields.io/badge/Email-555?style=flat-square&logo=maildotru&logoColor=white" alt="Email"></a>
</p>

---

I work where numerical methods meet physical data. My focus is making scientific software **numerically reliable**: finding where an algorithm quietly breaks, explaining why, and fixing it without disturbing the cases that already work.

**Current interests:** ill-conditioned covariance estimation · uncertainty quantification · Bayesian model fitting for neutron scattering and molecular dynamics · verifiable computation

---

### 🔬 Research

#### Numerical stability of covariance inversion in kinisi &nbsp;·&nbsp; [`kappa-kinisi`](https://github.com/ShubhamX57/kappa-kinisi)
*MSc dissertation. Builds on McCluskey, Coles & Morgan, J. Chem. Theory Comput. 21, 79–87 (2025).*

[kinisi](https://github.com/kinisi-dev/kinisi) estimates diffusion coefficients from MD trajectories by fitting to a mean-squared-displacement covariance matrix. In a small fraction of fits that matrix becomes ill-conditioned, and the resulting estimates are wrong.

- Generated a **64,000-fit population**, which isolated **14 anomalous cases**
- Showed that the raw covariance can be **reconstructed** from what kinisi stores after its own repair step
- Traced each failure to a **single eigendirection**: replacing one direction out of 126 repaired every affected fit
- Designed an **adaptive eigenvalue floor**. It was validated not to distort healthy fits and to transfer to a different physical system
- Showed that the **bootstrap covariance is misleading** in this setting, using direct measurement of the true variance

`Python` `NumPy` `SciPy` `scipp` `eigendecomposition` `GLS`

#### Bayesian analysis of quasi-elastic neutron scattering &nbsp;·&nbsp; [`qens`](https://github.com/ShubhamX57/QENS) &nbsp;·&nbsp; [docs](https://qens.readthedocs.io/en/latest/)

An end-to-end Python library for QENS data from ISIS Mantid `.nxspe` files.

- Forward model **S(Q, ω)** combining Debye–Waller, translational diffusion (Fickian, Chudley–Elliott, Singwi–Sjölander) and isotropic/anisotropic rotation, convolved with a *measured* resolution kernel
- **Joint-Q likelihood** across all Q-bins, with NNLS amplitudes per bin
- Multi-start MAP, then **MCMC** (`emcee`) with automatic autocorrelation and Gelman–Rubin R̂ diagnostics
- Plug-in model registry, so new physics needs no changes to core code

`Bayesian inference` `MCMC` `emcee` `Read the Docs`

#### Verified numerical answers &nbsp;·&nbsp; [`scisolve`](https://github.com/ShubhamX57/scisolve)

A solver for ODEs, optimisation, fitting, linear algebra and statistics. Its one hard rule, **enforced in code**, is that every number in an answer must trace back to output computed in the same session. Each answer must also name the check it passed: analytic, independent method, limiting case, invariant, convergence or dimensional.

- 122 tests across Python 3.10–3.13, run in CI
- Known failure modes kept as **running tests**, so closing one forces it to be documented

---

### 🤝 Open source

- **[kinisi](https://github.com/kinisi-dev/kinisi)**: contributor to the Python package for estimating diffusion properties from molecular dynamics

---

### 📄 Publications

- **Shinde, S.** *et al.* (2023). *TITLE*. Journal of Emerging Technologies and Innovative Research (JETIR), VOL(ISSUE), PAGES. [link](#)

---

### 🧰 Toolkit

| | |
|---|---|
| **Numerical** | NumPy · SciPy · scipp · linear algebra · optimisation · ODEs |
| **Statistical** | Bayesian inference · MCMC (emcee) · bootstrap · uncertainty quantification |
| **Domain** | Molecular dynamics (kinisi) · neutron scattering (Mantid `.nxspe`) |
| **Engineering** | Python packaging · pytest · GitHub Actions · Sphinx / Read the Docs · conda |
| **ML** | Retrieval systems · reranking · evaluation ([`arxiv-rag`](https://github.com/ShubhamX57/arxiv-rag)) |

---

### 🎓 Background

- **MSc Scientific Computing with Data Science**, University of Bristol, 2026. SARTHI Maharashtra Government Foreign Scholarship; elected Student Academic Representative
- **BE Mechanical Engineering**, Savitribai Phule Pune University, 2020
- Previously in ML research (Spartifical) and in engineering roles in industry

<p align="center"><sub>Open to research software, scientific computing and PhD opportunities. Get in touch.</sub></p>
