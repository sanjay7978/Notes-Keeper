# 📝 Keeper — Your Personal Notes App

<div align="center">

![React](https://img.shields.io/badge/React-17.0.2-61DAFB?style=for-the-badge&logo=react&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-5.x-646CFF?style=for-the-badge&logo=vite&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![CSS3](https://img.shields.io/badge/CSS3-Styled-1572B6?style=for-the-badge&logo=css3&logoColor=white)

*A clean, minimal note-taking app inspired by Google Keep — built with React.*

</div>

---

## ✨ Features

- 🖊️ **Create notes** with a title and content in seconds
- 🗑️ **Delete notes** you no longer need
- ⚡ **Instant updates** — no page reloads, powered by React state
- 📱 **Clean card layout** that keeps things organized
- 🎨 **Minimal, distraction-free UI** with a warm golden theme

---

## 🚀 Getting Started

### Prerequisites

Make sure you have **Node.js** installed on your machine.

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/your-username/keeper-app.git

# 2. Navigate into the project folder
cd keeper-app

# 3. Install dependencies
npm install

# 4. Start the development server
npm run dev
```

Then open your browser and visit `http://localhost:5173` 🎉

---

## 🗂️ Project Structure

```
keeper/
├── public/
│   └── styles.css          # Global styles
├── src/
│   ├── components/
│   │   ├── App.jsx         # Root component — manages notes state
│   │   ├── Header.jsx      # Top navigation bar
│   │   ├── Footer.jsx      # Footer with dynamic year
│   │   ├── Note.jsx        # Individual note card
│   │   └── CreateArea.jsx  # Form to add new notes
│   └── index.jsx           # App entry point
├── index.html
├── vite.config.js
└── package.json
```

---

## 🧠 How It Works

The app follows a simple **unidirectional data flow**:

```
CreateArea  ──(addNote)──▶  App (state)  ──(props)──▶  Note cards
                                │
                          (deleteNote)
                                │
                           filters out
                           by index
```

- `App.jsx` holds the `notes` array in state using `useState`
- `CreateArea` lifts the new note up via an `onAdd` callback
- Each `Note` card receives an `onDelete` callback to remove itself by index

---

## 🛠️ Built With

| Tool | Purpose |
|------|---------|
| [React 17](https://reactjs.org/) | UI component library |
| [Vite](https://vitejs.dev/) | Lightning-fast build tool |
| [Google Fonts](https://fonts.google.com/) | McLaren & Montserrat typefaces |
| CSS3 | Styling and layout |

---

## 📸 Preview

```
┌─────────────────────────────────┐
│  🟡  Keeper                     │  ← Header
├─────────────────────────────────┤
│  ┌───────────────────────────┐  │
│  │  Title                    │  │  ← Create Area
│  │  Take a note...           │  │
│  │                       [+] │  │
│  └───────────────────────────┘  │
│                                 │
│  ┌──────┐  ┌──────┐  ┌──────┐  │
│  │ Note │  │ Note │  │ Note │  │  ← Note Cards
│  │      │  │      │  │      │  │
│  │ DEL  │  │ DEL  │  │ DEL  │  │
│  └──────┘  └──────┘  └──────┘  │
└─────────────────────────────────┘
```

---

## 📜 Available Scripts

| Command | Description |
|---------|-------------|
| `npm run dev` | Start development server |
| `npm run build` | Build for production |
| `npm run preview` | Preview production build |
| `npm run lint` | Run ESLint checks |

---

## 🤝 Contributing

Contributions are welcome! Feel free to open an issue or submit a pull request.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

<div align="center">

</div>
