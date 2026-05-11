# Fixed Rank Kriging (FRK) - Estimation of Italian municipal GDP

> **Spatial Statistics and Geostatistical Modeling for the [GRINS](https://grins.it/) Project**  

## Project Overview
This project, developed as part of the **GRINS** initiative, evaluates the socio-economic resilience of more than 7,900 Italian municipalities. Since official GDP data is unavailable at the municipal level, this work implements a **geostatistical downscaling** framework to produce granular estimates and analyze local capacity to absorb shocks and sustain development.

## Geostatistical Methodology
The methodological framework is divided into four main phases:

* **Social Growth Index (SGI)**: A composite indicator serving as a proxy for territorial resilience, based on the annual growth rates of GDP, Population, and GDP per capita. Variable redundancy was assessed through correlation analysis to ensure robustness.

![Correlation Matrix](images/Correlation%20Matrix%202022.png)
* **LISA Maps (Local Indicators of Spatial Association)**: Analysis based on the *Local Moran's I* statistic to identify statistically significant spatial clusters (High-High, Low-Low) and map territorial interdependence.
![Moran](images/Local%20Moran%20Cluster%202022.png)
* **Fixed-Rank Kriging (FRK)**: Used to project provincial-level GDP to the municipal level. The model combines systematic effects of covariates, such as population, employment, and fiscal capacity, with structured spatial random effects and fine-scale components.
![FRK Reprojection](images/FRK%20reprojection%20GDP%202022.png)

* **Penalty-Adjusted Copeland Ranking**: A ranking procedure based on pairwise comparisons to classify resilience. A spatial penalty term incorporating the average values of neighboring territories was introduced to ensure temporal stability.

## Key Results
* **Spatial Dependence**: Results reveal strong positive spatial autocorrelation; territorial units are significantly influenced by the socio-economic conditions of their neighbors.
* **Resilience Leaders**: The assessment identifies the most resilient areas within the **Lombardy** region, particularly, Milan emerged as the most resilient areas in the country.
![Copeland](images/Copeland%20Municipalities%202022.png)
*Resilience ranking comparison: Provinces (left) vs. Municipalities (right).*

* **Temporal Dynamics (2019–2022)**: The Copeland assessment highlighted an increase in resilience scores in Northern Italy, contrasting with a decreasing trend in many Southern municipalities.
![Copeland Score Changes](images/Copeland%20Score%20Changes.png)
*Spatial distribution of resilience changes: green indicates growth, red indicates a decrease.

## 📂 Repository Structure
* [`docs/`](docs/): Complete academic documentation.
    * [`GRINS_Executive_Summary.pdf`](docs/GRINS_Executive_Summary.pdf): Detailed analysis of the mathematical framework and data sources.
    * [`Scientific_Poster.pdf`](docs/Scientific_Poster.pdf): Visual presentation of resilience patterns and FRK methodology.
* [`images/`](images/): Visualizations of LISA maps, FRK projections, Copeland Score and correlation matrices.

---

## Authors
* [Alessio Pani](https://www.linkedin.com/in/alessio-pani-8739b93bb) (Team Leader)
* Miguel Gutierrez
* Luca Montalto
* Jumil Reyes
* Rahmat Perdana

**Supervisors**: Dr. Matteo Greco, Dr. Giacomo Milan, Prof. Francesca Ieva.

---
*Developed for the Applied Statistics course @ Politecnico di Milano (A.Y. 2024-2025).*
