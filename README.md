# mj.project


Purposes Of the Project:
The major aim of the project is to gain insights into salary values by category and by experience level and to see how many deviations there are between different types of employment.

About data:
This dataset was obtained from the https://www.kaggle.com/datasets/henryshan/2023-data-scientists-salary. 
Certain changes were made, employee names were added (names are fictitious and have less connection with real people), as well as a salary bonus (salary * 2%). Dates are organized by exact days and times for additional analysis that can be presented in this project.
To conduct this analysis, a dataset containing relevant information about Data Scientists was used. The dataset includes the following variables:
Date and time: The time and date when the salary was paid. Salaries were paid on certain days of the month to the mentioned employees. The values are large because the salaries imply payments for the entire previous year (for the previous 365 days from the date indicated in the first column).

experience_level: The experience level in the job during the year.
•	EN > Entry-level / Junior
•	MI> Mid-level / Intermediate
•	SE > Senior-level / Expert
•	EX > Executive-level / Director
employment_type: The type of employment for the role.
•	PT > Part-time
•	FT > Full-time
•	CT > Contract
•	FL > Freelance
job_title: The role worked in during the year.
salary: The total gross salary amount paid.
salary_currency: The currency of the salary paid as an ISO 4217 currency code.
salaryinusd: The salary in USD.
employee_residence: Employee's primary country of residence during the work year as an ISO 3166 country code.
remote_ratio:The overall amount of work done remotely.
company_location: The country of the employer's main office or contracting branch.
company_size: The median number of people that worked for the company during the year.

 

COLUMN	DATA TYPE
Date	DATE not null
Time	Time not null
Employee_name	varchar (100) not null primary key,
Job_title	varchar (50) not null,
Job_category	varchar (50) not null,
Salary_currency	Varchar (10) not null,
Salary	INT not null,
salary_in_usd	INT not null,
employee_residence	varchar (50) not null,
experience_level	varchar (50) not null,
employment_type	varchar (50) not null,
work_setting	varchar (50) not null,
company_location	varchar (50) not null,
company_size	Varchar (5) not null,
bonus	Decimal (10,2));


Approach Used:

Data Wrangling: This is the first step where inspection of data is done to make sure NULL values and missing values are detected and data replacement methods are used to replace, missing or NULL values.
•	Build a database
•	Create a table and insert the data.
•	Select columns with null values in them. There are no null values in our database as in creating the tables, we set NOT NULL for each field, hence null values are filtered out.
Feature Engineering: This will help generate some new columns from existing ones.

•	Add a new column named time_of_day to give insight of total salaries in the Morning, Afternoon and Evening. This will help answer the question on which part of the day most salaries are paid out. 
•	Add a new column named day_name that contains the extracted days of the week on which the given transaction took place (Mon, Tue, Wed, Thur, Fri). 
•	Add a new column named month_name that contains the extracted months of the year on which the given transaction took place (Jan, Feb, Mar). Help determine which month of the year has the most paid salaries.


Generic Question
1.	How many unique company locations does the data have?
2.	In which company does the individual employee work?
3.	How many unique levels of employment does the company support/require?
4.	What is the most common employment_ type?
5.	What is the most common job title?
6.	What is the total salary by month?
7.	Which employee has the highest salary shown by individual months?
8.	In which category do employees have a higher salary than the average salary?
9.	What is the average salary by employment experience?
