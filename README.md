# Student Quiz Performance Analysis Tool
## Overview
This project is a comprehensive data processing and analysis tool that extracts, processes, and analyzes quiz performance data to generate meaningful insights. The tool normalizes scores, identifies performance personas, highlights strengths and weaknesses, and provides recommendations to enhance learning outcomes.

## Setup Instructions
### Prerequisites
Python 3.7 or later.

Libraries: pandas, requests, matplotlib, seaborn.
### Installation
Clone this repository or download the ZIP file.

Install dependencies:
> ```pip install pandas requests matplotlib seaborn```

Ensure your JSON data URL is updated in the script (url variable).

## Usage Instructions
Run the script to fetch and process the JSON data into a CSV file,
The script automatically:
1. Computes time taken for quizzes.
2. Normalizes scores.
3. Generates detailed personas.
4. Student Personas based on various performance metrics.
5. Strengths and Weaknesses, highlighting improvement areas.
6. Visualizations for accuracy distribution and topic performance trends are generated.


## Approach Description
### Data Fetching:
Fetch quiz data from the provided JSON API. Parse metadata like quiz titles and topics to enrich the dataset.

### Data Normalization:
Calculate normalized scores by dividing final_score by the total number of questions. Normalize varying quiz lengths to provide a fair comparison.

### Persona Creation:
Combine metrics like accuracy, speed, and time taken to assign personas:

### Insight Generation:
Highlight top strengths (e.g., high accuracy, fast thinking) and weaknesses (e.g., poor time management, high penalties for negative scores).

### Visualization:
Use matplotlib and seaborn to create graphs for data exploration and trends.

## Extra
I'm unsure if it was a mistake or done intentionally to test us.

The quiz endpoint ```https://jsonkeeper.com/b/LLQT``` contains several questions, but the Historical Quiz Data ```https://api.jsonserve.com/XgAgFJ``` doesn't include these questions in the response map.

Additionally, the difficulty field is null across the response, so I can't use it to generate any meaningful insights.

I haven't created a model yet because the dataset is sparse and many feature values are missing. Instead, I relied on basic statistics to complete the task. However, if a model is needed, one could use a decision tree or K-means clustering, though both methods would require the missing features.

Whatever the reason, I think it was a clever move to filter applications.


## Bonus
I appreciate the opportunity to explore the use of AI for enhancing student outcomes. This assignment has inspired additional ideas that I can either collaborate with you on if selected or develop independently for my own project.
