# Resume Screening and Candidate Ranking System

## Project Overview
This project develops an NLP-based Resume Screening and Candidate Ranking System using Python and Machine Learning.

The system analyses resumes, extracts relevant skills, compares candidates against a job description, identifies missing skills, and ranks candidates according to their suitability for a selected role.

## Objectives
- Extract relevant skills and keywords from resumes.
- Clean and preprocess resume text.
- Compare resumes with job descriptions.
- Calculate candidate similarity and skill match scores.
- Rank candidates according to their final scores.
- Identify missing skills for each candidate.

## Technologies Used
- Python
- Google Colab
- Pandas
- Scikit-learn
- NLTK / NLP techniques
- Matplotlib
- Seaborn
- PyPDF

## Dataset
The project uses the Kaggle Resume Dataset, containing resumes from different professional categories.

## Methodology
1. Resume PDF extraction.
2. Text cleaning and preprocessing.
3. Skills extraction using keyword matching.
4. Job description creation.
5. TF-IDF vectorization and cosine similarity.
6. Required skills matching.
7. Candidate scoring and ranking.
8. Results visualization and export.

## Scoring Method
The final candidate score combines:

- Skill Match Score: 60%
- Resume Similarity Score: 40%

**Final Score = (0.60 × Skill Match Score) + (0.40 × Similarity Score)**

## Project Results
The system processed 2,483 resumes for a Junior Data Analyst position.

The highest-ranked candidate achieved:
- Skill Match Score: 66.67%
- Resume Similarity Score: 17.94%
- Final Score: 47.18%

The project also generates candidate rankings, missing skills analysis, and visualizations.

## Repository Structure
```text
FUTURE_ML_03/
├── notebooks/
├── models/
├── results/
├── docs/
└── README.md
```

## How to Run
1. Open the notebook in the `notebooks` folder.
2. Upload or provide the resume dataset in Google Colab.
3. Install the required Python libraries.
4. Run the notebook cells in order.
5. Review the candidate rankings and generated results.

## Limitations and Ethical Considerations
The system uses keyword matching and TF-IDF similarity, which may not fully understand the meaning or context of a resume.

The scores are experimental and should support, not replace, human recruitment decisions. All candidates should receive fair and human-reviewed consideration.

## Author
Chuleza Dotye

## Programme
Future Interns – Machine Learning Internship 2026
