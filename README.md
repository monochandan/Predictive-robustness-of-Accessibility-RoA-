[![Python 3.12.6](https://img.shields.io/badge/Python-3.12.6-e34fc3?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/) 
[![Vite](https://img.shields.io/badge/Vite-Frontend-orange?style=for-the-badge&logo=vite&logoColor=white)](https://vite.dev/) 
[![javascript](https://img.shields.io/badge/JavaScript-ded416?style=for-the-badge&logo=JavaScript&logoColor=white)]([https://vite.dev/](https://developer.mozilla.org/de/docs/Web/JavaScript)) 
[![FastAPI](https://img.shields.io/badge/FastAPI-Backend-24bf2c?style=for-the-badge&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/) 

<!--![Status](https://img.shields.io/badge/status-in--progress-yellow)-->
![License](https://img.shields.io/badge/license-MIT-green)
![scikit-learn](https://img.shields.io/badge/sklearn-ML-orange)
![OSMnx](https://img.shields.io/badge/OSMnx-network--data-lightgrey)
[![RoA](https://img.shields.io/badge/RoA%20-Springer-3636cf?style=for-the-badge&logo=springer&logoColor=white)](https://link.springer.com/chapter/10.1007/978-3-031-56826-8_10)


<!--[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Database-24b2bf?style=for-the-badge&logo=postgresql&logoColor=white)](https://www.postgresql.org/) 
[![Google](https://img.shields.io/badge/Google-gemini-3636cf?style=for-the-badge&logo=google&logoColor=white)](https://ai.google.dev)-->

# Predictive Robustness of Accessibility (RoA)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
<!--![Status](https://img.shields.io/badge/Status-Completed-success)-->
Extends shortest-path-based road network resilience analysis (Trier flood case study) by replacing static, 
binary flood-zone disruption with ML-predicted, weather-driven flood probabilities per road segment. 
Uses OpenStreetMap road network data, official flood hazard scenarios (BfG), and Open-Meteo weather data to
train Random Forest / XGBoost classifiers estimating flood likelihood per edge from rainfall, elevation, 
and river proximity. These probabilities feed into a probabilistic RoA index, enabling forecast-driven 
resilience assessment of emergency logistics access (hospitals, fire stations) rather than only post-hoc 
disruption analysis.

# Idea 1: Flood Impact Route Comparison
![Status](https://img.shields.io/badge/Status-Active%20Development-yellow)

This module lets a user select a source and destination (e.g., a residential area and its nearest hospital or fire station) and view two maps side by side: the shortest route in the intact road network versus the shortest route under 2021 flood conditions, with the corresponding Robustness of Accessibility (RoA) score shown for each. The goal is to make the flood's resilience impact immediately visible and comparable for a given connection, extending the original paper's static analysis into an interactive tool. Work in progress.

# Idea 2: Live Flood Risk Lookup
![Status](https://img.shields.io/badge/Status-Active%20Development-yellow)

This module allows a user to click any point on the map and get a real-time flood risk estimate for the nearest road segment, using a trained ML classifier (Random Forest / XGBoost) combined with live rainfall data pulled from the Open-Meteo API. Static road/terrain features (elevation, distance to river, road type) are combined with recent rainfall (3-day and 7-day cumulative) to predict flood probability on demand, moving the project from historical flood analysis toward forecast-driven risk assessment. Work in progress.
