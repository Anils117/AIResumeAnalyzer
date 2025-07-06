# 🧠 AI Resume Analyzer using NLP

An AI-powered Resume Analyzer built using Python, NLP (spaCy), and Streamlit. It extracts key information like name, email, phone number, skills, education, and more from uploaded resumes (PDF/DOCX), and provides personalized feedback or recommendations.

---

## ✨ Features

* Extracts resume fields: Name, Email, Phone, Skills, Degree, Page Count
* Skill matching using a predefined list
* Streamlit-powered web UI
* Geolocation capture (optional)
* Admin Dashboard (optional)

---

## 🧰 Tech Stack

* Python 3.9.12
* Streamlit
* spaCy 2.3.5
* `en_core_web_sm` 2.3.1 model
* pyresparser
* geocoder, geopy
* PDF and DOCX parsing tools

---

## ⚙️ Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/AI-Resume-Analyzer.git
cd AI-Resume-Analyzer
```

---

### 2. Create and Activate a Virtual Environment

```bash
python -m venv .venv
```

**Activate:**

* On Windows:

```bash
.venv\Scripts\activate
```

* On Unix/Mac:

```bash
source .venv/bin/activate
```

---

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

Or manually install the key packages:

```bash
pip install spacy==2.3.5
pip install streamlit
pip install pyresparser
pip install pdfminer.six docx2txt
pip install geopy geocoder
```

---

### 4. Install spaCy Model (`en_core_web_sm`)

```bash
python -m spacy download https://github.com/explosion/spacy-models/releases/download/en_core_web_sm-2.3.1/en_core_web_sm-2.3.1.tar.gz
```

If the above fails, download and install locally:

```bash
wget https://github.com/explosion/spacy-models/releases/download/en_core_web_sm-2.3.1/en_core_web_sm-2.3.1.tar.gz
python -m spacy install en_core_web_sm-2.3.1.tar.gz
```

---

### 5. Downgrade `setuptools` (if model install fails)

```bash
pip install setuptools==58.0.4
```

---

### 6. Run the App

```bash
streamlit run App/App.py
```

---

## 📌 Notes

* This project uses `pyresparser`, which works best with spaCy v2.x.
* Custom NER is disabled for now to avoid config errors.
* Ensure PDF/DOCX files are clean for optimal parsing.
* Works best with English resumes.

---
