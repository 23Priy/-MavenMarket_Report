# MavenMarket_Report
# Data Analysis Project

## Data Used
Data used to make the report is added to the file section named 
## Problem Statement

Here I've worked with data from Maven Market, a multi-national grocery chain with locations in Canada, Mexico and the United States. This is a guided project (reference - udemy) that I've completely by myself but also with the directions followed and the lectures were a big help to understand everything where I stuck. This was to practice my skills and also showcase them to the potential recruiters how well I understand the concept of Data Analysis using Power BI.

### Steps followed 

- Step 1 : Converted the zip file to. xlsx and load it into Power Query for pre required transformations.
- Step 2 : Open power query editor & in view tab under Data preview section, checked "column distribution", "column quality" & "column profile" options to check for any error or empty data values and remove them if any.
- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset" to check for the errors and empty values for the entire data.
- Step 4 : Basic transformations :- name of columns, name of table, check data types of column, removing columns not required, conditional formatting, merge columns etc.
- Step 5 : The two tables "MavenMarket_Transactions_1997 " And "MavenMarket_Transactions_1998 " were appended to "Transaction_Data" having the same column structure.
- Step 5 : The data then loaded into Power BI with close and apply for data modeling.
- Step 5 : Remove the pre-made relationships by Power BI between tables to make own.
- Step 5 : In the MODEL view, lookup tables were arranged above the data table, using valid primary/foreign keys data tables are connected to look up tables.
- Step 5 : Connect Stores to Regions as a "snowflake" schema.
- Step 5 : It was made sure that "Filter context" are one way and flow downstream from lookup table to data table, all relationships follow "one to many" cardinality and hide all the foreign keys in the fact table to only use the primary key in the dimension table by using "hide in report view" Option to avoid any ambiguity.
- Step 5 : Now create calculated columns and  DAX measures as needed for :- Total transactions, Total returns, Profit ratio, Return rate, weekend transactions and many others
- Step 5 : In the report view, under the view tab, theme was selected.
- Step 5 : Visual filters (Slicers) were added as needed on the Page.
- Step 6 : Topline performance page is made as shown below using the various visualization and formatting options in the report view.

  


for creating new column following DAX expression was written;
       
        
        
Snap of new calculated column ,
![image](https://github.com/23Priy/-MavenMarket_Report/assets/151018390/bfe988ad-adb4-4bc5-9106-c65592f27f11)



        
 
 # Report Snapshot (Power BI DESKTOP)

 ![image](https://github.com/23Priy/-MavenMarket_Report/assets/151018390/90be8d59-3637-4acc-a973-0c17d794f47d)



Outcomes Achieved

This is my first full fledged Data Analysis guided project ( Mavenmarket_reports) It is done entirely in Power BI. I've used Power Query for Data transformation and cleaning part, Dax and measures to create calculated columns as needed, Data Modelling and Data visualization using the number of visuals and features available in the Power BI desktop. Power BI is a great tool to start with because of its user friendly interface and it has so many ever updating features to make beautiful and insight bringing reports and publishing the same using Power BI services. Hence, I chose Power BI for my project. I'm happy that I was able to use the skills I've learned and enjoyed the work so much.
