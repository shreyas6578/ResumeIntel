

## 🧠 AI Resume Analyzer (🔍 New Feature)

The **AI Resume Analyzer** is a robust end-to-end **Streamlit web app** that helps users enhance their resumes by providing automated parsing, grammar and readability feedback, career path insights, personalized skill and course recommendations, and an **AI-powered cover letter generator**. It also includes an **Admin Dashboard** to monitor usage and metrics.

---

### 🚀 Features

#### ✅ 1. Automated Resume Parsing
- Extracts **raw resume text** using `PDFMiner`.
- Uses `PyResparser` to extract structured data like:
  - 📛 Name
  - 📧 Email
  - 📞 Phone Number
  - 🧠 Skills
  - 📄 Page Count
- Helps users quickly verify their resume structure and key information.

#### 📘 2. Grammar & Readability Feedback
- Highlights major **spelling** and **grammar** issues using `LanguageTool`.
- Computes various **readability metrics** through `Textstat`, such as:
  - **Flesch Reading Ease**
  - **Gunning Fog Index**
  - **SMOG Index**
  - **Coleman–Liau Index**
  - **Automated Readability Index (ARI)**
- Provides feedback on the professional quality and clarity of the resume.

#### 🎯 3. Skill Tagging & Career Field Inference
- Uses `streamlit-tags` to display and **edit detected skills**.
- Automatically infers the user’s likely **career path**:
  - 👨‍💻 Data Science
  - 🌐 Web Development
  - 📱 Android/iOS Development
  - 🎨 UI/UX Design
- Based on the inferred track, recommends:
  - 🔧 Additional important skills
  - 🎓 Curated courses to upskill

#### 📊 4. Resume Strength Meter
- Checks for presence of **essential sections** like:
  - Objective
  - Projects
  - Experience
  - Education
  - Certifications
- Calculates a **completeness score** based on best practices.
- Animates a visual **progress bar** showing resume strength.

#### 📝 5. AI-Powered Cover Letter Generator
- Generates personalized **cover letters** using **Google Gemini 2.0 Flash API**.
- Customizable options:
  - 🎯 Desired tone (Formal, Friendly, Enthusiastic, etc.)
  - ✍️ Length (Short, Medium, Long)
  - ⭐ Skills to highlight
  - ❌ Buzzword removal toggle
- Users can **download** the generated cover letter in:
  - `.docx` (Microsoft Word format)
  - `.txt` (Plain text format)

#### 👨‍💼 6. Admin Dashboard
- Secured with a simple **admin login**.
- Lets admins:
  - View all past resume analyses
  - Download data as `.csv` or view in-browser
  - Analyze user activity and skill trends
- Displays **key analytics** such as:
  - 👥 Total users
  - 📈 Most common career fields
  - 📊 Average skill levels detected
- Interactive visualizations using `Plotly`, including:
  - Pie Charts
  - Bar Graphs
  - Time Series Trends
  - Heatmaps

---

### 📦 Tech Stack & Dependencies

#### 🧰 Backend & App Framework
- `Streamlit` — Fast UI development for Python apps

#### 📄 Resume Parsing & NLP
- `PDFMiner` — Extracts raw text from PDF files
- `PyResparser` — Extracts structured resume info (name, email, skills)
- `NLTK` — Natural Language Processing tasks

#### 🧠 AI & Readability Tools
- `LanguageTool-Python` — Grammar and spelling analysis
- `Textstat` — Readability scoring and text complexity

#### ✍️ AI Cover Letter Generator
- `google-generativeai` — Integrates **Gemini 2.0 Flash** for text generation

#### 💾 Database & Persistence
- `MySQL` — Stores analysis results and user logs
- `pymysql` — Python MySQL connector

#### 🎛️ UI Enhancements
- `streamlit-tags` — Editable skill tags interface
- `Plotly` — Interactive visual charts (bar, pie, heatmaps, etc.)
- `Pillow` — Image handling and formatting

#### 📁 Document Generation
- `python-docx` — Exports cover letters in `.docx` format
- `base64`, `pafy`, `pandas`, `numpy` — Data handling and formatting

---

### 📥 Installation

Make sure Python 3.8+ is installed.

Then install the required libraries:

```bash
pip install streamlit nltk google-generativeai python-docx pymysql \
    pdfminer.six pyresparser language-tool-python textstat \
    streamlit-tags plotly pafy pandas pillow
```

---


---

### 🛠️ How to Run the App

```bash
streamlit run app.py
```

---
