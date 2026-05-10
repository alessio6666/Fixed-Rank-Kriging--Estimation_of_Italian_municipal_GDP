# Fixed Rank Kriging (FRK) - Estimation of Italian municipal GDP

> **Spatial Statistics and Geostatistical Modeling for the [GRINS](https://grins.it/) Project**  

## Project Overview
This project, developed as part of the **GRINS** initiative, evaluates the socio-economic resilience of more than 7,900 Italian municipalities. Since official GDP data is unavailable at the municipal level, this work implements a **geostatistical downscaling** framework to produce granular estimates and analyze local capacity to absorb shocks and sustain development.

## Geostatistical Methodology
The methodological framework is divided into four main phases:

* **Social Growth Index (SGI)**: A composite indicator serving as a proxy for territorial resilience, based on the annual growth rates of GDP, Population, and GDP per capita.
* **Fixed-Rank Kriging (FRK)**: Used to project provincial-level GDP to the municipal level. The model combines systematic effects of covariates, such as population, employment, and fiscal capacity, with structured spatial random effects and fine-scale components.
* **LISA Maps (Local Indicators of Spatial Association)**: Analysis based on the *Local Moran's I* statistic to identify statistically significant spatial clusters (High-High, Low-Low) and map territorial interdependence.
* **Penalty-Adjusted Copeland Ranking**: A ranking procedure based on pairwise comparisons to classify resilience. A spatial penalty term incorporating the average values of neighboring territories was introduced to ensure temporal stability.

## Key Results
* **Spatial Dependence**: Results reveal strong positive spatial autocorrelation; territorial units are significantly influenced by the socio-economic conditions of their neighbors.
* **Resilience Leaders**: Provinces in the **Lombardy** region, particularly Milan, emerged as the most resilient areas in the country.
* **Temporal Dynamics (2019–2022)**: The Copeland assessment highlighted an increase in resilience scores in Northern Italy, contrasting with a decreasing trend in many Southern municipalities.

## 📂 Repository Structure
* [`docs/`](docs/): Complete academic documentation.
    * [`GRINS_Executive_Summary.pdf`](docs/GRINS_Executive_Summary.pdf): Detailed analysis of the mathematical framework and data sources.
    * [`Scientific_Poster.pdf`](docs/Scientific_Poster.pdf): Visual presentation of resilience patterns and FRK methodology.
* [`images/`](images/): Visualizations of LISA maps and correlation matrices.

---

## Authors
* [Alessio Pani](https://www.linkedin.com/in/alessio-pani-8739b93bb) (Team Leader)
* Miguel Gutierrez
* Luca Montalto
* Jumil Reyes
* Rahmat Perdana

**Supervisors**: Dr. Matteo Greco, Dr. Giacomo Milan, Prof. Francesca Ieva.

---
*Developed for the Applied Statistics course @ Politecnico di Milano (A.Y. 2024/2025).*
