# Predictive Robustness of Accessibility (RoA)

Extends shortest-path-based road network resilience analysis (Trier flood case study) by replacing static, 
binary flood-zone disruption with ML-predicted, weather-driven flood probabilities per road segment. 
Uses OpenStreetMap road network data, official flood hazard scenarios (BfG), and Open-Meteo weather data to
train Random Forest / XGBoost classifiers estimating flood likelihood per edge from rainfall, elevation, 
and river proximity. These probabilities feed into a probabilistic RoA index, enabling forecast-driven 
resilience assessment of emergency logistics access (hospitals, fire stations) rather than only post-hoc 
disruption analysis.

# Idea 1: Flood Impact Route Comparison

This module lets a user select a source and destination (e.g., a residential area and its nearest hospital or fire station) and view two maps side by side: the shortest route in the intact road network versus the shortest route under 2021 flood conditions, with the corresponding Robustness of Accessibility (RoA) score shown for each. The goal is to make the flood's resilience impact immediately visible and comparable for a given connection, extending the original paper's static analysis into an interactive tool. Work in progress.

# Idea 2: Live Flood Risk Lookup

This module allows a user to click any point on the map and get a real-time flood risk estimate for the nearest road segment, using a trained ML classifier (Random Forest / XGBoost) combined with live rainfall data pulled from the Open-Meteo API. Static road/terrain features (elevation, distance to river, road type) are combined with recent rainfall (3-day and 7-day cumulative) to predict flood probability on demand, moving the project from historical flood analysis toward forecast-driven risk assessment. Work in progress.
