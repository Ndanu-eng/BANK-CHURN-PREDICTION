---
# FOR TEAM MEMBERS

## Overview
This project uses a Kaggle dataset stored in **Google Drive** for easy access by all team members. We will work collaboratively using **Google Colab**, ensuring everyone can load and analyze the dataset without downloading it locally.

## Accessing the Dataset from Google Drive
https://drive.google.com/drive/folders/1kyYj-jEOInyj-Kes1PoSz9AWVXCCSYmQ?usp=drive_link

 # Open Google Colab from Chrome browser Signup and  login.Create a new Notebook.
 
 **mount your Google Drive:**
```python
from google.colab import drive
drive.mount('/content/gdrive')
```

 **Set the dataset path:**
```python
csv_path = "/content/gdrive/My Drive/BankChurn/Customer-Churn-Records.csv"
```
 **Load the dataset in Pandas:**
```python
import pandas as pd
df = pd.read_csv(csv_path)

# Display the first 5 rows
df.describe()
```
 ---
 
# BANK-CHURN-PREDICTION-PROJECT





