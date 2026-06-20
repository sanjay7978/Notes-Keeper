# 🗺️ Keeper — Future Plans & Roadmap

> A living document of ideas to evolve Keeper from a simple React app into a full-stack, AI-powered productivity platform.

---

## 📊 Current State

```
Frontend only  →  React + Vite  →  Notes live in memory (lost on refresh)
```

---

## 🏗️ Phase 1 — Make It a Real App (Full Stack Foundation)

### 🔧 Backend Setup
- [ ] Set up a **Node.js + Express** REST API server
- [ ] Connect a **MongoDB** database (or PostgreSQL if you prefer SQL)
- [ ] Use **Mongoose** (for MongoDB) to define a Note schema with fields:
  - `title`, `content`, `createdAt`, `updatedAt`, `color`, `isPinned`, `tags`
- [ ] Build CRUD API endpoints:
  - `GET /notes` — fetch all notes
  - `POST /notes` — create a note
  - `PUT /notes/:id` — update a note
  - `DELETE /notes/:id` — delete a note

### 🔐 Authentication & User Accounts
- [ ] Add **JWT-based authentication** (JSON Web Tokens)
- [ ] Build Sign Up / Login pages in React
- [ ] Use **bcrypt** to hash passwords before storing them
- [ ] Each note belongs to a specific user (private notes)
- [ ] Add **Google OAuth** login with Passport.js ("Sign in with Google")
- [ ] Add a "Remember me" checkbox with refresh tokens

### 💾 Data Persistence
- [ ] Replace React `useState` with **API calls** using `fetch` or `axios`
- [ ] Notes now survive page refresh — stored in the database
- [ ] Add **loading spinners** and **error messages** for network requests
- [ ] Use **React Query** or **SWR** for smart data fetching and caching

---

## 🎨 Phase 2 — Richer Note Features

### ✏️ Note Enhancements
- [ ] **Rich text editor** — bold, italic, bullet lists, headings (use `react-quill` or `TipTap`)
- [ ] **Color-coded notes** — pick a background color for each note card
- [ ] **Pin important notes** to the top of the board
- [ ] **Archive notes** instead of permanently deleting them
- [ ] **Trash / Recycle bin** — recover accidentally deleted notes within 30 days
- [ ] **Character / word count** shown while typing
- [ ] **Note timestamps** — "Created 2 hours ago", "Edited just now"

### 🏷️ Organization
- [ ] **Labels / Tags** — add multiple tags to notes and filter by them
- [ ] **Search bar** — real-time search across all note titles and content
- [ ] **Sort options** — by date created, date edited, alphabetical, color
- [ ] **Grid vs List view** toggle for the notes board
- [ ] **Drag and drop** to reorder notes (use `react-beautiful-dnd`)
- [ ] **Folders / Notebooks** — group related notes into collections

### 📎 Media Attachments
- [ ] **Image upload** — attach photos to a note (store in AWS S3 or Cloudinary)
- [ ] **File attachments** — PDFs, documents linked to a note
- [ ] **Voice memos** — record audio and attach it to a note
- [ ] **Drawing / Sketch pad** — draw diagrams or doodles on a canvas

---

## 🤖 Phase 3 — AI-Powered Features

> This is where Keeper becomes truly powerful.

### 📝 Smart Writing Assistant
- [ ] **AI auto-complete** — press Tab to let AI finish your sentence
- [ ] **Rewrite / rephrase** — select text and ask AI to make it clearer, shorter, or more formal
- [ ] **Grammar & spelling checker** powered by AI (better than basic spellcheck)
- [ ] **Tone detector** — tells you if your note sounds formal, casual, aggressive, etc.

### 🧠 Note Intelligence
- [ ] **Auto-summarize** — generate a 2-3 line summary of any long note with one click
- [ ] **Extract action items** — AI reads your note and lists out the tasks mentioned
- [ ] **Auto-tagging** — AI suggests relevant labels based on the note content
- [ ] **Smart title generator** — AI suggests a title if you leave it blank
- [ ] **Keyword extraction** — highlights the most important words in a note

### 💬 Chat with Your Notes
- [ ] **Ask questions about your notes** — "What did I write about my project last week?"
- [ ] **Semantic search** — search by meaning, not just exact words ("find my fitness goals" returns health-related notes)
- [ ] Use **vector embeddings** (OpenAI or local models) to power this feature

### 🌍 Language Features
- [ ] **Translate notes** to any language with one click
- [ ] **Multilingual support** — write notes in any language, search works across all
- [ ] **Vocabulary suggestions** — AI suggests better words while you write

