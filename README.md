# 🎓 EduGenie – Gemini Learning Assistant

EduGenie is an AI-powered learning assistant designed to help students learn, understand, and revise academic topics using **Google Gemini Generative AI**.

The application can be developed as an interactive learning platform where students enter a topic or question and receive simple, personalized explanations, examples, summaries, quizzes, and study support.

> **Repository:** https://github.com/priya12pri2007-cpu/EduGenie-Gemini-Learning-Assistant

## 📌 Project Overview

EduGenie aims to make learning easier by combining a simple student-friendly interface with Generative AI.

### Main Objectives

- Provide AI-based learning assistance.
- Explain difficult concepts in simple language.
- Generate topic summaries and study notes.
- Create practice questions and quizzes.
- Give examples based on the student's question.
- Provide an interactive learning experience.
- Reduce the time required to prepare study material.

---

# ✨ Key Features

- 🤖 **AI Learning Assistant**
- 💬 **Question & Answer Support**
- 📚 **Topic Explanation**
- 📝 **Automatic Notes/Summary Generation**
- ❓ **Quiz / Practice Question Generation**
- 🎯 **Personalized Learning Prompts**
- 🧠 **Google Gemini Integration**
- 🌐 **Simple Web-Based Interface**
- ⚡ **Real-Time AI Responses**

---

# 🏗️ Project Structure

A suitable full-stack structure for EduGenie is:

```text
EduGenie-Gemini-Learning-Assistant/
│
├── app.py
├── requirements.txt
├── README.md
├── .env
├── .gitignore
│
├── templates/
│   └── index.html
│
├── static/
│   ├── css/
│   │   └── style.css
│   │
│   └── js/
│       └── script.js
│
└── assets/
    └── images/
```

> **Important:** The GitHub repository currently visible from the supplied link contains project-document PDFs (for example, brainstorming, problem-statement, and empathy-map documents). The source-code files above describe the recommended implementation structure; they should be changed to match the actual code files when the application source is uploaded.

---

# 💻 Front-End

The front-end is the part of EduGenie that students directly interact with.

### Front-End Technologies

- HTML5
- CSS3
- JavaScript
- Jinja2 templates (if Flask is used)

### Front-End Functions

The interface can provide:

1. Student question/topic input.
2. Learning mode selection.
3. Generate button.
4. AI answer display.
5. Summary/notes display.
6. Quiz generation.
7. Clear/reset controls.
8. Responsive student-friendly design.

### Example Front-End Flow

```text
Student
   ↓
Enter Topic / Question
   ↓
Click Generate
   ↓
JavaScript sends request
   ↓
Backend API
   ↓
Gemini AI
   ↓
AI Response
   ↓
Display Result on Web Page
```

---

# ⚙️ Back-End

The back-end manages the application logic and communication with Gemini AI.

### Back-End Technologies

- Python
- Flask
- Google Gemini API / Google Generative AI SDK
- Python-dotenv
- JSON
- HTTP/API handling

### Back-End Responsibilities

1. Receive the student's input.
2. Validate the input.
3. Build an appropriate AI prompt.
4. Send the prompt to Google Gemini.
5. Receive the AI-generated response.
6. Process the response.
7. Send the result back to the front-end.
8. Handle API errors safely.

---

# 🤖 AI Technology Used

## Google Gemini Generative AI

The main AI technology used for EduGenie is **Google Gemini**.

Gemini can understand natural-language questions and generate educational responses based on the student's prompt.

### AI Capabilities

EduGenie can use Gemini for:

- Concept explanations
- Summaries
- Notes
- Examples
- Practice questions
- MCQs
- Revision assistance
- Personalized learning responses

### AI Workflow

```text
Student Input
      ↓
Python Backend
      ↓
Prompt Creation
      ↓
Google Gemini API
      ↓
Gemini Model
      ↓
Generated Educational Content
      ↓
Backend
      ↓
Frontend
      ↓
Student
```

---

# 🧠 Prompt Engineering

EduGenie can create structured prompts so that Gemini produces student-friendly answers.

### Example Prompt

```text
You are EduGenie, an educational AI assistant.

Explain the following topic in simple language.

Topic:
{student_topic}

Requirements:
- Give a clear definition.
- Explain the concept step by step.
- Give a simple example.
- Mention important points.
- Keep the explanation suitable for a student.
```

For quiz generation:

