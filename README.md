# Predictive Robustness of Accessibility (RoA)

Extends shortest-path-based road network resilience analysis (Trier flood case study) by replacing static, 
binary flood-zone disruption with ML-predicted, weather-driven flood probabilities per road segment. 
Uses OpenStreetMap road network data, official flood hazard scenarios (BfG), and Open-Meteo weather data to
train Random Forest / XGBoost classifiers estimating flood likelihood per edge from rainfall, elevation, 
and river proximity. These probabilities feed into a probabilistic RoA index, enabling forecast-driven 
resilience assessment of emergency logistics access (hospitals, fire stations) rather than only post-hoc 
disruption analysis.
