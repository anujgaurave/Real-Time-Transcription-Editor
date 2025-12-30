# 🎧 Real-Time Transcription Editor

A full-stack web application that records audio in the browser, transcribes speech in real time, and displays it in a Word-like editable editor with word-level audio synchronization.

Built as a **production-style system** with modular architecture, real-time streaming, manual save control, and MongoDB persistence.

---

## 🚀 Features

### 🎙️ Recording & Real-Time Transcription
- Start / Stop microphone recording
- Live interim transcription while speaking
- Final transcript updates in real time
- Visual recording status indicator + timer

### ✍️ Word-Like Rich Text Editor
- Fully editable transcript
- Bold / Italic / Underline formatting
- Undo / Redo support
- Cursor-safe editing (live updates never overwrite user edits)
- Manual save control (no auto-save surprises)

### 🔊 Audio Playback + Word Sync
- Audio recorded directly in the browser
- Play recorded audio anytime
- Current word highlights during playback
- Click any word → audio seeks to that word
- Custom word → timestamp mapping (no external aligners)

### 💾 MongoDB Persistence
- Manual **Save to Database** button
- Load transcript by ID
- Edit & re-save existing transcripts
- Session-safe updates (no duplicate records)

### 🧠 Robust Sync Strategy
- Live transcription never overwrites user edits
- After editing, timestamps reset (expected & documented behavior)
- Reload restores transcript and word timeline correctly

---

## 🛠️ Tech Stack

### Frontend
- React
- Socket.IO (client)
- ContentEditable rich-text editor
- Modular components & custom hooks
- Vite

### Backend
- Flask
- Flask-SocketIO (threading mode)
- Google Speech-to-Text (streaming)
- Custom word timestamp logic

### Database
- MongoDB Atlas
- Transcript + word timeline schema

---
## ▶️ Running Locally (Backend)

```md
1. Navigate to backend directory  
   `cd backend`

2. Create virtual environment  
   `python -m venv venv`

3. Activate virtual environment (Windows)  
   `venv\Scripts\activate`

4. Install dependencies  
   `pip install -r requirements.txt`

5. Run the server  
   `python app.py`

```
---
## ▶️ Running Locally (Frontend)
```md
1. Navigate to frontend directory  
   `cd frontend`

2. Install dependencies  
   `npm install`

3. Start the development server  
   `npm run dev`

