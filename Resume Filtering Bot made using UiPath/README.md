# **Automated Resume Classification Bot (UiPath)**

This UiPath project automatically analyzes and classifies a large collection of resumes (100+ CVs) by applying OCR, extracting key information, checking for required skills/keywords, and categorizing each resume as **Shortlisted** or **Rejected**.
All results are exported to separate Excel files for easy review.

---

## 📂 **Project Folder Structure**

Based on your project directory:

```
Automated Resume Filter Bot/
│
├── .entities
├── .objects
├── .project
├── .settings
├── .templates
├── .tmh
│
├── Resume Classification/         ← Automation outputs & logic folder
├── Resume_CVs/                    ← Contains 100+ resumes for screening
│
├── Sequence.xaml                  ← Primary workflow file
├── project.json                   ← Project configuration
└── README.md
```

### **Key Folders**

* **Resume_CVs** — Source resumes (PDF) for classification
* **Resume Classification** — Contains generated Excel sheets for shortlisted and rejected candidates

---

## 🧠 **Workflow Summary**

The automation follows a structured, rule-based approach for processing resumes.
The workflow implements the following stages:

---

### **1️⃣ Resume Source Initialization**

The bot begins by defining the folder path containing all resumes.
All CV files within the directory are retrieved dynamically, allowing the bot to process large batches (100+ files) without manual intervention.

---

### **2️⃣ Resume File Retrieval**

The automation scans the `Resume_CVs` directory and identifies all supported file formats.
Each file path is added to a collection, which becomes the input set for the subsequent processing loop.

---

### **3️⃣ Output DataTables Construction**

Two output datasets are created:

* **shortlistedDT**
* **rejectedDT**

Each DataTable includes schema fields such as:

* Candidate Name
* File Name
* Extracted Keywords
* Match Score 
* Classification Status

These tables serve as structured repositories for the classification results.

---

### **4️⃣ Iterative Processing of Each Resume**

Each resume undergoes the following operations inside a controlled iteration loop:

#### **✔ OCR-Based Text Extraction**

The bot uses UiPath’s PDF and Document Understanding capabilities to extract textual content from resumes, supporting scanned and digital files.

#### **✔ Keyword Matching Algorithm**

Extracted text is analyzed using a predefined set of skills or role-specific keywords.
A threshold-based logic determines whether a candidate qualifies for shortlisting.

#### **✔ Classification Decision**

Based on keyword presence and scoring logic, the candidate is categorized as:

* **Shortlisted**, or
* **Rejected**

The classification is logged into the corresponding DataTable.

---

### **5️⃣ Excel Output Generation**

The automation exports the processed results into:

* `Shortlisted_CVs.xlsx`
* `Rejected_CVs.xlsx`

These files are placed under the **Resume Classification** folder and serve as the final outcome of the automation.

---

## ⚙️ **Dependencies**

The project uses the following UiPath packages (defined in `project.json`):

* UiPath.DocumentUnderstanding.Activities
* UiPath.PDF.Activities
* UiPath.Excel.Activities
* UiPath.System.Activities
* UiPath.Mail.Activities
* UiPath.IntegrationService.Activities

All dependencies are automatically restored when the project is opened in UiPath Studio.

---

## ▶️ **How to Run the Automation**

1. Open the project in **UiPath Studio**
2. Verify project dependencies are restored
3. Place all resumes inside the **Resume_CVs** folder
4. Review or update keyword lists (if applicable)
5. Run the workflow from **Sequence.xaml**
6. Retrieve the classification outputs from the **Resume Classification** folder

---

## 📝 **Output Files**

The bot generates structured Excel reports:

| Output File              | Description                                        |
| ------------------------ | -------------------------------------------------- |
| **Shortlisted_CVs.xlsx** | Contains resumes that meet the keyword threshold   |
| **Rejected_CVs.xlsx**    | Contains resumes with insufficient keyword matches |

Each record includes:

* File name
* Candidate details
* Identified keywords
* Match evaluation
* Final classification

---

## 🚀 **Scalability**

The bot is designed to handle:

* Large resume volumes (100+ files)
* Multiple document formats
* Flexible keyword sets
* Extensible workflows (e.g., emailing shortlisted candidates, adding ML scoring)

This makes it suitable for deployment in HR departments or recruitment agencies.

---

## 💡 **Future Enhancements**

* Integration with **AI-Based Resume Ranking Models**
* Mapping of resume sections (Experience, Education, Skills)
* Cloud-based execution via UiPath Orchestrator
* Automated email notifications for shortlisted candidates
* Dashboard visualization of classification statistics

---

## 🙌 **About This Project**

This project demonstrates the use of UiPath RPA for real-world HR automation.
It applies OCR, keyword rule engines, and bulk file processing techniques to deliver an efficient resume screening workflow that minimizes manual effort and increases operational accuracy.

---
