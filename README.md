# CUSTOMER-SHOPPING
Datasets of shopping malls in Turkey


**CUSTOMER SHOPPING DATASET (A CASE STUDY OF 10 SHOPPING MALL IN TURKEY)**
Hi guys, this is my second documentation on Microsoft excel for data cleaning, creating pivot chart and interactive dashboard. Together, let’s explore the dataset and discover the fascinating world of Istanbul shopping.
The Data Collection
This dataset was obtained from Kaggle. You can get the dataset from this link.
https://www.kaggle.com/datasets/mehmettahiraslan/customer-shopping-dataset?resource=download
About Dataset
Welcome to the shopping world of Istanbul! The dataset contains shopping information from 10 different shopping malls between 2021 and 2023. Data was gathered from various age groups and genders to provide a comprehensive view of shopping habits in Istanbul. The dataset consists of 10 columns. The dataset includes essential information such as invoice numbers, customer IDs, age, gender, payment methods, product categories, quantity, price, order dates, and shopping mall locations. 
Data dictionary:
•	invoice_no: Invoice number. Nominal. A combination of the letter 'I' and a 6-digit integer uniquely assigned to each operation.
•	customer_id: Customer number. Nominal. A combination of the letter 'C' and a 6-digit integer uniquely assigned to each operation.
•	gender: String variable of the customer's gender.
•	age: Positive Integer variable of the customers age.
•	category: String variable of the category of the purchased product.
•	quantity: The quantities of each product (item) per transaction. Numeric.
•	price: Unit price. Numeric. Product price per unit in Turkish Liras (TL).
•	payment_method: String variable of the payment method (cash, credit card or debit card) used for the transaction.
•	invoice_date: Invoice date. The day when a transaction was generated.
•	shopping_mall: String variable of the name of the shopping mall where the transaction was made.

Data Cleaning
Prior to the analysis of the dataset, I took it upon myself to carefully go through data cleaning to ensure its accuracy and reliability. This process involved thoroughly scrutinizing each data column for any inconsistencies, errors, outliers and duplicates.
However, I discovered the dataset was already cleaned. Hence, it was ready for thorough analysis. For the sake of this analysis, Microsoft Excel was used for the data exploration and analysis.
The first step was to import the raw dataset into Microsoft Excel. This involved opening a new Excel sheet and selecting the “Data” tab from the top menu. From there, I selected “From Text/CSV” and browsed for the dataset file. After selecting the file, I clicked “Import” to bring the data into Excel.

For more overview of the dataset, I explored some excel functions, such as AVERAGE, MAX, MIN, MEAN, MEDIAN to calculate summary statistics for Age, Quantity and Price.
Age
The analysis of the age distribution of customers revealed that the average age was 43 years, with a min and max range of 18 and 69 years. 
MEAN_AGE =AVERAGE(D:D), MIN_AGE = MIN(D:D), MAX_AGE = MAX(D:D)
It can be inferred that the ages are not uniformly distributed around the mean but rather are spread out in a moderate range of values, with some customers being much younger (18) or older (69) than the mean age (43).
Quantity
It discovered that the average number of items purchased per transaction was 3.00, with a minimum and maximum of 1 and 5 respectfully. Additionally, the median or 50th percentile of 3 indicated that half of the transactions involved the purchase of 3 or fewer items, while the other half involved the purchase of 4 or more items. Finally, the 75th percentile value of 4 suggested that 75% of the transactions involved the purchase of 4 or fewer items.
MEAN_qty =AVERAGE(D:D), MIN_qty = MIN(D:D), MAX_qty = MAX(D:D)
MEDIAN =PERCENTILE.EXC (F:F,0.5)
Price
The calculation revealed that the average price per item sold was 689.26 Turkish Lira (TL), with a minimum price of 5.23 TL and a maximum price of 5250 TL. The median or 50th percentile value of 203.3 TL suggested that half of the products sold were priced at 203.3 TL or lower, and the other half were priced higher. 

SOME ADDITIONAL CALCULATION
The Age column was used to group the data field to Age bracket using the formula below:

Age bracket =IF(D2<25,"18-24", IF(D2<35,"25-34", IF(D2<45, "35-44", IF(D2<55,"45-54", IF(D2>=55, "55 and more"))))).
Revenue
This is a custom column calculated by multiplying the price column and the quantity column
Revenue = G2*H2
PIVOT TABLE FOR ALL CHARTS
pivot tables were created to analyze data related to product categories, shopping mall locations, payment method, Purchase by age group, sales per year and gender.

1.	Payment method
For this pivot table, payment method, count of payment method was expressed as percentage (%) of grand total. The given data consist of three different payment methods. The cash, credit card, and debit card. The cash payment method had the highest use making up 44% of the total payment method.

2.	Purchase by gender
This indicates that Female gender had 20% increase in purchase over the male counterpart. This can be likely due to some of the products having affinity to the female gender such as clothing, cosmetics having the first and second largest sales respectfully.

3.	Purchase by category of products
The clothing category had the highest sales while books had the least sales


4.	Shopping mall by sales
The mall of Istanbul had the highest sales while Forum Istanbul shopping mall contributed the least sales.
4 prominent malls (Mall of Istanbul, Kanyon, Metrocity, Metropol AVM) made up to 65% of the total sales. The wide variation in sales may be due to location of these mall.

Sales per Age group
The table below represents the sales distribution across various age brackets. The highest proportion of sales, which amounts to 28.46%, is contributed by the age group (55 and more).
25-54 age bracket contributed to 57% of total sales, followed by 55 and more, while the age bracket of 18-24 had the least sales.

![image](https://github.com/jaybee30/CUSTOMER-SHOPPING/assets/106179938/35e8a740-f981-4da5-b190-6e7183279b09)
