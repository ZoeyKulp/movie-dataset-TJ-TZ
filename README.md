# פרויקט חלק 1: איסוף נתוני סרטים

**שמות חברי הצוות:**  
זוהר קולפ: 322435918  
רוני פחימה: 212009260  

**קבוצת סרטים:** סרטים שכותרתם מתחילה באותיות TJ עד TZ

**קישור לגיט:**  
<!-- הכניסו כאן את הקישור ל-GitHub -->

---

## קבצים בפרויקט

| קובץ | תיאור |
|------|--------|
| `notebook_final1.ipynb` | קוד Python המלא לאיסוף הנתונים |
| `dataset.csv` | סט הנתונים הסופי |
| `report.pdf` | דוח על תהליך האיסוף |
| `README.md` | קובץ זה |

---

## הוראות הרצה

### דרישות מקדימות

```
pip install requests beautifulsoup4 pandas numpy
```

### הכנה לפני הרצה

יש להוריד את קבצי IMDb מהאתר: https://datasets.imdbws.com/  
ולשמור באותה תיקייה של המחברת:
- `title.basics.tsv.gz`
- `title.ratings.tsv.gz`
- `title.principals.tsv.gz`

### שלבי הרצה

1. פתחו את `notebook_final1.ipynb` ב-Jupyter
2. הריצו את התאים לפי הסדר מלמעלה למטה
3. תא הויקיפדיה ירוץ על כל הסרטים
4. בסיום יישמר קובץ `dataset.csv` בתיקייה הנוכחית

---

## תיאור קצר של שיטת האיסוף

הנתונים נאספו משלושה מקורות:
- **IMDb** - סינון סרטים לפי titleType, שנים, משך זמן וכותרת. מיזוג עם ratings ו-principals לקבלת דירוגים ושחקנים.
- **Wikipedia** - Web scraping לחילוץ Language, Country, budget ו-BoxOffice מה-infobox של כל סרט.
- **OMDb API** - שליפת plot לפי מזהה tconst.

נבחרו 5,000 הסרטים עם הכי הרבה קולות (numVotes) להבטחת סרטים מתועדים היטב.
