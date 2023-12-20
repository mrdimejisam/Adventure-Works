# Adventure-Works

### Introduction

Adventure work project is a guided project from the Master Power BI Desktop for data analysis with hands-on assignments & projects, Powered by Udemy. I came across the dataset and admired how rich the data is as I have been trying to get my hands dirty with a very rich dataset to practice my skills of data cleaning, analysis and visualization.

### Power BI Concepts applied:

DAX Concepts: 

Calculated column, Custom Column, Year(), IF(), Weekday(), Switch(), Left(), etc.
Data Modelling: Star Schema (*:1)

### Project Goals

Track KPIs

Compare Regional Performance

Analyze Product-level trends

Identify High-level Customers


#### Data Sourcing

Having Identified the Project goals, I went ahead to get the data. I then downloaded the csv file, and extracted it into Power BI for clening, analysis and visualization.

Adventure work folder contains the following tables:

Calender Lookup

Customer Lookup

Product Categories Lookup

Product Lookup

Product Subcategories

Return Data

Sales Data 2021-2022

Territory Lookup

Product Category Sales


### Data Transformation/Cleaning:

Data was efficiently cleaned and transformed with the Power Query Editor of Power BI. For example;

<img width="948" alt="QUERY EDITOR PRODUCT LOOKUP" src="https://github.com/mrdimejisam/Adventure-Works/assets/111657348/490c5e33-741c-4117-8166-5281609d17ab">

Some of the applied steps included

Making first row as headers in the Product Lookup table.

Add new column from the ProductSKU

Extract using delimeters to Add new column, then rename column to SKU Type 

Change datatype

## DAX Calculated Columns

Calculated column refer to entire table and were used to generate values for each row.

Some of the Dax fomulars include;




## Creating DAX Measures

Measures evaluate based on filter context, which means they recalculate when the fields or filters around them change. Measures aren't visible within tavles; they can only be "seen" within a visualization. 
Below are some measures I have created



## Data Modelling

Power BI automatically connected related tables resulting in a star schema model. The 'Sales Data' and 'Return Data' table are the fact tables of the model. The remaining tables are connected to the Fact tables via the primary key columns in the Dimension tables



## Data Analysis and Visuals


From the dashboard, it is observed that it takes 4 days on average to deliver each product on every order.
Total sales made in 2012= 2.26M, 2013=2.68M ,2014=3.41M ,2015=4.30M.
Sales is highest in the Western Europe region with almost 450k dollars.


Tamara Chand is the most valuable costumer by sales.

## Conclusions & Recommendations

An order takes 4days on average before delivery.
There has been a gradual increase in the yearly sales since 2012 at the rate of approximately 19%.
Different customers topped the profit list for each year.
Tamara Chand has made the highest sales overall since 2012 to 2015. However, on a yearly basis, Sanjit Chand made the highest sale in 2012 with over 5.7k dollars while Tamara Chand could not make the top 10 sales for that year.
In 2013; Mike Gokenbach made the higest sales with 4.8k dollars.

In 2014; Tamara chand purchased products worth 8.5k.

In 2015; Raymond Buch purchsed products worth $7.4k.

Canon Image (Class 2200) advance copier made the highest profit in both 2014 and 2015. Other Insights:
The consumer segment has made more than 50% of the total sales.
Asia Pacific is the region with the highest sales.