### 📅 AI + Productivity
- [ ] **Meeting notes mode** — AI structures your raw meeting notes into agenda, decisions, and action items
- [ ] **Daily journaling prompts** — AI suggests a writing prompt every morning
- [ ] **Mood tracking** — AI detects the sentiment of your journal entries over time and shows a mood graph

---

## 🔔 Phase 4 — Collaboration & Sharing

- [ ] **Share a note** via a public link (view-only or editable)
- [ ] **Invite collaborators** to a notebook — real-time editing with **WebSockets** (Socket.io)
- [ ] **Comments** on shared notes
- [ ] **Version history** — see every change made to a note and restore any version
- [ ] **Multiplayer cursors** — see where collaborators are typing (like Google Docs)
- [ ] **Export notes** as PDF, Markdown, or plain text

---

## 📱 Phase 5 — Cross-Platform

- [ ] **Progressive Web App (PWA)** — installable on phone/desktop, works offline
- [ ] **Offline mode** — sync notes when internet reconnects using **IndexedDB**
- [ ] **Mobile app** with React Native (share most of the codebase)
- [ ] **Browser extension** — clip any webpage content directly into a note
- [ ] **Desktop app** with Electron
- [ ] **Keyboard shortcuts** for power users (Ctrl+N for new note, etc.)

---

## 📈 Phase 6 — Analytics & Insights Dashboard

- [ ] **Writing streak** — track how many days in a row you've written a note
- [ ] **Notes per day/week** graph
- [ ] **Most used tags** visualization
- [ ] **Word count over time** — see how much you've written
- [ ] **Mood / sentiment graph** over weeks (from journal entries)
- [ ] **"This day last year"** — resurface old notes from the same date

---

## 🔗 Phase 7 — Integrations

| Integration | What it does |
|-------------|--------------|
| **Google Calendar** | Create a note linked to a calendar event |
| **Slack / Discord** | Send a note as a message to a channel |
| **Gmail** | Save an email as a note automatically |
| **GitHub** | Link code snippets or issues to a note |
| **Notion import** | Import your existing Notion pages |
| **Zapier / Make** | Connect Keeper to 1000+ other apps |
| **WhatsApp** | Send a message to a bot number to save a note |

---

## 🛡️ Phase 8 — Security & Privacy

- [ ] **End-to-end encryption** — notes encrypted on your device before being sent to the server (zero-knowledge)
- [ ] **Password-protect individual notes**
- [ ] **Two-factor authentication (2FA)** — OTP via email or authenticator app
- [ ] **Rate limiting** on the API to prevent abuse
- [ ] **GDPR compliance** — "Download my data" and "Delete my account" options
- [ ] **Session management** — see and revoke active login sessions

---

## 🏛️ Suggested Tech Stack (Full Picture)

```
┌─────────────────────────────────────────────────────┐
│                     FRONTEND                        │
│   React + Vite  │  React Query  │  TailwindCSS      │
│   React Router  │  Socket.io-client                 │
└──────────────────────────┬──────────────────────────┘
                           │ HTTP / WebSocket
┌──────────────────────────▼──────────────────────────┐
│                      BACKEND                        │
│   Node.js + Express  │  JWT Auth  │  Socket.io      │
│   OpenAI API  │  Passport.js (OAuth)                │
└──────────────────────────┬──────────────────────────┘
                           │
┌──────────────────────────▼──────────────────────────┐
│                    DATABASE                         │
│   MongoDB (notes, users)                           │
│   Redis (sessions, caching)                        │
│   Pinecone / pgvector (AI embeddings for search)   │
└─────────────────────────────────────────────────────┘
                           │
┌──────────────────────────▼──────────────────────────┐
│                   INFRASTRUCTURE                    │
│   AWS S3 (file storage)  │  Vercel (frontend)       │
│   Railway / Render (backend)  │  MongoDB Atlas      │
└─────────────────────────────────────────────────────┘
```

---

## 🎯 Recommended Order to Build

If you want a step-by-step path, here's the smartest order:

```
1. Add backend (Express + MongoDB)        ← makes it a real app
2. Add authentication (JWT + signup/login) ← makes it personal
3. Rich text editor + colors + tags        ← makes it useful
4. Search                                  ← makes it fast
5. AI summarize + auto-tag                 ← makes it impressive
6. PWA + offline mode                      ← makes it polished
7. Collaboration + sharing                 ← makes it social
8. Mobile app (React Native)              ← makes it everywhere
```

---

> 💡 Start small, ship often. Each phase above is a complete, working upgrade on its own.