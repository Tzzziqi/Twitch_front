# TwitchF: Frontend for Twitch Recommendation System

## Overview
TwitchF is the frontend part of a full-stack streaming recommendation system that provides personalized Twitch resource suggestions.  
This component is responsible for the user interface, interaction design, and data visualization, communicating with the backend recommendation API to deliver customized video and stream recommendations.

---

## Features
- User-friendly interface for exploring Twitch streams and clips  
- Real-time data retrieval from backend API  
- Responsive layout optimized for desktop and mobile  
- Modular React component structure for scalability  
- Easy integration with Docker for deployment  

---

## Tech Stack
| Layer | Technology |
|-------|-------------|
| Frontend | React (Create React App), JavaScript, CSS3 |
| Backend Connection | RESTful API (Node.js / Express or FastAPI) |
| Deployment | Docker Compose |
| Version Control | Git + GitHub |

---

## Project Structure
```
TwitchF/
├── public/
│ ├── index.html
│ └── assets/
├── src/
│ ├── components/
│ ├── utils.js
│ ├── App.js
│ ├── index.js
│ ├── index.css
│ └── reportWebVitals.js
└── package.json
```

---

## Setup and Run Locally

### 1. Clone the repository
```bash
git clone https://github.com/Tzzziqi/TwitchF.git
cd TwitchF
```
### 2. Install dependencies
```bash
npm install
```

### 3. Start the development server
```bash
npm start
```

## Docker Deployment
Build and run the application with Docker Compose:

```bash
docker-compose up --build
```
Then open http://localhost:3000 in your browser.

## Future Improvements
- Connect with production-level recommendation backend
- Add login and user preference management
- Integrate CDN optimization for static assets
- Improve accessibility and UI/UX responsiveness
