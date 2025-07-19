# Resume-Checker
# 📄 Resume Analyzer based on Job Description

A ⚙️ Gradio-powered tool that analyzes resumes against job descriptions using OCR, NLP, and skill-matching to compute an ATS (Applicant Tracking System) match score and suggest best-fit roles.

---

## ✨ Features

- 🔍 Extracts text from PDF resumes using OCR (`pytesseract`, `pdf2image`)
- 🧠 Tokenizes and filters job description text to identify key skills
- 🧰 Matches extracted resume skills with predefined role-based skill sets
- 📊 Calculates ATS match score and visualizes it via a pie chart
- 💡 Suggests best-fit roles and gives actionable feedback

---

## 💼 Predefined Roles & Skills

Supported roles include:
- 🤖 AI/ML Intern  
- 📊 Data Analyst  
- 🌐 Web Developer  
- 🛠️ Backend Developer  
- ☁️ Cloud Engineer  
- 🔧 DevOps Engineer  
- 🛡️ Cybersecurity Analyst  
- 📈 Data Scientist  
- 📋 Business Analyst  
- 🧩 Full Stack Developer  

Each role has a mapped list of recommended skills used for scoring and role matching.

---

## 🧾 Requirements

Install the following:

```bash
pip install gradio pdf2image pytesseract nltk matplotlib PyMuPDF
apt-get install -y poppler-utils
```

NLTK downloads required:

```python
import nltk
nltk.download("punkt")
nltk.download("stopwords")
```

---

## 🧠 How It Works

1. 🖼️ **Resume Parsing**: Converts PDF to images, then extracts text using `pytesseract`.
2. ✍️ **JD Analysis**: Tokenizes and filters out stopwords from the job description.
3. 🧮 **Skill Matching**: Compares resume content with predefined skill sets.
4. 📈 **Scoring**: Computes a match percentage based on overlapping skills.
5. 🥧 **Visualization**: Generates a pie chart of the ATS score.
6. 📌 **Feedback**: Suggests role(s) based on skill match strength.

---

## 🚀 Usage

Run the interface locally or with shareable link:

```python
demo.launch(share=True)
```

📥 Input:
- PDF Resume file
- Text Job Description

📤 Output:
- 🥧 Pie chart image of ATS match score
- 📝 Markdown block with suggestions and best-fit roles

---

## 🗂️ File Structure

- Resume parsing and skill extraction
- JD keyword extraction
- Role and skill definitions
- Gradio interface setup

---
