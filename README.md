Here's a professional `README.md` file in **English** for your Titanic data preprocessing script, ready for GitHub:

---

# 🧼 Titanic Data Cleaning Script

This project contains a Python script for preprocessing the original Titanic dataset (`titanic_original.csv`). The goal is to clean and prepare the data for further analysis or machine learning tasks.

---

## 📄 Dataset

* **Input file**: `titanic_original.csv`
* **Output file**: `titanic_cleaned.xlsx` (cleaned version saved in Excel format)

---

## 🧹 Cleaning Steps

1. **Drop Unnecessary Columns**
   The following columns were removed as they contain many missing values or are not relevant for modeling:

   * `cabin`
   * `boat`
   * `body`
   * `home.dest`

2. **Handle Missing Values in Age**

   * Missing values in the `age` column were filled using the **mean age**.
   * All age values were **rounded to the nearest integer**.

3. **Fix Missing Embarked Values**

   * Missing values in the `embarked` column were filled with `'S'`, the most frequent port of embarkation.

4. **Correct Fare Values**

   * Zero or negative `fare` values were replaced with the **mean fare** of positive fares only.
   * Negative fare values were clamped to `0`.

5. **Remove Duplicates**

   * Duplicate records were identified and removed from the dataset.

---

## 💾 Output

* Cleaned dataset saved as: `titanic_cleaned.xlsx`
* Format: Excel (uses `openpyxl` engine)

---

## ▶️ How to Use

### 1. Install Dependencies

```bash
pip install pandas openpyxl
```

### 2. Run the Script

Ensure the `titanic_original.csv` file is in the same directory, then run:

```bash
python titanic_cleaning.py
```

After execution, `titanic_cleaned.xlsx` will be generated in the same directory.

---

## 📌 Notes

* The script is designed to be a **lightweight and simple preprocessor** for Titanic data.
* It’s easily extensible for further cleaning or feature engineering.

---

