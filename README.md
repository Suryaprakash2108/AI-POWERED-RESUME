# 🤖 AI Resume Optimizer Suite

A collection of two Python tools that help you **analyze**, **score**, and **enhance resumes** for better compatibility with **ATS (Applicant Tracking Systems)** and specific **job descriptions**.

---

## 📁 Projects Included

### 1. `ats_score.py` – ATS Score Evaluator

**Purpose**: Automatically evaluate your resume's compatibility with a job description using keyword matching and formatting scores.

#### 🔍 Features:
- Extracts and preprocesses text from `.pdf`, `.docx`, or `.txt` files
- Calculates ATS score based on keyword and formatting match
- Highlights matched and missing keywords
- Suggests improvements if ATS score is low
- Rewrites resume by:
  - Adding missing keywords to the "Skills" section
  - Creating missing standard sections like "Education", "Experience", etc.
- Exports the improved resume as a Word document

#### 🚀 How to Run:
```bash
python ats_score.py
```

#### 📦 Requirements:
```bash
pip install nltk spacy pdfplumber docx2txt python-docx
python -m spacy download en_core_web_sm
```

---

### 2. `ai_resume_builder.py` – Tailored Resume Generator

**Purpose**: Automatically tailor your resume to fit a specific job description by emphasizing matched terms and reorganizing content.

#### 🔍 Features:
- Extracts job skills, responsibilities, and qualifications using NLP
- Extracts candidate's skills and experience
- Matches resume content with job requirements
- Reorganizes and emphasizes relevant content
- Generates a tailored resume as a `.docx` file

#### 🚀 How to Run:
```bash
python ai_resume_builder.py
```

#### 📦 Requirements:
```bash
pip install nltk spacy pdfplumber docx2txt python-docx
python -m spacy download en_core_web_sm
```

---

## 🧠 Technologies Used

- **Python**
- **spaCy** – NLP for skill extraction
- **NLTK** – Text preprocessing
- **pdfplumber** – PDF parsing
- **docx2txt / python-docx** – Word document processing

---

## 💡 Example Use Case

1. You have a resume and a job description file.
2. Use `ats_score.py` to:
   - Evaluate the resume’s ATS score
   - Receive suggestions
   - Automatically rewrite it to improve compatibility
3. Use `ai_resume_builder.py` to:
   - Analyze the job description in detail
   - Reorder your resume content to emphasize job-relevant skills
   - Output a customized, tailored resume

---

## 📌 File Naming Note

Update these lines in both scripts with your actual file names:
```python
resume_path = 'your_resume.pdf'        # your resume file
job_desc_path = 'job_description.txt'  # your job description file
```

---

## 📂 Output Files

- `improved_resume.docx` – Output from `ats_score.py`
- `tailored_resume.docx` – Output from `ai_resume_builder.py`

---
