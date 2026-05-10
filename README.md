# Fixed Rank Kriging (FRK) - Estimation of Italian municipal GDP

> **Spatial Statistics and Geostatistical Modeling for the [GRINS Project](https://grins.it/)**  

## Project Overview
Questo progetto, sviluppato nell'ambito del progetto **GRINS**, mira a valutare la resilienza socio-economica degli oltre 7.900 comuni italiani. Poiché i dati ufficiali sul PIL non sono disponibili a livello municipale, il lavoro implementa un framework di **downscaling geostatistico** per produrre stime granulate e analizzare la capacità dei territori di assorbire shock e sostenere lo sviluppo.

## Geostatistical Methodology
Il framework metodologico si articola in quattro fasi principali:

* **Social Growth Index (SGI)**: Un indicatore composito che funge da proxy per la resilienza, basato sui tassi di crescita annuali di PIL, Popolazione e PIL pro capite.
* **Fixed-Rank Kriging (FRK)**: Utilizzato per proiettare il PIL provinciale a livello comunale. Il modello combina effetti sistematici di covariate (occupazione, capacità fiscale) con effetti casuali spaziali strutturati e componenti a scala fine.
* **LISA Maps (Local Indicators of Spatial Association)**: Analisi basata sulla statistica *Local Moran's I* per identificare cluster spaziali significativi (High-High, Low-Low) e mappare la dipendenza territoriale.
* **Penalty-Adjusted Copeland Ranking**: Un metodo di ordinamento basato su confronti a coppie per classificare la resilienza. È stato introdotto un termine di penalità basato sulla media dei vicini per garantire stabilità temporale ai risultati.

## Key Results
* **Dipendenza Spaziale**: I risultati rivelano una forte autocorrelazione spaziale positiva; i territori tendono a influenzare ed essere influenzati dalle condizioni socio-economiche delle aree limitrofe.
* **Leader della Resilienza**: Le province della **Lombardia** (con Milano in testa) sono emerse come le unità territoriali più resilienti del paese.
* **Dinamiche Temporali (2019-2022)**: L'analisi del punteggio Copeland ha evidenziato un incremento della resilienza nel Nord Italia, contrapposto a una tendenza alla diminuzione in molti comuni del Mezzogiorno.

## Repository Structure
* [`docs/`](docs/): Documentazione accademica completa.
    * [`GRINS_Executive_Summary.pdf`](docs/GRINS_Executive_Summary.pdf): Analisi dettagliata del framework matematico e dei dati.
    * [`Scientific_Poster.pdf`](docs/Scientific_Poster.pdf): Presentazione visuale dei pattern di resilienza e della metodologia FRK.
* [`images/`](images/): Visualizzazioni delle mappe LISA e delle matrici di correlazione.

---

## Authors
* [Alessio Pani](https://www.linkedin.com/in/alessio-pani-8739b93bb) (Team Leader)
* Miguel Gutierrez
* Luca Montalto
* Jumil Reyes
* Rahmat Perdana

**Supervisors**: Dr. Matteo Greco, Dr. Giacomo Milan, Prof. Francesca Ieva.
---
*Developed for the Applied Statistics course @ Politecnico di Milano (A.A. 2024/2025).*
