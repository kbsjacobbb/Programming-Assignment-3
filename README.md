# ECE 2112 - Experiment 3: Python Data Analysis (PANDAS)

Balagtas, Jacob T.

2ECE-B

9/10/2026

## Objective of the Experiment

The objective of this experiment is to hone and develop Python skills. In these activities, the programmer tackles the topic of PANDAS or **Python Data Analysis**. It will help in gaining knowledge and developing skills in concepts such as positional and label-based indexing, filtering records using certain conditions, and extracting a well-defined subset without altering the source.

### General Codes:

    import pandas as pd

The code above is a Python command that imports the **pandas** library and uses the alias "pd" to shorten it.

    cars = pd.read_csv('cars.csv')

The code above is used to read the imported CSV file. The name of "cars" is the assigned variable, **pd.read_csv** is the command used to read the CSV file, and **cars.csv** is the CSV file being read.

## A. POSITIONAL AND LABEL-BASED SLICING

### Code:

    cars = pd.read_csv('cars.csv')
    cars

The code above reads the imported CSV file and displays its contents.

    cars.shape

    cars.columns.tolist()

These codes display the shape and the column names, respectively.

    cars_6_to_10 = cars.iloc[5:10]
    cars_6_to_10

These lines of code display the contents of rows 6-10 in the CSV file, but 5-9 in the content. The code of **cars.iloc[5:10]** selects and returns rows 5 through 9; in this code, it will always exclude the last number.

    cars_6_to_10 = cars_6_to_10[['Model', 'mpg', 'cyl', 'hp', 'gear']]
    cars_6_to_10

The code emphasizes that the variable **cars_6_to_10**, which shows rows 5-9 in the content, only shows the 'Model', 'mpg', 'cyl', 'hp', and 'gear' columns for each row.

## B. MODEL LOOKUP

### Code:

    toyota = cars[(cars['Model'] == 'Toyota Corolla')]
    toyota

The code emphasizes that the variable "cars" shows the row for **Toyota Corolla** with **cars['Model']** set to  **Toyota Corolla**.

    pontiac = cars[(cars['Model'] == 'Pontiac Firebird')][['Model', 'mpg', 'hp', 'wt']]
    pontiac

This is similar to the first line of code, but this time it shows only the 'Model', 'mpg', 'hp', and 'wt' for the selected car.

## C. MULTI-MODEL SUBSETTING

### Code:

    models = ['Datsun 710', 'Lotus Europa', 'Ferrari Dino']

This line of code emphasizes that the variable **models** is stating three elements, the 'Datsun 710', 'Lotus Europa', and 'Ferrari Dino.'

    selected_cars = cars.loc[cars['Model'].isin(models), ['Model', 'mpg', 'cyl', 'hp', 'gear']]
    selected_cars

With the help of the first code, the line **cars.loc[cars['Model'].isin(models)** filters the dataset to identify the **models** or cars being asked for. On the other hand, the line **['Model', 'mpg', 'cyl', 'hp', 'gear']** specifies what columns are to be shown with the selected cars.

    print("Shape of Selected Cars: ")
    selected_cars.shape

Lastly, this line of code shows the shape of the variable **selected_cars**.
