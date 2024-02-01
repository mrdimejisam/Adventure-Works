# Adventure-Works
## PowerBI Bike Sale Project

### Interact with Dashbord:
https://app.powerbi.com/view?r=eyJrIjoiYTVjMThhM2MtZDE0NC00ODA4LTg5ZTItNDg1YTY2NzI5ZmExIiwidCI6IjlkZDY3OTRiLWEzNWMtNGNjNC05NTZkLThiN2YxZmFlYmVjNCJ9

### Introduction

Adventure work project is a guided project from the Master Power BI Desktop for data analysis with hands-on assignments & projects, Powered by Udemy. I came across the dataset and admired how rich the data is as I have been trying to get my hands dirty with a very rich dataset to practice my skills of data cleaning, analysis and visualization.

### Power BI Concepts applied:

DAX Concepts: 

Calculated column, Custom Column, Year(), IF(), Weekday(), Switch(), Left(), etc.
Data Modelling: Star Schema (*:1)

### Project Goals

1. Track KPIs

2. Compare Regional Performance

3. Analyze Product-level trends

4. Identify High-level Customers


#### Data Sourcing

Having Identified the Project goals, I went ahead to get the data. I then downloaded the csv file, and extracted it into Power BI for clening, analysis and visualization.

Adventure work folder contains the following tables:

- Calender Lookup

- Customer Lookup

- Product Categories Lookup

- Product Lookup

- Product Subcategories

- Return Data

- Sales Data 2021-2022

- Territory Lookup

- Product Category Sales


### Data Transformation/Cleaning:

Data was efficiently cleaned and transformed with the Power Query Editor of Power BI. For example;


<img width="948" alt="QUERY EDITOR PRODUCT LOOKUP" src="https://github.com/mrdimejisam/Adventure-Works/assets/111657348/490c5e33-741c-4117-8166-5281609d17ab">


Some of the applied steps included;

- Making first row as headers in the Product Lookup table.

- Add new column from the ProductSKU

- Extract using delimeters to Add new column, then rename column to SKU Type 

- Change datatype

## DAX Calculated Columns

Calculated column refer to entire table and were used to generate values for each row.


<img width="923" alt="DAX EDU CATEGORY" src="https://github.com/mrdimejisam/Adventure-Works/assets/111657348/81c5557d-404e-4e22-ae37-812f09382090">



Some other calculated columns Dax fomulars include;


```Income Level = SWITCH(TRUE(),'Customer Lookup'[AnnualIncome] >= 150000, "Very High",'Customer Lookup'[AnnualIncome] >= 100000, "High",'Customer Lookup'[AnnualIncome] >= 50000, "Average","Very Low")```

```Quantity Type = IF('Sales Data'[OrderQuantity]>1,"Multiple item","Single Item")```


## Creating DAX Measures

Measures evaluate based on filter context, which means they recalculate when the fields or filters around them change. Measures aren't visible within tavles; they can only be "seen" within a visualization. 



<img width="954" alt="DAX MEASURE" src="https://github.com/mrdimejisam/Adventure-Works/assets/111657348/e9c97ef7-deb1-4058-a763-5a61e15acce2">



Below are some other measures I have created;

```Bike Return Rate = DIVIDE([Bike Returns],[Bike Sales],0)```

```Average Revenue Per customer = DIVIDE([Total Revenue],[Total Customers],0)```

```Previous Month Revenue = CALCULATE([Total Revenue], DATEADD('Calendar Lookup'[Date], -1,MONTH))```

```Total Orders = DISTINCTCOUNT('Sales Data'[OrderNumber]```


## Data Modelling

Power BI automatically connected related tables resulting in a star schema model. The 'Sales Data' and 'Return Data' table are the fact tables of the model. The remaining tables are connected to the Fact tables via the primary key columns in the Dimension tables


<img width="877" alt="DATA MODEL" src="https://github.com/mrdimejisam/Adventure-Works/assets/111657348/bc05c206-823c-4f39-8cc0-9ec832e98523">



## Data Analysis and Visuals




Executive Dashboard showing KPIs

<img width="608" alt="image" src="https://github.com/mrdimejisam/Adventure-Works/assets/111657348/dd4ca306-9010-46db-b80b-480bc7d5b9bf">




Product Details Dashboard


<img width="608" alt="image" src="https://github.com/mrdimejisam/Adventure-Works/assets/111657348/eafb6106-39c2-400f-a6d6-43303eb67e51">

Customer Dashboard

<img width="608" alt="image" src="https://github.com/mrdimejisam/Adventure-Works/assets/111657348/108e8e65-1ce6-4574-9560-ddf746e03bf0">








