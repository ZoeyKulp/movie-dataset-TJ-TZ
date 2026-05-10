# Final Project-Part 1: Movie Data Collection

**Team Members:**  
Zohar Kulp: 322435918  
Roni Fahima: 212009260  

**Movie Group:** Movies whose titles start with the letters TJ to TZ

**GitHub Link:**  
<!-- Insert your GitHub link here -->

---

## Project Files

| File | Description |
|------|-------------|
| `notebook_final1.ipynb` | Full Python code for data collection |
| `dataset.csv` | Final dataset |
| `report.pdf` | Report on the collection process |
| `README.md` | This file |

---

## How to Run

### Prerequisites

```
pip install requests beautifulsoup4 pandas numpy
```

### Setup

Download the IMDb files from: https://datasets.imdbws.com/  
Save the following files in the same folder as the notebook:
- `title.basics.tsv.gz`
- `title.ratings.tsv.gz`
- `title.principals.tsv.gz`

### Steps

1. Open `notebook_final1.ipynb` in Jupyter
2. Run all cells from top to bottom
3. The Wikipedia cell runs on all movies - **takes several hours**
4. When done, `dataset.csv` will be saved in the current folder

---

## Data Collection Overview

Data was collected from three sources:

- **IMDb** - Filtered by titleType, year, runtime and title prefix (TJ–TZ). Merged with ratings and principals to get scores and actors.

- **Wikipedia** - Web scraping to extract Language, Country, budget and BoxOffice from each film's infobox. The scraper handles special characters in titles, disambiguation pages, and verifies each page is actually a film page.

- **OMDb API** - Plot fetched by tconst identifier. Chosen for its clean and structured summaries.

The 5,000 films with the most votes (numVotes) were selected to ensure well-documented films.
