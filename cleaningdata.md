Cleaning table "dailyactivity":

- Checked how many users there are:

```
SELECT DISTINCT(id) 
FROM dailyactivity

```

- Checked for duplicate entries:

```
SELECT id, activity_date, COUNT(activity_date)
FROM dailyactivity
GROUP BY id, activity_date
HAVING COUNT(activity_date) > 1

```
