---
# GUIDE FOR TEAM MEMBERS 

## Overview
This project uses a  Bank churn Kaggle dataset stored in **Google Drive** for easy access by all team members. We will work collaboratively using **Google Colab** notebook

## HOW TO USE THIS GITHUB REPOSITORY AS A TEAM

Open google colab https://colab.google/

Open  a new notebook

Inside the first colab code cell Run:
```sh
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

## HOW TO USE THE DATASET AS A TEAM

 Insert a new second colab code cell then Run:
 ```sh
 import pandas as pd

# Correct direct file link
file_id = "1-6FhvYRRgceTptrIMfgvaXkq-QKw8dwf"
file_url = f"https://drive.google.com/uc?id={file_id}"

# Load the dataset
df = pd.read_csv(file_url)

df
```

## HOW TO WORK ON YOUR OWN NOTEBOOK.

Before this rename your notebook to what you are working on i.e Data_Preprocessing.ipynb edaanalysis.ipynb<b> don't leave it to untitled.ipynb</b>

Work on your notebook according to the task in the milestones.

 ### Create a New Branch: 
 
 Each team member should create their own branch to work on their notebook. This helps in keeping the main branch clean and allows for easy merging of changes.

 Insert a new third cell and run:
 
 ```sh
 #Replace you-branch-name with what you are working on i.e edaanalysis etc..
 !git checkout -b your-branch-name -q #meaning quite mode
  ```

## Mount and Copy  your Notebook to a Google Drive

Keeps your original notebook safe in Google Drive you can access it later.

Prepares files for execution in an isolated workspace i.e Github.

Insert a third cell and run:

```sh
from google.colab import drive
drive.mount('/content/drive')

!ls -la "/content/drive/My Drive/Colab Notebooks"
!find "/content/drive/My Drive" -name "Data_Preprocessing.ipynb" #replace "Data_Preprocessing.ipynb" with the name of your file i.e edaanalysis.ipynb

!cp "/content/drive/My Drive/Colab Notebooks/Data_Preprocessing.ipynb" /content/BANK-CHURN-PREDICTION/ #replace Data_Preprocessing.ipynb with the name of your file

!ls -la "/content/BANK-CHURN-PREDICTION/"
```
 
# After working on your notebook 

 Insert a fourth cell and run:
 
```sh
# Git commands to push the changes adding your changes
!git config --global user.name "Adamsomondi" #replace your own github name.
!git config --global user.email "mustafajohnson123@gmail.com" #replace your own github gmail.
!git add . #adds the file

 # Commit your changes
!git commit -m " Finished Data_Preprocessing.ipynb file" #write a message "finished eda analysis"

```

 ## Push Your Branch
 
 Before you push your branch to the remote repository.

Generate a PAT Token if you don't have any.

Go to your GitHub Developer Settings. https://github.com/settings/tokens

Click on Generate new token the <b>Token(classic one)</b> do not generate fine grained token.

Select the scopes or permissions you need, such as repo for full control of private repositories.

Click Generate token and <b>copy the token</b>. You will not be able to see it again, <b>so save it securely</b>.

 Set the Remote URL to Use HTTPS

Insert a fifth cell and run:

 ```sh
#!git remote set-url origin https://<TOKEN>@github.com/Adamsomondi/BANK-CHURN-PREDICTION.git  #replace <TOKEN> with PAT keys you created.
!git remote set-url origin https://the token@github.com/Adamsomondi/BANK-CHURN-PREDICTION.git #replace the token with what you copied

```

# Push Your Branch Using HTTPS

```sh
!git push origin your-branch-name # Replace with your actual branch name you created earlier

```

 # Create a Pull Request

 Once you are ready to merge your changes into the main branch, create a pull request on GitHub. This allows other team members to review your work before it is merged.
 
 Go to the Repository on GitHub

 Navigate to the repository on GitHub (https://github.com/Adamsomondi/BANK-CHURN-PREDICTION).


 Switch to Your Branch from github

Switch to the branch you just pushed by selecting it from the branch dropdown menu.

Create a Pull Request
 
 ## Reviewed and Merged
 Other team members should review the pull request. Once it is approved, it can be merged into the main branch

  ---
 
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















