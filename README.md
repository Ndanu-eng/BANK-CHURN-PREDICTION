---
# FOR TEAM MEMBERS 

## Overview
This project uses a  Bank churn Kaggle dataset stored in **Google Drive** for easy access by all team members. We will work collaboratively using **Google Colab** notebooks, ensuring everyone can load and analyze the dataset without downloading it locally.

## HOW TO USE THIS GITHUB REPOSITORY AS A TEAM

Open google colab new notebook From your Chrome Browser:

 https://colab.google/

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

 ## Option 1-Easy
 Insert a new second colab code cell then Run:
 
 ```sh
 import pandas as pd

# Correct direct file link
file_id = "1-6FhvYRRgceTptrIMfgvaXkq-QKw8dwf"
file_url = f"https://drive.google.com/uc?id={file_id}"

# Load the dataset
df = pd.read_csv(file_url)

# Describe the data
df.describe()
```

# Option 2-Flexibility
Click the BankChurn shared folder link below then open shared tab inside Google drive to make sure you can access it.

```sh
https://drive.google.com/drive/folders/1kyYj-jEOInyj-Kes1PoSz9AWVXCCSYmQ?usp=sharing
```

 Open a google Colab NewNotebook then Run:
 
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

## HOW TO WORK ON YOUR OWN NOTEBOOK

 **Create a New Branch:**
   Each team member should create their own branch to work on their notebook. This helps in keeping the main branch clean and allows for easy merging of changes.

 # Create a new branch
 Insert a new third cell and run:
 
 ```sh
 #Replace you-branch-name with what you are working on i.e Datacleaning
 !git checkout -b your-branch-name
  ```

## Move the colab  file to your working directory

```sh
from google.colab import drive
drive.mount('/content/drive')

!ls -la "/content/drive/My Drive/Colab Notebooks"
!find "/content/drive/My Drive" -name "Datacleaning.ipynb"

!mv "/content/drive/My Drive/Colab Notebooks/Datacleaning.ipynb" /content/BANK-CHURN-PREDICTION/

!ls -la "/content/BANK-CHURN-PREDICTION/"
```

# After working on your notebook
 
```sh
   # Add your changes
!git config --global user.name "You Name" #replace your github name.
!git config --global user.email "you@example.com" #replace your github gmail.
!git add .

   # Commit your changes
!git commit -m "Describe your changes" #write a message "finished data Cleaning"
```

 **Push Your Branch:**
   Push your branch to the remote repository.

   Generate an ssh key.

   ```sh
ssh-keygen -t ed25519 -C "your-email@example.com" #replace with your github email.
```
 Get the Key
```sh
!cat ~/.ssh/id_ed25519.pub
```

Add the ssh key to your Github

   ```sh
   !git push origin your-branch-name #replace with your actual branch-name
   ```

**Create a Pull Request:**
   Once you are ready to merge your changes into the main branch, create a pull request on GitHub. This allows other team members to review your work before it is merged.

 **Review and Merge:**
   Other team members should review the pull request. Once it is approved, it can be merged into the main branch
   
 ---
 
# BANK-CHURN-PREDICTION
## Milestone 1

![Screenshot](https://github.com/Adamsomondi/BANK-CHURN-PREDICTION/blob/main/images/Screenshot%202025-03-19%20031243.png)

## Data Understanding

....

....

....


## Exploratory Data Analysis

....

....

....


## Milestone 2
## Modelling Approach

....

....

....

## Milestone 3
## Evaluation Metrics

....

....

....

 









