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

![Data Modeling ](https://user-images.githubusercontent.com/97677904/210134103-0d0d5f3f-d450-4918-b206-c03278c12211.png)

# Data Aanalysis/ Visualization

Analysis was done using simple and appropriate visuals in Power Bi

---
# Sales by Region

![Sales by region](https://user-images.githubusercontent.com/97677904/210134228-3227989c-ca48-47db-a8ed-850f21fbafa8.png)

The company has four region in which it sales are focused on, and these are the West, East, Central and South. The image above make it clear that the West had the highest sales of $725,457 and the South with the lowest sales of $391,721

---
# Profit by Region

![Profit by region](https://user-images.githubusercontent.com/97677904/210134507-2f293477-7110-4dec-b62a-8e1bbfc10886.png)

Western region has made the highest profit so far, with about $108,418 follow by the Eastern region having $91,522 profit. The Central region had the lowest profit of $39,706

---
# Profit by Category of product

![Profit by category of product ](https://user-images.githubusercontent.com/97677904/210134660-4be1958e-a194-4ed5-b773-6d81f907f5b1.png)

There are three categories of product that are being produced in this company. We have the Technology product, Office supplies product and the Furniture product. The Technology product has brought more profit to the company's sales over the year. It has the highest profit of $145,454 and Furniture with the over all lowest profit of $18,451

---
# Sales by SalesReps

![Sales by sales rep](https://user-images.githubusercontent.com/97677904/210134762-691518d0-5c61-45eb-96b9-6a6f0e4d1235.png)

Something seems not to be right here. "ORGANIC" is definitely an outlier. After making more enquiries from the stakeholders, I got to know that the term "Organic" refers to sales made without the help of the salesreps and should thus be excluded:

![Best sales rep](https://user-images.githubusercontent.com/97677904/210134880-b5642fa5-0130-4abe-8f01-f3df930d6cf0.png)

After getting rid of the outlier which is the "Organic" from the data, the correct hierarchy of the salesReps in correlation with sales made is shown above, this help is to know the salesRep with the highest sales. As seen above, Morris Garcia had the highest sales of $92,366 and Jessica Smith had the lowest sales of $50,206

---
# Sales by Segment

![Sales by segment](https://user-images.githubusercontent.com/97677904/210135127-d8c4bde6-5361-42e8-8ad8-ee6cd677b45c.png)

The segment that had the highest sales was Consumer segment, this recorded the total sales of over $1M follow by the Corporate segment with about $700k and Home office which is the last segment had the lowest sales of $429k

---
# Sales by Customer's Name

![PNG image](https://user-images.githubusercontent.com/97677904/210136237-8b64531d-72e6-4802-8ca9-85652ba717f4.png)

Apparently, Sean Miller happens to be the customer with the highest purchase of the company product. He has made a purchase of $25k
