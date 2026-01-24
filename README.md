# VibePick_front: Frontend for Twitch Recommendation System

## Overview
VibePick_front is the frontend part for **VibePick**, a content discovery and recommendation platform for live streams, videos, and clips.  
The frontend is built with **React (Create React App)** and **Ant Design**, and communicates with the backend through REST APIs using cookie-based session authentication.

---

## Key Features

- **User Authentication**
  - Supports user login via a modal interface
  - Maintains authentication state using cookie-based sessions

- **Content Browsing**
  - Displays live streams, videos, and clips with tab-based navigation
  - Fetches and renders content dynamically from the backend

- **Personalized Recommendations**
  - Shows recommended content based on user preferences
  - Updates recommendations after user interactions

- **Favorites Management**
  - Allows users to favorite or unfavorite content items
  - Synchronizes favorite state with the backend

- **Search Functionality**
  - Enables custom content search by game or category
  - Triggers backend queries and updates displayed results

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
│   └── assets/                        # Static assets (images, icons, etc.)
│
├── src/
│   ├── components/                    # Reusable React components
│   │   ├── Home.js                    # Main content area (Streams / Videos / Clips tabs)
│   │   ├── Login.js                   # Login modal and authentication form
│   │   ├── PageHeader.js              # Application header (login status, user actions)
│   │   └── CustomSearch.js            # Custom search component (e.g. by game/category)
│   │
│   ├── utils.js                       # Centralized API layer (fetch wrappers for backend)
│   ├── App.js                         # Main React component, global state & layout logic
│   ├── index.js                       # Entry point rendering <App /> to the DOM
│   ├── index.css                      # Global CSS styling and Ant Design imports
│   ├── App.css                        # App-level styles
│   ├── App.test.js                    # Default Create React App test file
│   ├── setupTests.js                  # Test configuration for CRA
│   ├── reportWebVitals.js             # Performance metrics configuration
│   └── logo.svg                       # Default CRA asset
│
└── package.json                       # Project metadata, dependencies, and scripts

```

---


## Running the Project Locally

```bash
npm install
npm start
```

## Docker Deployment
Build and run the application with Docker Compose:

```bash
docker-compose up --build
```
Then open http://localhost:3000 in your browser.

