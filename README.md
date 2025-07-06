# 💼 Resume–Job Description Matching using NLP

This project automates the matching of resumes to job descriptions using **Natural Language Processing (NLP)** techniques like `TF-IDF`, `Cosine Similarity`, and visual analysis with heatmaps.

## 🧠 Key Concepts Used

- **Text Cleaning** using `nltk`
- **Resume Text Extraction** from PDF using `PyMuPDF (fitz)`
- **TF-IDF Vectorization**
- **Cosine Similarity** for document matching
- **Heatmap Visualization** using `Seaborn`

## 📦 Workflow Summary

### 📍 Step 1: Preprocessing Job Descriptions
- Load job descriptions from a CSV file.
- Apply:
  - Lowercasing
  - Tokenization (`nltk.word_tokenize`)
  - Stopword removal (`nltk.corpus.stopwords`)
  - Lemmatization (`WordNetLemmatizer`)
- Save as: `processed_job_descriptions.csv`

### 📍 Step 2: Extract & Preprocess Resume PDFs
- Unzip and extract resumes.
- For each resume PDF:
  - Use `fitz` to extract text page-by-page
  - Apply the same preprocessing steps
- Save as: `processed_resumes.csv`

### 📍 Step 3: Matching Resumes with Jobs
- Use `TfidfVectorizer` on both processed datasets.
- Compute similarity using `cosine_similarity()`
- For each resume:
  - Find top 3 matching jobs
- Save match results to: `resume_job_matches.csv`

### 📍 Step 4: Visualizing Results
- Create a heatmap of top N resume vs job similarity scores
- Display with annotated scores using `Seaborn`

## 🗂️ Datasets Used

1. **Gaurav Dutta Resume Dataset** – Kaggle  
2. **Indeed Resume Dataset** – DataStock  
3. **Job Descriptions Dataset** – Ravindra Singh Rana (Kaggle)


## 🔧 Technologies Used

- **Python Libraries**:
  - `nltk`, `pandas`, `numpy`
  - `scikit-learn` (`TfidfVectorizer`, `cosine_similarity`)
  - `PyMuPDF (fitz)` for PDF parsing
  - `matplotlib`, `seaborn` for visualization
 
## 📌 Use Cases

- Automating recruitment pipelines
- Resume screening and shortlisting
- Candidate-job role recommendations
- HR tech applications and career portals

