**Cleaning table "dailyactivity":**

**- Checked how many users there are:**

```
SELECT DISTINCT(id) 
FROM dailyactivity
```
Number of Users = 35

**- Checked for duplicate entries:**

```
SELECT id, activity_date, COUNT(activity_date)
FROM dailyactivity
GROUP BY id, activity_date
HAVING COUNT(activity_date) > 1
```
No duplicates found

**- Checked for any null values:**

```
SELECT *
FROM dailyactivity
WHERE id IS NULL
```
```
SELECT *
FROM dailyactivity
WHERE activity_date IS NULL
```
No null values found