```text
Create 5 multiple-choice questions about:

{topic}

For each question:
1. Give four options.
2. Identify the correct answer.
3. Give a short explanation.
```

---

# 📁 File Description

| File / Folder | Purpose |
|---|---|
| `app.py` | Main Python application and backend logic |
| `requirements.txt` | Python packages required by the project |
| `.env` | Stores the Gemini API key locally |
| `.gitignore` | Prevents secret and unnecessary files from being uploaded |
| `templates/index.html` | Main web interface |
| `static/css/style.css` | Front-end styling |
| `static/js/script.js` | Front-end interaction and API requests |
| `assets/` | Images and other UI resources |
| `README.md` | Project documentation |

---

# 🛠️ Technologies at a Glance

| Category | Technology |
|---|---|
| Programming Language | Python |
| Front-End | HTML, CSS, JavaScript |
| Backend Framework | Flask |
| AI | Google Gemini Generative AI |
| API Communication | HTTP / JSON |
| Environment Variables | python-dotenv |
| Version Control | Git & GitHub |

---

# 🔐 API Key Configuration

Create a `.env` file in the project folder:

```text
GEMINI_API_KEY=your_gemini_api_key
```

Do **not** upload the real API key to GitHub.

Add the following to `.gitignore`:

```text
.env
__pycache__/
*.pyc
venv/
```

---

# 📦 Installation

## 1. Clone the Repository

```bash
git clone https://github.com/priya12pri2007-cpu/EduGenie-Gemini-Learning-Assistant.git
```

## 2. Open the Project

```bash
cd EduGenie-Gemini-Learning-Assistant
```

## 3. Create a Virtual Environment

```bash
python -m venv venv
```

### Windows

```bash
venv\Scripts\activate
```

### Linux / macOS

```bash
source venv/bin/activate
```

## 4. Install Dependencies

```bash
pip install -r requirements.txt
```

## 5. Add Gemini API Key

Create `.env`:

```text
GEMINI_API_KEY=your_gemini_api_key
```

## 6. Run the Application

For a Flask application:

```bash
python app.py
```

Then open:

```text
http://127.0.0.1:5000
```

---

# 🔄 Application Workflow

```text
┌─────────────────────┐
│       Student       │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│  Enter Topic /      │
│  Question           │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│   Front-End         │
│ HTML/CSS/JavaScript │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│ Python Flask        │
│ Backend             │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│ Google Gemini AI    │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│ Generated Learning  │
│ Content             │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│ Display Result      │
│ to Student          │
└─────────────────────┘
```

---

# 🌟 Innovative Aspects

### 1. AI-Based Personalized Learning

Instead of showing the same fixed content to every student, Gemini can generate responses based on the student's question and learning requirement.

### 2. Simple-Language Explanations

Students can request difficult concepts to be explained in simple language.

### 3. Multiple Learning Modes

The same topic can be converted into:

```text
Topic
 ↓
Explanation
 ↓
Summary
 ↓
Examples
 ↓
Quiz
 ↓
Revision
```

### 4. Interactive Learning

Students can continue asking follow-up questions instead of only reading static notes.

### 5. Generative AI Integration

The project demonstrates how a Generative AI model can be integrated into a real student-oriented application.

---

# 🎯 Use Cases

EduGenie can be useful for:

- College students
- School students
- Exam preparation
- Quick revision
- Concept clarification
- Practice questions
- Self-learning
- Academic project demonstrations

---

# 🔮 Future Enhancements

- 📄 PDF upload and document-based learning
- 🎤 Voice-based questions
- 🔊 Text-to-speech answers
- 🌐 Multi-language learning
- 📊 Student progress dashboard
- 🧠 Personalized learning paths
- 📝 Automatic question-paper generation
- 🃏 Flashcard generation
- 📅 AI study planner
- 💾 Learning history
- 🔐 Student login and profiles

---

# ⚠️ Security

Never expose your Gemini API key in source code or commit it to GitHub.

Use:

```text
.env
```

and keep it inside `.gitignore`.

---

# 📜 License

This project can be released under the MIT License if the project owner chooses to use that license.

---

# 👩‍💻 Project

**Project Name:** EduGenie – Gemini Learning Assistant

**Repository:**  
https://github.com/priya12pri2007-cpu/EduGenie-Gemini-Learning-Assistant

**AI Technology:** Google Gemini Generative AI

**Purpose:** AI-powered educational assistance and personalized learning
