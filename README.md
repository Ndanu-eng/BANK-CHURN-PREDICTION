**GUIDE FOR TEAM MEMBERS**

**Overview**

This project uses a Bank churn Kaggle dataset stored in **Google Drive** for easy access by all team members. We will work collaboratively using **Google Colab** notebook.

**HOW TO USE THIS GITHUB REPOSITORY AS A TEAM**

Open google colab https://colab.google/

Open a new notebook

Inside the first colab code cell Run:

```
!apt install git

# Change to your working directory
%cd /content

# Clone the shared GitHub repository
!git clone https://github.com/Adamsomondi/BANK-CHURN-PREDICTION.git

# Move into the repo
%cd BANK-CHURN-PREDICTION

# Checks the contents of the repository
!ls -la

# Ensures you are in the correct repository
%cd /content/BANK-CHURN-PREDICTION
```

**HOW TO USE THE DATASET AS A TEAM**

**OPTION 1**

Insert a new second colab code cell then Run:

```
import pandas as pd

# Correct direct file link
file_id = "1-6FhvYRRgceTptrIMfgvaXkq-QKw8dwf"
file_url = f"https://drive.google.com/uc?id={file_id}"# Load the dataset
df = pd.read_csv(file_url)

df
```

**OR**

### Option 2

Click the BankChurn shared folder link below then open shared tab inside Google drive to make sure you can access it.

```
<https://drive.google.com/drive/folders/1kyYj-jEOInyj-Kes1PoSz9AWVXCCSYmQ?usp=sharing>

```

Insert a new second colab code cell then Run:

```python
#It creates a virtual mount point at /content/gdrive/
from google.colab import drive
drive.mount('/content/gdrive')
```

**Set the dataset path:**

```python
csv_path = "/content/gdrive/My Drive/BankChurn/Customer-Churn-Records.csv"

or

csv_path = "/content/gdrive/Shared drives/Shared Folder/BankChurn/Customer-Churn-Records.csv"

note:
Open Google Drive (drive.google.com).
Click on "Shared with me" in the left sidebar.
Find the shared folder you want to add.
Right-click on the folder.
Click "Add shortcut to Drive".
Select "My Drive" or a specific folder.
Click "Add shortcut" to complete.
```

**Load the dataset in Pandas:**

```python
import pandas as pd
df = pd.read_csv(csv_path)

# Describe the data
df.describe()

```

**HOW TO WORK ON YOUR OWN NOTEBOOK.**

Before this rename your notebook to what you are working on i.e edaanalysis.ipynb,Datacleaning.ipynb don't leave it to untitled.ipynb

**Create a New Branch:**

Each team member should create their own branch to work on their notebook. This helps in keeping the main branch clean and allows for easy merging of changes.

Insert a new third cell and run:

```
#Replace you-branch-name with what you are working on i.e edaanalysis,datacleaning, etc..
!git checkout -b your-branch-name -q #meaning quite mode
```

**WORK ON YOUR NOTEBOOK**

Every person Creates their notebook according to the task in the milestone and works on it then pushes it.

**Mount and Copy your Notebook to your google drive**

Replace the datacleaning.ipynb with the file you are personally working on i.e edaanalysis.ipynb etc..

Insert a third cell and run:

```
from google.colab import drive
drive.mount('/content/drive')

!ls -la "/content/drive/My Drive/Colab Notebooks"!find "/content/drive/My Drive" -name "Datacleaning.ipynb"!cp "/content/drive/My Drive/Colab Notebooks/Datacleaning.ipynb" /content/BANK-CHURN-PREDICTION/

!ls -la "/content/BANK-CHURN-PREDICTION/"
```

**After working on your notebook**

Insert a fourth cell and run:

```
# Git commands to push the changes adding your changes
!git config --global user.name "Adamsomondi" #replace your own github name.
!git config --global user.email "mustafajohnson123@gmail.com" #replace your own github gmail.
!git add .

 # Commit your changes
!git commit -m "Updated data cleaning" #write a message "finished data Cleaning/added eda analysis"

```

**Push Your Branch**

Before you push your branch to the remote repository.

Generate a PAT Token if you dont have any,

Go to your GitHub Developer Settings. https://github.com/settings/tokens

Click on Generate new token the Token(classic one).

Select the scopes or permissions you need, such as repo for full control of private repositories.

Click Generate token and **copy the token. You will not be able to see it again, so save it securely.**

Set the Remote URL to Use HTTPS

Insert a fifth cell and run:

```
#!git remote set-url origin https://<TOKEN>@github.com/Adamsomondi/BANK-CHURN-PREDICTION.git  #replace <TOKEN> with PAT keys you created.
!git remote set-url origin https://the token@github.com/Adamsomondi/BANK-CHURN-PREDICTION.git #replace the token with what you copied

```

**Push Your Branch Using HTTPS**

```
!git push origin your-branch-name # Replace with your actual branch name you created earlier
```

**Create a Pull Request**

Once you are ready to merge your changes into the main branch, create a pull request on GitHub. This allows other team members to review your work before it is merged.

Go to the Repository on GitHub

Navigate to the repository on GitHub (https://github.com/Adamsomondi/BANK-CHURN-PREDICTION).

Switch to Your Branch from github

Switch to the branch you just pushed by selecting it from the branch dropdown menu.

Create a Pull Request

**Reviewed and Merged**

Other team members should review the pull request. Once it is approved, it can be merged into the main branch
# BANK-CHURN-PREDICTION

## Dataset Source

https://www.kaggle.com/datasets/adammaus/predicting-churn-for-bank-customers

## Description

This project leverages bank customer churn data and classification machine learning technique to accurately predict customer churn, enabling proactive decision-making and improved customer retention.We accomplished this using the following steps:

### Step 1.Data Preprocessing

   <b>a.Data cleaning</b>
   
   Removed and fixed errors(e.g., handling missing values, duplicates, or incorrect data).
   
   <b>b.Data Transformation</b>
   
   Encoded categorical variables and scaled numerical features.
   
<b>c.Data Quality Handling</b>
   
   Detected and resolved outliers, ensuring consistency in data.

  ### Step 2.Exploratory Data Analysis
  
<b>a.Descriptive Statistics</b>

Computed summary statistics (mean, median, mode, standard deviation) to understand the data distribution.

<b>b.Data Visualization</b>

Used histograms, box plots, and scatter plots to explore trends, distributions, and relationships.

### Step 3.Data Modelling















