---
# FOR TEAM MEMBERS

## Overview
This project uses a  Bank churn Kaggle dataset stored in **Google Drive** for easy access by all team members. We will work collaboratively using **Google Colab**, ensuring everyone can load and analyze the dataset without downloading it locally.The dataset folder is to shared through  link if you use option 2.

# HOW TO USE THE DATASET
 Open Google Colab from Chrome browser  sign up and login  then create a new Notebook.

 ## Option 1
 Direct Google Drive File Access (No Mounting Required)
 
 ```sh
 import pandas as pd

# Correct direct file link (Replace FILE_ID with your actual file ID)
file_id = "1-6FhvYRRgceTptrIMfgvaXkq-QKw8dwf"
file_url = f"https://drive.google.com/uc?id={file_id}"

# Load the dataset
df = pd.read_csv(file_url)

# Display first 5 rows
df.describe()
```

# Option 2
Google Drive Mounting (Shared Folder Access)

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





