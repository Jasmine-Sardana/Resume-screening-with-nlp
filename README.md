# Resume–Job Description Analyzer

This project automates the process of matching resumes to job descriptions using Natural Language Processing (NLP) and Machine Learning techniques.  
It provides similarity scoring, keyword comparison, skill classification, and identifies missing skills to generate data-driven recommendations.

---

## Key Features

- **Resume Parsing** – Extracts text content from PDF and DOCX resumes using `pdfplumber`, `PyPDF2`, and `textract`.
- **Job Description Input** – Accepts a raw text job description for analysis.
- **Resume–JD Similarity** – Calculates textual similarity using `CountVectorizer` and `cosine_similarity`.
- **Spelling Correction** – Detects and suggests corrections for spelling errors.
- **Summarization** – Generates a concise summary of resumes using `facebook/bart-large-cnn`.
- **Keyword Extraction** – Utilizes RAKE (`rake_nltk`) for identifying key phrases from resumes and job descriptions.
- **Skill Matching** – Classifies resume content into five core data science areas:
  - Data Engineering & Warehousing  
  - Data Mining & Statistical Analysis  
  - Cloud & Distributed Computing  
  - Machine Learning & AI  
  - Data Visualization
- **Gap Analysis** – Detects missing skills relative to the job description and suggests targeted resources for improvement.
- **Importance Ranking** – Ranks missing skills based on their frequency and normalized importance within the job description.
- **Visual Analysis** – Generates skill classification pie charts using `matplotlib`.

---

## Tech Stack

- **Languages:** Python  
- **Libraries:** PyPDF2, pdfplumber, textract, docx2txt, pandas, matplotlib, scikit-learn, spellchecker, transformers, nltk, rake-nltk, spaCy  
- **Model Used:** `facebook/bart-large-cnn` (for summarization)

---

## Workflow Overview

1. **Extract Text** from resume PDFs.  
2. **Preprocess and Clean** data for uniformity.  
3. **Input Job Description** from user.  
4. **Compute Similarity Score** using Bag-of-Words and cosine similarity.  
5. **Detect Spelling Errors** and suggest corrections.  
6. **Summarize Resume** using a transformer model.  
7. **Extract Keywords** from both resume and JD.  
8. **Perform Skill Classification** and visualize results.  
9. **Identify Missing Skills** and recommend resources.  
10. **Rank Missing Skills** by importance to JD context.

---

## Sample Results

**Resume–JD Similarity:** 54.83%  
**Jaccard Score:** 0.5375  
**Top Skill Categories:**  
- Data Visualization (11 matches)  
- ML & AI (9 matches)  
- Cloud Computing (9 matches)

**Top Missing Skills:** `statistics`, `experimental design`, `data visualization tools`, `math`

**Recommended Learning Resources:**  
- *Coursera – Machine Learning by Andrew Ng*  
- *Tableau Public Training*  
- *AWS Training and Certification*  

**Skill Distribution Visualization:**
(Pie chart generated using matplotlib)

---
---

## Future Enhancements

- **Web-based Interface:**  
  Develop an interactive user interface using Streamlit or Flask to allow users to upload resumes and job descriptions directly from a browser.

- **Contextual Similarity with Embeddings:**  
  Integrate advanced embedding models such as BERT or Sentence-BERT (SBERT) to compute semantic similarity beyond Bag-of-Words.

- **Multi-Resume Batch Analysis:**  
  Extend functionality to process multiple resumes simultaneously for bulk evaluation and comparison.

- **Database Integration:**  
  Store extracted features, similarity scores, and skill classifications in a structured database for easy querying and historical tracking.

- **Recruiter Dashboards:**  
  Build visual dashboards for recruiters to view analytics on candidate fit, missing skills, and improvement areas.

---

## References

- [Hugging Face Transformers](https://huggingface.co/docs/transformers/index)  
- [scikit-learn Documentation](https://scikit-learn.org/stable/documentation.html)  
- [NLTK](https://www.nltk.org/) and [RAKE-NLTK](https://pypi.org/project/rake-nltk/) for keyword extraction  
- [Coursera Data Science Specializations](https://www.coursera.org/specializations/data-science)

---


