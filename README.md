# 🚢 Titanic Dataset - Data Cleaning & Preprocessing

This project demonstrates how to clean and preprocess raw data from the Titanic dataset using Python tools like **Pandas**, **NumPy**, **Matplotlib**, **Seaborn**, and **Scikit-learn**.

---

##  Objective

To prepare the Titanic dataset for machine learning by:
- Handling missing data
- Encoding categorical features
- Normalizing numerical features
- Detecting and removing outliers

---

##  Tools & Libraries Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

---

## Dataset

The dataset used is the [Titanic dataset](https://www.kaggle.com/competitions/titanic/data), which includes passenger information used to predict survival.

> **File:** `Titanic-Dataset.csv`

---

##  Steps Performed

### 1. **Data Loading & Exploration**
- Loaded dataset using `pandas.read_csv()`
- Displayed basic info: shape, column types, missing values

### 2. **Handling Missing Values**
- Filled missing `Age` with **mean**
- Filled missing `Embarked` with **mode**
- Dropped `Cabin` column (too many missing values)

### 3. **Encoding Categorical Features**
- Encoded `Sex` using **LabelEncoder**
- Encoded `Embarked` using **One-Hot Encoding**

### 4. **Normalizing Numerical Features**
- Standardized `Age` and `Fare` using **StandardScaler**

### 5. **Outlier Detection & Removal**
- Used **boxplots** to visualize outliers in `Age` and `Fare`
- Removed outliers using **IQR (Interquartile Range) method**

### 6. **Saving Cleaned Data**
- Final cleaned dataset saved as: `Cleaned_Titanic_Dataset.csv`

---

##  Output

<img width="681" alt="image" src="https://github.com/user-attachments/assets/9aff4add-5a8c-4853-ad1f-5d4245e6127d" />
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 891 entries, 0 to 890
Data columns (total 12 columns):
 #   Column       Non-Null Count  Dtype  
---  ------       --------------  -----  
 0   PassengerId  891 non-null    int64  
 1   Survived     891 non-null    int64  
 2   Pclass       891 non-null    int64  
 3   Name         891 non-null    object 
 4   Sex          891 non-null    object 
 5   Age          714 non-null    float64
 6   SibSp        891 non-null    int64  
 7   Parch        891 non-null    int64  
 8   Ticket       891 non-null    object 
 9   Fare         891 non-null    float64
 10  Cabin        204 non-null    object 
 11  Embarked     889 non-null    object 
dtypes: float64(2), int64(5), object(5)
memory usage: 83.7+ KB
None

PassengerId    Survived      Pclass         Age       SibSp  \
count   891.000000  891.000000  891.000000  714.000000  891.000000   
mean    446.000000    0.383838    2.308642   29.699118    0.523008   
std     257.353842    0.486592    0.836071   14.526497    1.102743   
min       1.000000    0.000000    1.000000    0.420000    0.000000   
25%     223.500000    0.000000    2.000000   20.125000    0.000000   
50%     446.000000    0.000000    3.000000   28.000000    0.000000   
75%     668.500000    1.000000    3.000000   38.000000    1.000000   
max     891.000000    1.000000    3.000000   80.000000    8.000000   

            Parch        Fare  
count  891.000000  891.000000  
mean     0.381594   32.204208  
std      0.806057   49.693429  
min      0.000000    0.000000  
25%      0.000000    7.910400  
50%      0.000000   14.454200  
75%      0.000000   31.000000  
max      6.000000  512.329200  
PassengerId      0
Survived         0
Pclass           0
Name             0
Sex              0
Age            177
SibSp            0
Parch            0
Ticket           0
Fare             0
Cabin          687
Embarked         2
dtype: int64
<img width="700" alt="image" src="https://github.com/user-attachments/assets/8f591520-e755-4442-8886-b2973b853536" />
<img width="700" alt="image" src="https://github.com/user-attachments/assets/cc768e54-ece4-4d25-8a5e-3accc592b05f" />


