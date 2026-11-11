# HR Recruitment Screening Automation

An AI-powered recruitment screening workflow built using **n8n, Google Gemini, Google Drive, Google Sheets, Google Docs, and Gmail**.

This automation helps streamline the initial candidate screening process by collecting applications, extracting information from resumes, comparing candidate profiles with job requirements, generating AI-based scores, and categorizing applicants.

## Project Overview

The HR Recruitment Screening Automation is designed to reduce repetitive manual work during the initial recruitment stage.

Candidates submit their details and resume through an application form. The workflow extracts relevant information from the uploaded PDF, analyzes the candidate's profile using Google Gemini, compares it with the job description, and assigns a score between 1 and 10.

Based on the score, candidates are categorized as:

- **Shortlisted:** Score 7 or above
- **Under Review:** Score 5–6
- **Rejected:** Score below 5

## Workflow Architecture

1. **Candidate Application Form**
   - Collects first name, last name, email, and resume.
   - Accepts resume files in PDF format.
   - Includes a hidden job code field.

2. **Resume Upload**
   - Uploads candidate resumes to Google Drive.
   - Stores uploaded files in the designated Resumes folder.

3. **Resume Text Extraction**
   - Extracts text from the uploaded PDF resume.

4. **AI Information Extraction**
   - Uses Google Gemini to extract personal information.
   - Identifies professional details, education, experience, and technical skills.

5. **Candidate Profile Summarization**
   - Combines extracted information.
   - Generates a structured candidate summary.

6. **Job Description Retrieval**
   - Retrieves the job description from Google Docs.

7. **AI Candidate Evaluation**
   - Uses Google Gemini to compare the candidate profile against the job description.
   - Generates a score from 1 to 10.
   - Provides an assessment explaining the evaluation.

8. **Candidate Classification**
   - Uses a Python Code node to categorize candidates based on their scores.
   - Routes candidates into Shortlisted, Under Review, or Rejected categories.

9. **Google Sheets Integration**
   - Stores candidate information and screening results in Google Sheets.
   - Records details such as applicant name, email, experience, skills, education, score, and assessment.

10. **Email Notifications**
    - Sends email notifications based on the screening outcome.

## Technologies Used

- **n8n** – Workflow automation
- **Google Gemini** – AI-powered resume analysis and candidate evaluation
- **Google Drive** – Resume storage
- **Google Docs** – Job description retrieval
- **Google Sheets** – Candidate data management
- **Gmail** – Automated email notifications
- **Python** – Candidate score classification

## Candidate Scoring Logic

| AI Score | Classification |
|---|---|
| 7–10 | Shortlisted |
| 5–6 | Under Review |
| Below 5 | Rejected |

## Key Features

- Automated candidate application processing
- PDF resume text extraction
- AI-based information extraction
- Candidate profile summarization
- Job description matching
- AI-generated candidate scoring
- Rule-based candidate classification
- Google Sheets integration
- Automated email notifications

## Project Objective

The objective of this project is to demonstrate how AI and workflow automation can simplify repetitive recruitment tasks, organize candidate information, and support recruiters during the initial screening process.

## Important Notes

This project is a prototype. The exported workflow may require configuration of Google credentials, Gemini API access, Google Drive folders, Google Docs, Google Sheets, and Gmail before execution.

The workflow should be tested and validated before production use. AI-generated scores are preliminary assessments and should not be used as the sole basis for hiring decisions. Human review is necessary for fair and reliable recruitment decisions.

---

**Built with n8n and Google Gemini.**
