# Titanic Dataset Cleaning (Internship Task 5)

## 📌 Task Overview
This project is part of **Internship Task 5**, focused on performing **data cleaning using Python (Pandas & NumPy)** on the Titanic dataset.

The goal is to load the dataset, inspect it, handle missing values, remove duplicates, perform datatype conversions, create new features, and export the cleaned dataset.

---

## 🛠 Tools & Technologies Used
- Python
- Jupyter Notebook
- Pandas
- NumPy

---

## 📂 Dataset
- Titanic Dataset (`tested.csv`)

---

## ✅ Steps Performed
1. Loaded dataset using `pandas.read_csv()`
2. Checked dataset size using `.shape`
3. Viewed first records using `.head()`
4. Checked datatypes and missing values using `.info()`
5. Found missing values using `isnull().sum()`
6. Removed duplicate rows using `drop_duplicates()`
7. Filled missing values:
   - `Age` filled with median
   - `Fare` filled with median
   - `Embarked` filled with mode
   - `Cabin` filled with "Unknown"
8. Converted datatypes:
   - Converted `Sex` to numeric values (male=0, female=1)
   - Converted `Embarked` to categorical datatype
9. Feature engineering (new columns):
   - `FamilySize` = `SibSp + Parch + 1`
   - `AgeGroup` created by binning Age values
10. Exported cleaned dataset as `cleaned_data.csv`

---

## 📌 Output Files
- `Task5_Cleaning.ipynb` → Jupyter Notebook containing full code + explanations
- `cleaned_data.csv` → Final cleaned dataset

---

## 🚀 How to Run
1. Open Jupyter Notebook
2. Run the notebook `Task5_Cleaning.ipynb`
3. Ensure dataset path is correct:
   ```python
   df = pd.read_csv(r"D:\Downloads\tested.csv")
