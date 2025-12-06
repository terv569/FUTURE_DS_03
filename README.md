#Student Satisfaction Survey Analysis

This repository contains code and assets for analyzing a Student Satisfaction Survey and generating a clear visual report using:

Bar charts (e.g., average rating per question, top-rated courses)

Pie chart (overall rating distribution)

Word cloud (most frequent words from comments)

The goal of this project is to make it easy to explore survey results, identify strengths and weaknesses, and communicate findings visually.

##📁 Project Structure
.
├── Student_Satisfaction_Survey.csv   # Raw survey data
├── survey_analysis.ipynb             # Main analysis notebook / script
├── README.md                         # Project documentation


You may rename the files, but ensure that file paths remain consistent with the code.

📊 Dataset Description

The analysis assumes a CSV file with columns similar to:

Questions – Text of the survey question

Course Name – Name of the course or event

Weightage1 … Weightage5 – One-hot encoded rating columns (1–5)

Comment (optional) – Free-text response

If the dataset does not include a Rating or Comment column:

Rating is derived automatically from the Weightage* columns

Synthetic comments are generated for demonstration purposes

Column names can be customized inside the script to match your dataset.

⚙️ What the Code Does

The workflow includes:

1. Setup & Imports

Installs and imports pandas, numpy, matplotlib, seaborn, and wordcloud

Sets a clean default plotting style

2. Load the Data

Reads Student_Satisfaction_Survey.csv

Cleans column names (removes leading/trailing spaces)

3. Derive Rating & Comment (if missing)

Detects columns starting with Weightage

Creates a Rating column (1–5)

Generates synthetic comments if the dataset has none

4. Average Rating by Question (Bar Chart)

Groups by Questions

Plots a horizontal bar chart showing average rating per question

5. Overall Rating Distribution (Pie Chart)

Computes frequency of each rating

Displays a pie chart summarizing overall satisfaction levels

6. Top Courses / Events by Rating

Groups by Course Name

Plots top 10 courses/events based on average rating

7. Word Cloud of Comments

Combines all comments into one text block

Generates a word cloud showing the most common words used

8. Summary Metrics

Overall average rating

Best-rated question(s)

Lowest-rated question(s)

These metrics are printed for quick interpretation.

🚀 How to Run This in Google Colab

Open Google Colab

Create a new notebook

Upload Student_Satisfaction_Survey.csv

Copy code from survey_analysis.ipynb into Colab

Update the file path if necessary:

file_path = "Student_Satisfaction_Survey.csv"


Run the notebook — all charts will appear inline.

📦 Requirements

Python 3.8+

Install dependencies (if running locally):
pip install pandas numpy matplotlib seaborn wordcloud

🔧 Customization

You can adapt the workflow to your needs by:

Editing column names inside the script

Adding analyses by instructor, department, or semester

Saving charts for presentations:

plt.savefig("average_rating_by_question.png", dpi=300, bbox_inches="tight")


Exporting grouped summaries to CSV for reporting

Improving comment analysis using NLP techniques (optional)

📄 License

Specify your preferred license here, e.g.:

MIT License

MIT License
Or any other license appropriate for your project.
