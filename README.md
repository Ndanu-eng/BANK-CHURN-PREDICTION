---
# FOR TEAM MEMBERS

## Overview
This project uses a  Bank churn Kaggle dataset stored in **Google Drive** for easy access by all team members. We will work collaboratively using **Google Colab**, ensuring everyone can load and analyze the dataset without downloading it locally.

# HOW TO USE THE DATASET AS A TEAM
 Open Google Colab from Chrome browser sign up and login with your gmail.

 ## Option 1
 Open a google Colab NewNotebook then Run:
 
 ```sh
 import pandas as pd

# Correct direct file link (Replace FILE_ID with your actual file ID)
file_id = "1-6FhvYRRgceTptrIMfgvaXkq-QKw8dwf"
file_url = f"https://drive.google.com/uc?id={file_id}"

# Load the dataset
df = pd.read_csv(file_url)

# Describe the data
df.describe()
```

# Option 2
Click the BankChurn folder link below then open shared inside Google drive to make sure you can access it.

```sh
https://drive.google.com/drive/folders/1kyYj-jEOInyj-Kes1PoSz9AWVXCCSYmQ?usp=sharing
```
 Open a google Colab NewNotebook then Run
 
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

# Describe the data
df.describe()
```
 ---
 
# BANK-CHURN-PREDICTION






