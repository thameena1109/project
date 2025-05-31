
# Multi-Agent Document Classifier with Streamlit UI

This is a Python-based multi-agent system designed to classify and extract information from uploaded files (PDF, JSON, or Email in `.txt` format) using a Streamlit interface.

---

##  Features

- Upload files via **Streamlit UI**.
- Detect file **format** and **intent** using `ClassifierAgent`.
- Route files to the correct agent:
  - 📧 `EmailAgent` — Extracts sender, subject, and priority from plain text emails.
  - 🧾 `JSONAgent` — Extracts `id`, `type`, `amount` and reports anomalies.
  - 📄 `PDFAgent` — Extracts raw text from PDF files using `PyPDF2`.
- All outputs and logs are stored in a **SQLite database** (`shared_memory.db`).

---

## 🗂️ Project Structure

```
EMAIL1/
│
├── multi_agent_system/
│   ├── classifier_agent.py
│   ├── email_agent.py
│   ├── json_agent.py
│   ├── main.py
│   ├── pdf_agent.py
│   ├── shared_memory.py
│   ├── test_agents.py
│   └── __pycache__/...
│
├── streamlit_ui.py
├── shared_memory.db
├── shared_memory.json
├── requirements.txt
└── INSTALLATION_AND_RUN_INSTRUCTIONS.md
```

---

##  How to Run

1. **Install dependencies**:

```bash
pip install -r requirements.txt
```

2. **Run the Streamlit app**:

```bash
streamlit run streamlit_ui.py
```

---

##  How to Use

* Open the app in your browser (auto opens when Streamlit runs).
* Upload a `.pdf`, `.json`, or `.txt` file.
* View format, intent, extracted content, and memory logs.

---

##  Dependencies

* `streamlit`
* `PyPDF2`
* `sqlite3`
* `json`
* `datetime`

---

##  Memory Storage

All interactions are logged into `shared_memory.db`, including:

* File format
* Intent
* Extracted fields
* Timestamp

---

##  License

This project is for educational and demo purposes.

---

## drive link for project

https://drive.google.com/file/d/1Vpk2B67kzhesqHTMAmiZmnWclDEP-jYC/view?usp=sharing
