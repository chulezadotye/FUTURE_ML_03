# Resume Screening and Candidate Ranking System – Project Report

## 1. Introduction

Recruitment teams often receive many applications for a single job position. Manually reviewing every resume can be time-consuming.

This project develops a machine learning-based Resume Screening and Candidate Ranking System. It uses Natural Language Processing (NLP) techniques to extract skills, compare resumes with job descriptions, identify missing skills, and rank candidates according to their suitability.

## 2. Project Objectives

The main objectives are:

- Extract relevant information and skills from resumes.
- Clean and preprocess resume text.
- Compare resumes against a job description.
- Calculate candidate skill matching scores.
- Rank candidates based on their final scores.
- Identify missing skills.
- Present results through tables and visualizations.

## 3. Dataset Description

The project uses the Kaggle Resume Dataset.

- Total resumes processed: 2,484
- Resumes retained after cleaning: 2,483
- Resume format: PDF
- Categories: 24 professional categories.

One resume was removed because it contained no usable extracted text.

## 4. Technologies and Tools

The following technologies were used:

- Python
- Google Colab
- Pandas
- Scikit-learn
- PyPDF
- Matplotlib
- Seaborn
- Regular Expressions (Regex)

## 5. Methodology

### 5.1 Resume Text Extraction

PDF files were processed using PyPDF to extract text from resumes.

### 5.2 Data Cleaning and Preprocessing

The extracted text was cleaned by:

- Converting text to lowercase.
- Removing email addresses and URLs.
- Removing unnecessary numbers and special characters.
- Removing extra spaces.
- Normalizing Unicode characters.

### 5.3 Skills Extraction

A predefined skills dictionary and keyword matching were used to identify relevant skills in each resume.

The system extracted technical and professional skills such as Python, Java, SQL, Excel, Power BI, communication, research, and project management.

### 5.4 Job Description Analysis

A Junior Data Analyst job description was created with nine required skills:

1. Python
2. SQL
3. Excel
4. Power BI
5. Data Analysis
6. Database Management
7. Communication
8. Problem Solving
9. Research

### 5.5 Resume Similarity Scoring

TF-IDF vectorization was used to convert resume and job description text into numerical representations.

Cosine similarity measured how closely each resume matched the job description.

### 5.6 Skills Matching

The system compared extracted candidate skills against the nine required skills.

It calculated a skill match percentage and identified matched and missing skills.

### 5.7 Candidate Ranking

The final score was calculated using:

**Final Score = (0.60 × Skill Match Score) + (0.40 × Similarity Score)**

Candidates were ranked from the highest final score to the lowest.

## 6. Experimental Results

The system successfully screened 2,483 resumes.

### 6.1 Top Candidate

The highest-ranked candidate achieved:

| Metric | Result |
|---|---:|
| Candidate ID | 25397102 |
| Category | BUSINESS-DEVELOPMENT |
| Similarity Score | 17.94% |
| Skill Match Score | 66.67% |
| Final Score | 47.18% |

### 6.2 Matched Skills

- Python
- SQL
- Excel
- Communication
- Problem Solving
- Research

### 6.3 Missing Skills

- Power BI
- Data Analysis
- Database Management

### 6.4 Additional Results

The system generated:

- Complete candidate rankings.
- Top 10 candidate rankings.
- Missing skills analysis.
- Top 10 candidate visualization.
- Missing skills visualization.
- Similarity score distribution chart.

The average final candidate score was 12.11%.

## 7. Models and Configuration

The project saved two files:

- `tfidf_vectorizer.joblib`
- `screening_configuration.joblib`

These files store the fitted TF-IDF vectorizer and the screening configuration, including the job description and required skills.

## 8. Limitations

The project has some limitations:

- Keyword matching may fail to recognize skills expressed using different words.
- TF-IDF does not fully understand the meaning or context of resumes.
- The predefined skills dictionary may not cover every relevant skill.
- Results depend on the selected job description and required skills.
- The scoring method is experimental and has not been validated against real recruitment outcomes.

## 9. Ethical Considerations

The system should be used as a decision-support tool rather than an automatic hiring decision-maker.

Recruiters should review candidate information carefully, check for unfair bias, and ensure that all candidates are evaluated fairly. Sensitive personal information should be protected.

## 10. Conclusion

The project successfully demonstrates how Python and NLP techniques can be used to automate parts of the resume screening process.

The system extracts skills, compares resumes with job descriptions, calculates matching scores, identifies missing skills, and ranks candidates.

The project provides a foundation for developing more advanced recruitment systems using improved NLP techniques and machine learning models.

## 11. Future Improvements

Possible improvements include:

- Using advanced NLP models such as BERT or spaCy.
- Improving skill extraction with synonyms and contextual understanding.
- Supporting multiple job descriptions.
- Adding an interactive recruiter dashboard.
- Improving fairness and evaluating the system on real recruitment outcomes.

## 12. Project Information

**Programme:** Future Interns – Machine Learning Internship 2026

**Task:** Machine Learning Task 3 – Resume / Candidate Screening System

**Author:** Chuleza Dotye

**Programming Language:** Python
