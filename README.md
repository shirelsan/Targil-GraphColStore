# GitHub Archive Analysis - GraphColStore

## חברי הקבוצה
* שיראל סננס (ת.ז:322328824)
* תהילה בן דוד (ת.ז: [להשלים])

## הוראות הפעלה
כדי להריץ את הפרויקט במלואו, יש להריץ את המחברות הבאות לפי הסדר בסביבת WSL:
1. `01_explore.ipynb` - תחקור נתונים גולמיים בעזרת שאילתות JSONiq.
2. `02_to_parquet.ipynb` - שיטוח הנתונים והמרתם למאגר עמודות (Parquet).
3. `03_analysis.ipynb` - חישובים, אגרגציות ויצירת גרפים.

## שורות תוצאה נדרשות
* **משימה A1 (מספר אירועים כולל):** 28,506,909
* **משימה A2 (תדירות סוגי אירועים):** :
* The query output 14 items, which is too many to display. Displaying the first 10 items:
{
  "type": "PushEvent",
  "count": 14271557
}
{
  "type": "CreateEvent",
  "count": 3328235
}
{
  "type": "IssueCommentEvent",
  "count": 2782424
}
{
  "type": "WatchEvent",
  "count": 2552211
}
{
  "type": "IssuesEvent",
  "count": 1463914
}
{
  "type": "PullRequestEvent",
  "count": 1393766
}
{
  "type": "ForkEvent",
  "count": 971107
}
{
  "type": "DeleteEvent",
  "count": 548218
}
{
  "type": "PullRequestReviewCommentEvent",
  "count": 441408
}
{
  "type": "GollumEvent",
  "count": 294042
}
הערה: הפלט קוצץ ל-10 התוצאות הראשונות על ידי מנגנון ברירת המחדל של RumbleDB.

* **משימה A4 (מספר רשומות עם commits):** [להשלים פלט]
* **משימה B4 (אימות פלט Parquet):** * גודל קובץ מקורי (`.json.gz`): [להשלים] MB
  * גודל קובץ מומר (`events.parquet`): [להשלים] MB
  * יחס המרה: [להשלים]
  * שטח זיכרון בשימוש ה-DataFrame: [להשלים] MB

---

## טבלאות תזמון

### חלק א' - תחקור מידע (JSONiq)
| Query | Wall-clock time (s) |
| :--- | :--- |
| A1 - total event count | 28m 50.0s (1730s) |
| A2 - event type frequencies | 135m 30.0s (8130s) |
| A3 - first 5 PushEvents | [להשלים] |
| A4 - non-empty commits count | [להשלים] |
| A5 - timestamp range | [להשלים] |

### חלק ב' - המרה לעמודות (Parquet)
| Step | Wall-clock time (s) | Throughput (rows/s) |
| :--- | :--- | :--- |
| B3 - full JSON → Parquet conversion | [להשלים] | [להשלים] |
| B4 - reload Parquet into DataFrame | [להשלים] | N/A |

### חלק ג' - חישובים (Pandas)
| Step | Wall-clock time (s) |
| :--- | :--- |
| Parquet load + timestamp parse | [להשלים] |
| C1 - top users by event count | [להשלים] |
| C1 - top users by commit count | [להשלים] |
| C2 - top repos by event count | [להשלים] |
| C2 - top repos by commit count | [להשלים] |
| C3 - hourly aggregation | [להשלים] |
| C3 - day-of-week aggregation | [להשלים] |
