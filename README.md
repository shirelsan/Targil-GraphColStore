# GitHub Archive Analysis - GraphColStore

## חברי הקבוצה
* שיראל סננס (ת.ז:322328824)
* תהילה בן דוד (ת.ז: 314692195)

## הוראות הפעלה
כדי להריץ את הפרויקט במלואו, יש להריץ את המחברות הבאות לפי הסדר:
1. `01_explore.ipynb` - תחקור נתונים גולמיים בעזרת שאילתות JSONiq.
2. `02_to_parquet.ipynb` - שיטוח הנתונים והמרתם למאגר עמודות (Parquet).
3. `03_analysis.ipynb` - חישובים, אגרגציות ויצירת גרפים.

## שורות תוצאה נדרשות
* **משימה A1 (מספר אירועים כולל):** 28,506,909
<<<<<<< HEAD
* **משימה A2 (תדירות סוגי אירועים):**
```text
The query output 14 items, which is too many to display. Displaying the first 10 items:
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

```
* **משימה A3 (חמשת ה-PushEvents הראשונים):**
```text
{
  "actor_login": "davidcarlsonberg",
  "repo_name": "PubWlkr/PubWlkr",
  "created_at": "2015-02-20T01:00:01Z"
}
{
  "actor_login": "loomchild",
  "repo_name": "loomchild/reload",
  "created_at": "2015-02-20T01:00:01Z"
}
{
  "actor_login": "lsqshr",
  "repo_name": "lsqshr/nipype",
  "created_at": "2015-02-20T01:00:01Z"
}
{
  "actor_login": "PhancyCat",
  "repo_name": "PhancyCat/HTMLClock",
  "created_at": "2015-02-20T01:00:01Z"
}
{
  "actor_login": "saramartinez",
  "repo_name": "saramartinez/tv-or-not-tv",
  "created_at": "2015-02-20T01:00:01Z"
}
```

* **משימה A4 (מספר רשומות עם commits):** 14,173,075 רשומות.
  * *השוואה ל-A2:* מתוך 14,271,557 אירועי PushEvent סך הכל, 14,173,075 מכילים קומיטים שאינם ריקים. ישנם 98,482 אירועי Push ללא קומיטים (כ-0.7% מכלל אירועי ה-Push).
* **משימה A5 (טווח חותמות הזמן):**
```json
{
  "IssueCommentEvent": {
    "earliest": "2015-01-01T00:00:06Z",
    "latest": "2015-02-28T23:59:59Z"
  },
  "CreateEvent": {
    "earliest": "2015-01-01T00:00:01Z",
    "latest": "2015-02-28T23:59:59Z"
  },
  "WatchEvent": {
    "earliest": "2015-01-01T00:00:18Z",
    "latest": "2015-02-28T23:59:58Z"
  },
  "IssuesEvent": {
    "earliest": "2015-01-01T00:00:30Z",
    "latest": "2015-02-28T23:59:59Z"
  },
  "PublicEvent": {
    "earliest": "2015-01-01T00:09:13Z",
    "latest": "2015-02-28T23:57:28Z"
  },
  "PullRequestReviewCommentEvent": {
    "earliest": "2015-01-01T00:00:08Z",
    "latest": "2015-02-28T23:59:26Z"
  },
  "ForkEvent": {
    "earliest": "2015-01-01T00:00:16Z",
    "latest": "2015-02-28T23:59:34Z"
  },
  "ReleaseEvent": {
    "earliest": "2015-01-01T00:02:19Z",
    "latest": "2015-02-28T23:59:06Z"
  },
  "GollumEvent": {
    "earliest": "2015-01-01T00:01:10Z",
    "latest": "2015-02-28T23:59:44Z"
  },
  "DeleteEvent": {
    "earliest": "2015-01-01T00:00:30Z",
    "latest": "2015-02-28T23:59:46Z"
  },
  "MemberEvent": {
    "earliest": "2015-01-01T00:04:11Z",
    "latest": "2015-02-28T23:58:56Z"
  },
  "PullRequestEvent": {
    "earliest": "2015-01-01T00:00:11Z",
    "latest": "2015-02-28T23:59:58Z"
  },
  "CommitCommentEvent": {
    "earliest": "2015-01-01T00:00:55Z",
    "latest": "2015-02-28T23:58:56Z"
  },
  "PushEvent": {
    "earliest": "2015-01-01T00:00:00Z",
    "latest": "2015-02-28T23:59:59Z"
  }
}
```


* **משימה B4 (אימות פלט Parquet):** * גודל קובץ מקורי (`.json.gz`): [להשלים] MB
  * גודל קובץ מומר (`events.parquet`): [להשלים] MB
  * יחס המרה: [להשלים]
  * שטח זיכרון בשימוש ה-DataFrame: [להשלים] MB
=======
* **משימה A2 (תדירות סוגי אירועים):** [להשלים פלט של השאילתה]
* **משימה A4 (מספר רשומות עם commits):** [להשלים פלט]
* **משימה B4 (אימות פלט Parquet):**
  * גודל קובץ מקורי (`.json.gz`): 10180.67 MB
  * גודל קובץ מומר (`events.parquet`): 746.15 MB
  * יחס המרה: 0.073
  * שטח זיכרון בשימוש ה-DataFrame: 0.06 MB
>>>>>>> 5d61aa9 (stage2)

---

## טבלאות תזמון

### חלק א' - תחקור מידע (JSONiq)
| Query | Wall-clock time (s) |
| :--- | :--- |
| A1 - total event count | 28m 50.0s (1730s) |
| A2 - event type frequencies | 135m 30.0s (8130s) |
| A3 - first 5 PushEvents | 3.9s |
| A4 - non-empty commits count | 65m 42.7s (3942.7s) |
| A5 - timestamp range | 69m 15.6s (4155.6s) |

### חלק ב' - המרה לעמודות (Parquet)
| Step | Wall-clock time (s) | Throughput (rows/s) |
| :--- | :--- | :--- |
| B3 - full JSON → Parquet conversion | 6751.00 | 4222.62 |
| B4 - reload Parquet into DataFrame | 63.10 | N/A |

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
