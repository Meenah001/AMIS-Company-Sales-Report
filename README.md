# AMIS-Company-Sales-Report

# Introduction
In order to know the best location to build a new branch of AMIS company, an analysis was carried out on the dataset given for this to be achieved.The problem satatement is an imaginary case scenario I thought about after seeing the dataset.

# Problem Statement

An international company in Canada known as AMIS COMPANY wish to build a new branch of their office in a location where the highest sales has been made. At the board meeting, the stakeholders made a conclusion of awarding the salesrep that made the highest sales as the Manager of the new branch, also to give discount to the customer that has made the highest purchase.

In order to achieve this, three questions need answers:
1. Which Region/location has the highest sales made?
2. Which Sales rep has made the highest sales?
3. Which of our Customers purchased highest sales?

The dataset is an excel file saved locally in a folder. The dataset is denormalised, that is all data are in a single table and this is not ideal for carrying out analysis

# Data sourcing
The data was normalised that is, the combined information was seperated into differnt tables resulting into 5 tables:
* Sales Table
* Customers Table
* Sales Reps Table
* Location Table
* Products Table

Data was then imported from Excel Workbook into Power BI for transformation, analysis and visualization.

# Data Transformation 

Data cleaning and transformation was performed per table. All the tables are then cleaned with no errors or null values. Below is a preview of each tables:

---
Customer's Table

![Customer’s Table](https://user-images.githubusercontent.com/97677904/210133551-6dfc7fca-8ece-4c41-886b-c346d05a0ff6.png)

---
Location's Table

![Location Table](https://user-images.githubusercontent.com/97677904/210133594-e4d0d827-9b0c-4c15-8207-035d70f02d12.png)

---
Product Table

![Product Table](https://user-images.githubusercontent.com/97677904/210133614-38f5bcc3-8e99-488a-a7c0-c1d5b0e4e7ff.png)

---
SalesReps Table

![Sales reps Table](https://user-images.githubusercontent.com/97677904/210133658-ffb153b3-cfd8-412c-ab6e-8763c64fb321.png)

---
Sales Table

![Sales Table](https://user-images.githubusercontent.com/97677904/210133688-2be86f61-2c81-4100-8dad-5fab2b46a47b.png)

For both Customers and Products Table, first rows were not headers and this was solved by applying the "Use First row as header" in power query. The datatypes for each column was also changed accordingly

# Data Modelling
The data for this analysis are located in various tables. For this reason, appropriate modelling is required. A star Schema is designed with the Sales Table representing the fact table containing all redundant data, and to which other dimension tables are connected to, using the column that is common. Sales Table has been modelled with:

* SalesRep Table using the "SalesRep ID"
* Locations Table using the "Location ID"
* Products Table using "Product ID"
* Customers Tables via "Customer ID"








