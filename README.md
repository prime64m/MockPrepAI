# MockPrep AI

MockPrep AI is an advanced, AI-powered mock interview platform designed to simulate realistic technical interviews. It analyzes a candidate's resume and conducts a rigorous, multi-stage interview complete with webcam proctoring, immersive 3D environments, and highly detailed, brutally honest feedback.

## 🚀 Features

- **📄 Intelligent Resume Parsing:** Upload a PDF resume to automatically extract context, allowing the AI to tailor questions specifically to your background and experience.
- **🧠 Dynamic AI Question Generation:** Powered by local LLMs (Ollama + Llama 3.2), the system generates relevant, section-specific interview questions (both multiple-choice and subjective) tailored to the target role and difficulty.
- **🎙️ Interactive Interview Room:** A fully immersive 3D interview environment built with React Three Fiber, providing a professional and engaging user experience.
- **👁️ Webcam Proctoring & Face Tracking:** Integrates `face-api.js` for live face tracking, ensuring interview integrity and focus.
- **📊 Comprehensive Evaluation:** At the end of the interview, the AI acts as a strict technical interviewer to grade responses. It provides detailed question-by-question breakdowns, correct solutions, and a final percentage score.
- **✨ Modern UI/UX:** A responsive, animated interface built with React, Vite, Framer Motion, and custom CSS.

## 🛠️ Technology Stack

**Frontend:**
- **Framework:** React 19, Vite
- **3D Graphics:** Three.js, `@react-three/fiber`, `@react-three/drei`
- **Animations:** Framer Motion
- **Webcam/Proctoring:** `face-api.js`
- **Icons:** `lucide-react`
- **Routing:** React Router DOM

**Backend:**
- **Server:** Node.js, Express.js
- **File Uploads:** Multer
- **PDF Processing:** `pdf-parse`

**AI Integration:**
- **Local Inference:** Ollama (defaulting to the `llama3.2` model)
- *Note: The architecture is currently being optimized for a cloud-hosted Vercel deployment with the Groq API (Llama-3.3-70b-versatile) for production.*

## 📁 Project Structure

```text
mockPrep AI/
├── server/                 # Express backend directory
│   ├── server.js           # Main backend entry point, API routes
│   ├── package.json        # Backend dependencies
│   └── uploads/            # Temporary storage for uploaded resumes
├── src/                    # React frontend directory
│   ├── components/         # Reusable UI components (Navbar, Button, 3D Scene)
│   ├── pages/              # Main application views (Landing, Dashboard, InterviewRoom, Result)
│   ├── App.jsx             # Main application component & routing
│   └── main.jsx            # React DOM rendering entry point
├── package.json            # Frontend dependencies
└── vite.config.js          # Vite configuration
```

## ⚙️ Setup and Installation

### Prerequisites
1. **Node.js** (v18 or higher recommended)
2. **Ollama**: You must have [Ollama](https://ollama.com/) installed locally to run the AI models.

### 1. Start the AI Backend (Ollama)
Ensure Ollama is running and download the required model:
```bash
ollama run llama3.2
```

### 2. Start the Express Backend
Open a terminal and navigate to the `server` directory:
```bash
cd server
npm install
npm start
```
The backend will start on `http://localhost:3001`.

### 3. Start the Frontend Development Server
Open a new terminal and navigate to the project root:
```bash
npm install
npm run dev
```
The Vite development server will start on `http://localhost:5173`.

## 🛣️ Roadmap / Upcoming Features
- [ ] Complete migration to Vercel Serverless Functions.
- [ ] Replace local Ollama dependency with Groq API (Llama-3.3-70b-versatile) for cloud scalability.
- [ ] Integrate MongoDB for persistent user profiles, past interview history, and JWT authentication.
- [ ] Implement enhanced dictation (Voice-to-Text) stability for hands-free interviewing.
- [ ] Expand proctoring to include tab-switching and keyboard shortcut blocking.

---
*Built for the ultimate interview preparation experience.*
