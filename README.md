# 🎬 Advanced Coding Project

---

## 📂 How to Load a CSV File in MySQL

### Step 1: Create a New Database
Open **MySQL Workbench**, create a new database, and name it.

<img width="441" alt="Screenshot 2025-02-12 at 7 27 06 pm" src="https://github.com/user-attachments/assets/8730cb14-8eb0-407d-9ff4-f2ea278ba03e" />

### Step 2: Use the Table Data Import Wizard
Right click on the database and select **"Table Data Import Wizard"**.

<img width="565" alt="Screenshot 2025-02-12 at 7 29 12 pm" src="https://github.com/user-attachments/assets/3287e849-1f07-4ce7-ade8-b029318c391a" />


### Step 3: Select Your CSV File
Click **"Browse"**, select the CSV file, and proceed with the import process.

<img width="783" alt="Screenshot 2025-02-12 at 7 29 40 pm" src="https://github.com/user-attachments/assets/044a871b-7e7c-4907-afe4-6a074ef0b9b8" />


---
## 📊 SQL Queries for Data Analysis

## -- Display All Data

```sql
SELECT * FROM Project.cleaned_file;
```
<img width="1250" alt="Screenshot 2025-02-12 at 7 32 20 pm" src="https://github.com/user-attachments/assets/00f5c7af-7c04-46e1-a869-1b03b61e0da4" />


## 1- Display All Theaters with Their Ratings

```sql
SELECT name, rating FROM cleaned_file;
```
<img width="1250" alt="Screenshot 2025-02-12 at 9 14 57 pm" src="https://github.com/user-attachments/assets/dd4d680c-1341-4b10-9181-899edee7080f" />


## 2- Display All Genres

```sql
SELECT DISTINCT genre FROM cleaned_file;
```
<img width="1250" alt="Screenshot 2025-02-12 at 9 13 05 pm" src="https://github.com/user-attachments/assets/ae780929-3f6d-447d-8985-f598570abbb0" />


## 3- Display All Theaters in Al Jubail

```sql
SELECT name FROM cleaned_file WHERE location LIKE '%Al Jubail%';
```
<img width="1250" alt="Screenshot 2025-02-12 at 9 14 19 pm" src="https://github.com/user-attachments/assets/c7e291dc-2397-4eb5-b9a2-1bbd233b63f0" />


## 4- Average Rating of All Theaters

```sql
SELECT AVG(rating) AS avg_rating FROM cleaned_file;
```
<img width="1250" alt="Screenshot 2025-02-12 at 9 35 04 pm" src="https://github.com/user-attachments/assets/b3ce02e6-d5f9-49e6-ae9d-8344e0fa40f8" />


## 5- Display Locations with Rating = 5 and More Than 20,000 Reviews

```sql
SELECT name, rating, review_count 
FROM cleaned_file 
WHERE rating = 5 AND review_count > 20000;
```
<img width="1250" alt="Screenshot 2025-02-12 at 9 44 13 pm" src="https://github.com/user-attachments/assets/2b5baa6d-c9b5-4292-a2bd-8f2b7b0a60d3" />



## 6- Display Top 5 Cinemas by Rating

```sql
SELECT * FROM cleaned_file
ORDER BY rating DESC
LIMIT 5;
```
<img width="1250" alt="Screenshot 2025-02-12 at 9 55 36 pm" src="https://github.com/user-attachments/assets/0a30fb05-e26b-4edb-a8e3-8d032b58fcf6" />



## 7- Display Theaters Hosting Movies with Rating 3 or More

```sql
SELECT * FROM cleaned_file 
WHERE genre LIKE '%Movie theater%' AND rating >= 3;
```
<img width="1250" alt="Screenshot 2025-02-12 at 9 58 23 pm" src="https://github.com/user-attachments/assets/bec0b3f1-c2af-4285-a689-05747cc66afb" />


## 8- Display Action Movies Theaters with Rating 4+, Reviews > 15,000


```sql
SELECT name, location 
FROM cleaned_file 
WHERE genre LIKE '%Action%' AND rating >= 4 AND review_count > 15000
ORDER BY review_count;
```
<img width="1250" alt="Screenshot 2025-02-12 at 10 04 49 pm" src="https://github.com/user-attachments/assets/50c5f97e-791c-415c-90e5-3c7affcb8a84" />




## 9- Display All Parks in Riyadh (Sorted by Rating)

```sql
SELECT name, rating, review_count, location
FROM cleaned_file
WHERE genre LIKE '%Park%' AND location LIKE '%Riyadh%'
ORDER BY rating DESC;
```
<img width="1250" alt="Screenshot 2025-02-12 at 10 14 33 pm" src="https://github.com/user-attachments/assets/e7098ec6-2794-4529-915b-eb9633edd618" />


## 10- Average Rating for Locations Grouped by Genre

```sql
SELECT genre, AVG(rating) AS avg_r 
FROM cleaned_file 
GROUP BY genre;
```
<img width="1250" alt="Screenshot 2025-02-12 at 10 26 06 pm" src="https://github.com/user-attachments/assets/146639f6-679c-4f2d-afd9-f33ba1d63398" />

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# 🎉 Thank You 🤍
