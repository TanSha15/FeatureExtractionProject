
# Feature Extraction Project

## Overview
This project focuses on extracting useful features from anime titles using Python and Pandas. It extracts episode counts, airing periods, and total airing duration from the original dataset to create a structured dataset for further analysis.

## Objectives
- Extract episode counts from anime titles.
- Extract airing periods from title strings.
- Calculate the total airing duration in months.
- Identify the highest-scored anime.
- Find the anime with the maximum number of episodes.
- Transform unstructured text into structured features.

## Technologies Used
- Python
- Pandas
- Datetime
- python-dateutil
- Google Colab

## Dataset
The project uses an `anime.csv` dataset containing anime rankings, titles, and scores.

Some useful information, such as episode counts and airing periods, is embedded within the `Title` column. The project extracts this information and stores it in separate columns.

## Project Workflow

### 1. Load the Dataset
Load the CSV file into a Pandas DataFrame for processing.

### 2. Extract Episode Counts
A custom function extracts the episode count from the text enclosed in parentheses.

Example:
- Original title: `Fullmetal Alchemist: BrotherhoodTV (64 eps)...`
- Extracted episodes: `64`

The extracted values are stored in the `Episodes` column.

### 3. Extract Airing Periods
The `extract_timestamp()` function extracts the airing period from each anime title.

Example:
- Extracted period: `Apr 2009 - Jul 2010`

The results are stored in the `TimeStamp` column.

### 4. Calculate Airing Duration
The `calculate_total_months()` function uses Python's `datetime` module and `relativedelta` to calculate the number of months between the start and end dates, including both endpoint months.

The results are stored in the `Months` column.

### 5. Analyze the Dataset
Pandas filtering operations are used to identify the anime with the highest score and the anime with the maximum number of episodes.

## 📊 Results

The final DataFrame contains the following columns:

| Column | Description |
|---|---|
| `Rank` | Anime ranking |
| `Title` | Original anime title |
| `Score` | Anime score |
| `Episodes` | Extracted episode count |
| `TimeStamp` | Extracted airing period |
| `Months` | Calculated airing duration |

### Sample Findings
- **Highest-scored anime:** Fullmetal Alchemist: Brotherhood
- **Score:** 9.10
- **Anime with the most episodes:** Gintama
- **Episode count:** 201
- **Airing period:** April 2006 – March 2010
- **Calculated duration:** 48 months

*Results are based on the dataset used in this project.*

## How to Run the Project

### Google Colab
Open the notebook directly:

[Open in Google Colab](https://colab.research.google.com/github/TanSha15/FeatureExtractionProject/blob/main/Feature_Extraction_Project.ipynb)

1. Open the notebook.
2. Upload `anime.csv` to the Colab environment.
3. Run the notebook cells sequentially.
4. Review the extracted features and results.

### Run Locally

**1. Clone the repository**
```bash
git clone https://github.com/TanSha15/FeatureExtractionProject.git
cd FeatureExtractionProject
```

**2. Install dependencies**
```bash
pip install pandas python-dateutil jupyter
```

**3. Place the dataset**

Place `anime.csv` in the project directory.

**4. Launch Jupyter Notebook**
```bash
jupyter notebook
```

Open `Feature_Extraction_Project.ipynb` and run the cells.

## Key Learnings
- Feature extraction from unstructured text.
- Data manipulation using Pandas.
- Creating new DataFrame columns.
- Date parsing and duration calculations.
- Applying custom functions to dataset columns.
- Filtering and analyzing structured data.

## Future Improvements
- Use regular expressions for more reliable feature extraction.
- Handle missing and invalid values.
- Improve parsing for inconsistent anime title formats.
- Add visualizations for scores, episode counts, and airing durations.
- Explore relationships between airing duration and anime scores.

## Author
**Tanish Sharma**

GitHub: [TanSha15](https://github.com/TanSha15)

---

⭐ If you find this project useful, consider starring the repository.
