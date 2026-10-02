# Project dashboard

An interactive, code-free HTML presentation of the project: the goal, the methods, the findings and the notebook figures.

| Page | Contents |
|---|---|
| `index.html` | Goal, dataset overview, pipeline, headline findings, team |
| `statistics.html` | Descriptive questions Q1–Q9 with interactive charts (category split, seasonality, CPI / real-price calculator, correlation heatmap, amenities) |
| `hypothesis.html` | Hypothesis tests H1–H4, Simpson's-paradox simulator, p-value vs sample-size explorer, Bonferroni calculator |
| `clustering.html` | Feature-set comparison, k = 4 / 7 / 10 profiles, DBSCAN parameter explorer, recommender demo |
| `prediction.html` | Rent and sale XGBoost models: model ladder, training curve, split explorer, error-band calculator |
| `maps.html` | The folium maps from `presentation/geo/` and the listing heatmap from `q4-5/map.html` |

## Viewing

Open `dashboard/index.html` in a browser. The charts work offline because Chart.js is vendored in `assets/vendor/`. The embedded maps load Leaflet tiles from the internet.

To serve it locally (the maps load best this way), run this from the repository root:

```bash
python -m http.server 8000
# then open http://localhost:8000/dashboard/
```

All numbers come from the saved outputs of the notebooks in `presentation/`. The figures in `assets/img/` were extracted from those notebooks.
