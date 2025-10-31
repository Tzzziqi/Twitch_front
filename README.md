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

| Layer              | Technology |
|--------------------|-------------|
| Frontend           | React (Create React App), JavaScript, CSS3 |
| Backend            | Spring Boot (Java), Maven |
| Communication      | RESTful API (JSON) |
| Deployment         | Docker Compose |
| Version Control    | Git + GitHub |


---

## Project Structure
```
TwitchF/
│
├── public/
│   ├── index.html                     # Root HTML template loaded by React
│   └── assets/                        # Static assets such as images or icons
│
├── src/
│   ├── components/                    # Reusable React components (UI elements)
│   ├── utils.js                       # Utility functions shared across components
│   ├── App.js                         # Main React component, application entry logic
│   ├── index.js                       # Entry point rendering <App /> to the DOM
│   ├── index.css                      # Global CSS styling
│   └── reportWebVitals.js             # Performance metrics configuration
│
└── package.json                       # Project metadata, dependencies, and scripts

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

