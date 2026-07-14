# 🏀 NBA Legends

### An interactive NBA hall-of-fame player browser built with React

[![Live Demo](https://img.shields.io/badge/🚀_Live_Demo-nba--legends26.netlify.app-C9082A?style=for-the-badge)](https://nba-legends26.netlify.app/)
[![React](https://img.shields.io/badge/React-19-61DAFB?style=for-the-badge&logo=react&logoColor=black)](https://react.dev/)
[![Bootstrap](https://img.shields.io/badge/Bootstrap-5-7952B3?style=for-the-badge&logo=bootstrap&logoColor=white)](https://getbootstrap.com/)
[![React Bootstrap](https://img.shields.io/badge/React_Bootstrap-2-7952B3?style=for-the-badge&logo=bootstrap&logoColor=white)](https://react-bootstrap.github.io/)
[![Create React App](https://img.shields.io/badge/Create_React_App-5-09D3AC?style=for-the-badge&logo=react&logoColor=white)](https://create-react-app.dev/)
[![Netlify](https://img.shields.io/badge/Netlify-Deployed-00C7B7?style=for-the-badge&logo=netlify&logoColor=white)](https://www.netlify.com/)

---

## ✨ Overview

**NBA Legends** is a responsive single-page React application that showcases 12 of the greatest players in NBA history as interactive flip cards. Each card displays the player's photo and name on the front; clicking reveals career statistics — points, rebounds, assists, and All-Star selections — on the back.

This project was built during my early React learning phase to practice component structure, props, `useState`, `.map()` rendering, conditional JSX, Bootstrap grid layouts, and parent-to-child data flow.

---

## 🖥️ Live Demo

> 🔗 **[https://nba-legends26.netlify.app/](https://nba-legends26.netlify.app/)**

---

## 🚀 Features

| Feature | Description |
|---|---|
| 🏀 **12 Legend Cards** | Kareem, Jordan, Kobe, Magic, Bird, and more with photos and stats |
| 🔄 **Flip Interaction** | Click a card to toggle between player photo and career statistics |
| 🔍 **Live Search** | Filter players by name with case-insensitive search |
| 📊 **Stat Icons** | Points, rebounds, assists, and All-Star counts with React Icons |
| 📐 **Responsive Grid** | 4 → 2 → 1 column layout across Bootstrap breakpoints |
| 🧩 **Reusable Components** | Header, Main, and CardContainer split into modules |
| 📦 **Data-Driven UI** | Player data stored in `data.js` and rendered with `.map()` |
| 🎨 **NBA Theme** | Full-page basketball court background with branded header |

---

## 🛠️ Tech Stack

| Technology | Role |
|---|---|
| **[React 19](https://react.dev/)** | Component-based UI with `useState` hooks |
| **[Bootstrap 5](https://getbootstrap.com/)** | Utility classes and responsive grid system |
| **[React Bootstrap](https://react-bootstrap.github.io/)** | Card, Form, Container, Row, Col components |
| **[React Icons](https://react-icons.github.io/react-icons/)** | Basketball-themed stat icons |
| **[Create React App](https://create-react-app.dev/)** | Project scaffolding and build tooling |
| **[Netlify](https://www.netlify.com/)** | Static deployment |

---

## 📁 Project Structure

```
src/
├── App.jsx
├── App.css
├── index.js
│
├── assets/
│   └── nba-legends26.gif       # App preview GIF
│
├── components/
│   ├── Header/
│   │   └── Header.jsx          # Logo, title, search input
│   ├── Main/
│   │   ├── Main.jsx            # Filtered player grid
│   │   └── main.css
│   └── CardContainer/
│       └── CardContainer.jsx   # Flip card with stats
│
└── helpers/
    ├── data.js                 # 12 NBA legend player objects
    ├── nba-bg.jpg              # Full-page background image
    └── nba-logo.png            # Header logo
```

---

## 🏗️ Data Flow

```
App (search state)
 ├── Header  ← inputValue, setInputValue (controlled search input)
 └── Main    ← value (search query)
      └── CardContainer × 12  ← name, img, statistics (via props + spread)
           └── useState (flip toggle per card)
```

**Search** — `App` holds the search string in `useState`. `Header` updates it on every keystroke; `Main` filters `data.js` and re-renders matching cards.

**Flip** — Each `CardContainer` manages its own `flipped` state. Clicking toggles between the photo view and the statistics list.

---

## 📱 Responsive Design

| Breakpoint | Layout |
|---|---|
| **≥ 992px (lg)** | 4-column card grid |
| **768px – 991px (md)** | 2-column card grid |
| **< 768px (xs / sm)** | Single-column card grid |

---

## ⚙️ Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) ≥ 18

### Installation

```bash
git clone https://github.com/cankurtduygu/NBA-legends.git
cd NBA-legends
npm install
npm start
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

### Production Build

```bash
npm run build
```

---

## 🌐 Deployment

The app is deployed on **Netlify** as a static Create React App build.

To deploy your own instance, connect the repo to Netlify and set:

- **Build command:** `npm run build`
- **Publish directory:** `build`

---

## 🚀 Future Improvements

- [ ] Empty state message when search returns no results
- [ ] Mobile-friendly search input width
- [ ] Keyboard accessibility for card flip
- [ ] Image lazy loading for player photos
- [ ] Player detail modal or dedicated page
- [ ] Sort / filter by stat category

---

## 🤝 Contributing

1. Fork the repository
2. `git checkout -b feat/your-feature`
3. `git commit -m "feat: your change"`
4. `git push origin feat/your-feature`
5. Open a Pull Request

---

Built with React · Bootstrap · Create React App

⭐ **Star this repo if you find it useful!**
