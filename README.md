Each model uses historical and sensor data:
- `RandomForestClassifier` for cyclone formation
- Pollution risk level classified by chemical indicators (pH, COD, BOD, etc.)
- Erosion prediction based on wind, wave, and coastal structure data

---

## 🗺️ Leaflet Integration

- Receives JSON API data every 10s
- Icons/Markers change color dynamically
- Flash animation on high-risk zones
- Popups show: **Threat Type**, **Timestamp**, **Intensity**, **Region**, **Action**

---

## ⚙️ Setup Instructions

1. **Clone Repo**
   ```bash
   git clone https://github.com/your-username/Coastal-Threat-Alert-System.git
   cd Coastal-Threat-Alert-System

2. Start Backend (FastAPI for each model)
   uvicorn CYCLONE_MODEL.cyclone_app:app --port 8001 --reload
uvicorn POLLUTION_MODEL.pollution_app:app --port 8002 --reload
uvicorn COASTALEROSION_MODEL.coastalErosion_app:app --port 8003 --reload
uvicorn STORM_MODEL.storm_app:app --port 8004 --reload

3.Start Frontend
cd FRONTEND
npm install
npm run dev

📈 Future Enhancements

Integration with IoT sensor hardware

SMS/email alert system

User dashboard with login & threat history

AI-based illegal activity detection from satellite images


