

# Pharmaceutical Sales Analysis
In this ‘Data Analysis’ project, we’ll analyze a global Pharmaceutical Manufacturing Company's raw sales data and draw meaningful insights.

## Features
⚡PowerBI Desktop   
⚡PowerQuery Editor [For data-transformation/data-modeling]    
⚡Multipage fully Interactive Report [For drawing insights and analysis] 


## Objectives
The firm has asked us to perform in-depth data analysis to get insight into company sales performance. Specifically, below are the essential requirements to be satisfied…
|For Whom|Requirement Description|
|:---|:--|
|Executive Committee|A high-level overview showing `company’s overall sales performance by `year` by `month,` by `customer cities,` by `channel,` by `sub-channel .`Should be able to quickly see `top drug class by sales`, `top drug by sales`, `top customer city by sales`
|Sales Manager/Sales Rep|A detailed overview showing sales `by distributors and product,` `top 5 product, customer and cities`, sales numbers split by `channels and sub-channels.`
|Head of Sales|A detailed report of `sales by sales-team split by product` and `sales by sales-team split by product class.` <br> A detailed analysis showing `Top sales managers`, `Top sales reps,` `Top product split by sales team contributions` answering. <br> An ability to filter/slice data by `year` and `months.`   

***Table-1 : Requirements***

## Dataset
The dataset is sourced from each distributor. It contains Pharmaceutical Manufacturing Company’s, Wholesale-Retail Data. The field description of the raw data is given below. The raw dataset `pharma-data.csv` can be downloaded from [here](https://drive.google.com/file/d/1npKF_C2tG5psY-at4wvpEgh6T-7KHxEZ/view?usp=share_link)


### Exploratory Data Analysis (EDA) [pandas]
To understand, be familiar with and check the sanity of the given data, the first step is EDA. This project's initial data exploration has been carried out using the `pandas` python package. Here, in general, we are checking... 
 * Presence of any missing values 
 * Any unusual value (outliers) 
 * Incorrect values (e.g., sales column, we see -ve numbers)
 * Determine `categorical` and `numeric` columns
 * Determine dimensions of categorical columns and range of numeric columns
Note that these steps can be performed using `PowerQuery Editor` and/or excel; however, `pandas` makes it much easier and faster; on top of that, `pandas` can handle massive datasets.

EDA steps can be found in the `data-exploration.ipynb` notebook.

### Data Cleaning and Transform [PowerQuery Editor]
The provided dataset was relatively clean and well organized; hence only a little work was required in this step; the following steps were carried out...
* Correct column heading provided
* Correct data type is assigned to columns

### Data Model Creation [PowerBI Desktop]
* The provided data is in a single table format. The exploration revealed that it contains both categorical (`dimensions`) and numeric (`facts`) data. 
* We build a data model where dimensions and facts are separated, then they are linked together by logical relationship to form a `star schema.` The resultant data model is shown below...

### Report Creation [PowerBI Desktop]
Three interactive reports/dashboards (report pages) will be created to implement the proposed solution. Refer to [Table-3: Proposed Solution](#solution-approach) for detailed requirements and the corresponding proposed solution. 


This high-level report shows the overall sales figures and elements at a glance.

<img src="https://github.com/sssingh/pharmaceutical-sales-analysis-powerbi/blob/main/images/exec-summary-page.png?raw=true"/>


This more granular detailed report analyses data from the company distributors' and customers' perspectives. Sales by the distributor can be drilled down to specific product levels.
 
 <img src="https://github.com/sssingh/pharmaceutical-sales-analysis-powerbi/blob/main/images/dist-cust-analysis-page.png?raw=true"/>

 This is another detailed report that analyses the performance of the company's sales team. Sales by the sales team can be drilled down to product class and specific product levels.
 
 <img src="https://github.com/sssingh/pharmaceutical-sales-analysis-powerbi/blob/main/images/sales-team-perform-page.png?raw=true"/>



## Credits
- Dataset sourced from [Foresight BI](https://foresightbi.com.ng/practice-data/3-datasets-for-your-portfolio/)

[Back To The Top](#pharmaceutical-sales-analysis)
