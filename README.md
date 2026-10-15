# 🌊 Quantum Coders — Flood Risk Prediction & Alert System

An AI-inspired flood monitoring and risk prediction platform designed to help users understand potential flood threats through weather data, risk indicators, interactive maps, and alerts.

## 🚀 Overview

The Flood Risk Prediction and Alert System combines weather information and water-level estimates to identify potential flood risks. It provides a dashboard for viewing risk levels, exploring geographic areas, and monitoring high-risk locations.

## ✨ Features

- 🌧️ **Flood Risk Prediction** — Estimates flood risk using rainfall and water-level indicators.
- 🗺️ **Interactive Maps** — Displays geographic risk information using Google Maps.
- 🚨 **Risk Alerts** — Records high-risk predictions for monitoring.
- 📊 **Risk Dashboard** — Visualizes low, medium, and high-risk levels.
- 🔮 **Future Risk Estimates** — Shows projected risk at different time intervals.
- 🗄️ **Database Persistence** — Stores predictions and alerts using SQLite or MySQL.
- 🧪 **Simulation Mode** — Tests risk scenarios using custom rainfall and water-level inputs.
- 🐳 **Docker Support** — Includes Docker Compose configuration for containerized development.

## 🛠️ Tech Stack

| Component | Technology |
|---|---|
| Frontend | React, Tailwind CSS, Vite |
| Backend | Python, FastAPI |
| Maps | Google Maps API |
| Weather Data | OpenWeather API |
| Database | SQLite / MySQL |
| API Communication | REST API |
| Containerization | Docker, Docker Compose |

## 📁 Project Structure

```text
Quantum-coders/
└── disaster managment AI/
    ├── backend/
    ├── frontend/
    ├── .env.example
    ├── .gitignore
    ├── docker-compose.yml
    └── README.md
```

## ⚙️ Getting Started

### Prerequisites

- Python 3.10 or later
- Node.js and npm
- OpenWeather API key
- Google Maps API key

### 1. Clone the repository

```bash
git clone https://github.com/Suhas810/Quantum-coders.git
cd Quantum-coders/disaster\ managment\ AI
```

### 2. Configure environment variables

Create a `.env` file in the project directory using `.env.example` as a reference.

```env
OPENWEATHER_API_KEY=your_openweather_api_key
GOOGLE_MAPS_API_KEY=your_google_maps_api_key
DATABASE_URL=sqlite:///backend/alerts.db
```

Never commit real API keys or other secrets to GitHub.

### 3. Start the backend

```bash
cd backend
python -m pip install -r requirements.txt
uvicorn app.main:app --reload --port 8000
```

### 4. Start the frontend

Open a second terminal:

```bash
cd "disaster managment AI/frontend"
npm install
```

Create a `.env` file inside the frontend directory:

```env
VITE_API_BASE_URL=http://localhost:8000
```

Start the development server:

```bash
npm run dev
```

Open the local URL displayed by Vite, usually `http://localhost:5173`.

## 🔌 API Endpoints

| Method | Endpoint | Purpose |
|---|---|---|
| GET | `/predict?lat={lat}&lon={lon}` | Predict risk for a location |
| GET | `/predict/multi` | Retrieve predictions for multiple locations |
| POST | `/simulate` | Simulate a flood-risk scenario |

The backend API documentation is typically available at `http://localhost:8000/docs` when FastAPI is running.

## 🧠 How It Works

1. Retrieve weather information for a selected location.
2. Estimate rainfall and water-level conditions.
3. Evaluate risk indicators using the prediction logic.
4. Display risk levels and future estimates on the dashboard.
5. Store predictions and generate alerts for high-risk locations.

**Note:** The current prediction logic is rule-based, not a trained machine-learning model. Results are estimates for demonstration purposes and should not be used as a substitute for official weather warnings or emergency instructions.

## 🔮 Future Improvements

- Integrate trained machine-learning models using historical flood data.
- Incorporate real-time river and water-level sensor data.
- Improve prediction accuracy with historical weather trends.
- Add user authentication and location-based notifications.
- Deploy the application to a cloud platform.
- Add automated testing and continuous integration.

## 👥 Team

**Quantum Coders**

Developed as a software project focused on applying web technologies and predictive analytics to disaster preparedness.

## 🤝 Contributing

Contributions and suggestions are welcome. Fork the repository, create a feature branch, make your changes, and submit a pull request.

## 📄 License

A license has not yet been specified. Add a `LICENSE` file before distributing the project under an open-source license.

---

⭐ If you find this project interesting, consider starring the repository!
