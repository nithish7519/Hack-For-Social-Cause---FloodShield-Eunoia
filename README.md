flood-prediction gis machine-learning disaster-management social-good hackathon flask scikit-learn india early-warning-system decision-support climate-resilience

# 🌊 FloodShield: AI + GIS Flood Preparedness for Bharat

> Plan relief *before* the flood arrives. · बाढ़ से पहले तैयारी

Built for the **Bharat "Hack For Social Cause" Hackathon**
(Track: AI, GIS & Emerging Technologies)

## The problem
Every monsoon, rivers flood villages across India. Poorer riverside families
are hit hardest, and shelters are often built exactly where the water arrives
first. Relief is frequently planned too late, or in the wrong place.

## Our solution
FloodShield turns rainfall forecasts into a clear, actionable plan:
who will be flooded, how soon, where to place shelters, what supplies to send,
and what to tell people, in their own language.

## Key features
- **AI flood-risk prediction**: a scikit-learn model gives a flood probability
  for every 250 m cell from rainfall, elevation, river distance and drainage.
- **GIS decision map**: terrain, river, bridges, population and vulnerability
  layers, with risk-weighted evacuation routes (Dijkstra) that avoid flooded land.
- **Shelter optimizer**: places flood-safe shelters to maximise coverage of
  at-risk, vulnerable people within a 30-minute walk. Also supports manual placement.
- **72-hour early warning**: village-level warning lead times and a timed
  action plan; optional live forecast via Open-Meteo.
- **Multilingual alerts**: English, Hindi and Tamil messages, ready to plug
  into SMS / IVR / WhatsApp (sending is simulated in this prototype).
- **Relief-supply estimator**: water, food, medical kits, boats and tarpaulins
  per village, with CSV export and print view.
- **Community reports**: residents and volunteers report SOS, blocked roads and
  rising water; reports raise a village's priority.
- **Clean UI**: English/Hindi toggle and a built-in guided tour.

## Tech stack
| Layer | Technology |
|---|---|
| Frontend | HTML, CSS, vanilla JavaScript (canvas map) |
| Backend | Python, Flask (REST API) |
| AI / ML | scikit-learn (logistic regression), NumPy |
| GIS / routing | SciPy sparse-graph Dijkstra on a risk-weighted grid |
| Database | SQLite (reports, alerts, saved plans) |

## Quick start (Windows)
    run.bat
Then open http://127.0.0.1:5000. See the full steps below or run
`python test_api.py` to smoke-test every endpoint.

## Social impact
Faster, fairer relief for the most vulnerable communities.
Aligned with UN SDG 1, 10, 11 and 13.

## Data note
All data in this prototype (district, villages, population, historical floods)
is **synthetic**, and village names are fictional. The same pipeline can use
SRTM/CartoDEM elevation, IMD/CHIRPS rainfall, Census/WorldPop population and
Sentinel-1 flood extents.

## Roadmap
- Real DEM, rainfall and flood-extent data; gradient-boosting / U-Net models
- Live SMS / IVR / WhatsApp gateway; offline-first PWA for field teams
- District-authority roles, audit log and privacy-preserving household data
