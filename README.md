# VibePick_front: Frontend for Twitch Recommendation System

## Overview
VibePick_front is the frontend part for **VibePick**, a content discovery and recommendation platform for live streams, videos, and clips.  
The frontend is built with **React (Create React App)** and **Ant Design**, and communicates with the backend through REST APIs using cookie-based session authentication.

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

## Application Architecture

### `App.js`
- Serves as the root component of the application
- Manages global state, including:
  - User login status
  - Favorite items
  - Top game list
  - Currently displayed resources
- Defines the main layout using Ant Design `Layout`, including:
  - Header
  - Sidebar (game list and recommendations)
  - Main content area

---

### `Home.js`
- Renders the main content area
- Displays **Streams**, **Videos**, and **Clips** using tab-based navigation
- Receives resource data and favorite state from `App.js`
- Propagates user interactions (e.g. favorite/unfavorite) back to the parent

---

### `Login.js`
- Implements user login functionality
- Uses Ant Design form components
- On successful login, updates global authentication state in `App.js`

---

### `PageHeader.js`
- Displays the application header
- Shows login status and user-related actions
- Triggers login modal when user is not authenticated

---

### `CustomSearch.js`
- Provides custom search functionality
- Allows users to search content based on selected criteria
- Communicates search intent back to `App.js`

---

## API Layer (`src/utils.js`)

All backend communication is centralized in `utils.js`.

Key characteristics:
- Uses the **Fetch API**
- Sends requests with `credentials: 'include'` to maintain session-based authentication
- Encapsulates all REST API calls to keep components clean and focused

Typical responsibilities include:
- User login and logout
- Fetching top games
- Searching content by game or category
- Fetching recommendations
- Managing user favorites

---

## Styling

- Global styles are defined in `index.css`
- Ant Design styles are imported globally
- Layout-specific styles (sidebar scrolling, content background, spacing) are customized via CSS

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

