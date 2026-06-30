# 🌤 Weather Glass Dashboard
### Final Year Project — Full Stack Weather Application

A production-ready, fully responsive weather dashboard built with **Node.js**, **Express**, **HTML5**, **CSS3**, and **JavaScript**.

---

## 📸 Features

| Feature | Details |
|---|---|
| 🌡️ **Live Weather** | Real-time temperature, humidity, wind, pressure, visibility |
| ⏱️ **24-Hour Forecast** | Scrollable hourly cards with rain probability |
| 📅 **7-Day Forecast** | Daily high/low with temperature range bars |
| 🌿 **Air Quality** | AQI index + PM2.5, PM10, NO₂, O₃, SO₂, CO |
| 📊 **Analytics** | Interactive charts — temperature, humidity, wind, rain trends |
| 🗺️ **Live Map** | 5 weather layers: temperature, precipitation, clouds, wind, pressure |
| ⭐ **Favorites** | Save & manage cities, persisted in localStorage |
| 🔔 **Alerts** | Auto-detects extreme weather and sends notifications |
| ☀️ **Sunrise/Sunset** | Animated sun arc with real-time daylight progress |
| 📍 **Geolocation** | Auto-detects your location on load |
| 🌐 **Aurora UI** | Animated glassmorphism design with aurora background |

---

## 🛠 Tech Stack

| Layer | Technology |
|---|---|
| **Backend** | Node.js + Express |
| **Frontend** | Vanilla HTML5, CSS3, JavaScript (ES2022) |
| **Charts** | Chart.js 4 |
| **Weather API** | OpenWeatherMap (free tier) |
| **Caching** | node-cache (10-minute server-side cache) |
| **Fonts** | Google Fonts (Inter + Space Grotesk) |

---

## 🚀 Getting Started

### 1. Install Dependencies

```bash
cd weather-glass-dashboard
npm install
```

### 2. Configure API Key

Edit `.env` and add your OpenWeatherMap API key:

```
PORT=3000
OWM_API_KEY=your_api_key_here
```

Get a free key at: https://openweathermap.org/api

### 3. Run the App

```bash
# Production
npm start

# Development (with auto-restart)
npm run dev
```

### 4. Open in Browser

```
http://localhost:3000
```

---

## 📁 Project Structure

```
weather-glass-dashboard/
├── server/
│   └── index.js          ← Express server + API proxy + caching
├── public/
│   ├── index.html        ← Main SPA shell
│   ├── css/
│   │   └── main.css      ← Full glassmorphism styles
│   └── js/
│       └── main.js       ← All frontend logic
├── .env                  ← API key config (never commit this)
├── package.json
└── README.md
```

---

## 🔌 API Endpoints

| Endpoint | Description |
|---|---|
| `GET /api/weather?city=London` | Current weather by city |
| `GET /api/weather/coords?lat=&lon=` | Current weather by GPS |
| `GET /api/forecast?lat=&lon=` | 5-day / 3-hour forecast |
| `GET /api/airquality?lat=&lon=` | Air quality index + pollutants |
| `GET /api/history?lat=&lon=` | Historical/trend data for charts |
| `GET /api/health` | Server health check |

---

## 📦 Dependencies

```json
"express"     : "^4.18.2"   — HTTP server
"axios"       : "^1.6.0"    — HTTP client for OWM API
"dotenv"      : "^16.3.1"   — Environment variables
"cors"        : "^2.8.5"    — Cross-origin headers
"node-cache"  : "^5.1.2"    — In-memory response caching
"nodemon"     : "^3.0.1"    — Dev auto-restart (devDependency)
```

---

## 📜 License

MIT — Free to use, modify and distribute.

---

*Final Year Project · Built with ❤️ using Node.js + Express + OpenWeatherMap*
