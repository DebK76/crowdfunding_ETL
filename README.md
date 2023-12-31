# Crowdfunding_ETL_Project 2

For this ETL mini project, we worked in a group to build an ETL pipeline using Python, Pandas, and either Python dictionary methods or regular expressions to extract and transform the data. 

To begin, once the data is transformed, we created four CSV files and use the CSV file data to create an ERD and a table schema. Finally, we upload the CSV file data into a Postgres database.

Before We Begin
Our team member Jesse Heaton- created a new repository, named Crowdfunding_ETL, for this project. And invited the rest of the team to collaborate. 

The new repository was then cloned to our individual terminals/computer.

We one person rename the ETL_Mini_Project_starter_code.ipynb file with the first name initial and last name of each member of the group. Add this Jupyter notebook file and the Resources folder containing the crowdfunding.xlsx and the contacts.xlsx files to the repository.

Instructions:

The instructions for this mini project are divided into the following subsections:

Create the Category and Subcategory DataFrames:
1. Extract and transform the crowdfunding.xlsx Excel data to create a category DataFrame that has the following columns:
A "category_id" column that has entries going sequentially from "cat1" to "catn", where n is the number of unique categories
A "category" column that contains only the category titles
2. Export the category DataFrame as category.csv and save it to your GitHub repository.
3. Extract and transform the crowdfunding.xlsx Excel data to create a subcategory DataFrame that has the following columns:
A "subcategory_id" column that has entries going sequentially from "subcat1" to "subcatn", where n is the number of unique subcategories
A "subcategory" column that contains only the subcategory titles
4. Export the subcategory DataFrame as subcategory.csv and save it to your GitHub repository.

Create the Campaign DataFrame:
Extract and transform the crowdfunding.xlsx Excel data to create a campaign DataFrame has the following columns:
The "cf_id" column
The "contact_id" column
The "company_name" column
The "blurb" column, renamed to "description"
The "goal" column, converted to the float data type
The "pledged" column, converted to the float data type
The "outcome" column
The "backers_count" column
The "country" column
The "currency" column
The "launched_at" column, renamed to "launch_date" and with the UTC times converted to the datetime format
The "deadline" column, renamed to "end_date" and with the UTC times converted to the datetime format
The "category_id" column, with unique identification numbers matching those in the "category_id" column of the category DataFrame
The "subcategory_id" column, with the unique identification numbers matching those in the "subcategory_id" column of the subcategory DataFrame

Create the Contacts DataFrame:
Choose one of the following two options for extracting and transforming the data from the contacts.xlsx Excel data:
Option 1: Use Python dictionary methods.
Option 2: Use regular expressions.

If you chose Option 1, complete the following steps:
Import the contacts.xlsx file into a DataFrame.
Iterate through the DataFrame, converting each row to a dictionary.
Iterate through each dictionary, doing the following:
Extract the dictionary values from the keys by using a Python list comprehension.
Add the values for each row to a new list.
Create a new DataFrame that contains the extracted data.
Split each "name" column value into a first and last name, and place each in a new column.
Clean and export the DataFrame as contacts.csv and save it to your GitHub repository.

If you chose Option 2, complete the following steps:
Import the contacts.xlsx file into a DataFrame.
Extract the "contact_id", "name", and "email" columns by using regular expressions.
Create a new DataFrame with the extracted data.
Convert the "contact_id" column to the integer type.
Split each "name" column value into a first and a last name, and place each in a new column.
Clean and then export the DataFrame as contacts.csv and save it to your GitHub repository.

Create the Crowdfunding Database:
1. Inspect the four CSV files, and then sketch an ERD of the tables by using QuickDBDLinks to an external site..
2. Use the information from the ERD to create a table schema for each CSV file. Specifying the data types, primary keys,  foreign keys, and other constraints.
3. Save the database schema as a Postgres file named crowdfunding_db_schema.sql, and save it to your GitHub repository.
4. Create a new Postgres database, named crowdfunding_db.
5. Using the database schema, create the tables in the correct order to handle the foreign keys.
6. Verify the table creation by running a SELECT statement for each table.
7. Import each CSV file into its corresponding SQL table.
8. Verify that each table has the correct data by running a SELECT statement for each.

Once completed, we combine all the subsections back into the final ETL_Mini_Project notebook and pushed the changes to GitHub.

Team members: 
Elias Hagos
Debbie Kabir
Thomas Gresco
Jesse Heaton 
