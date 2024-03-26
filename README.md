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
- Step 6 : The data then loaded into Power BI with close and apply for data modeling.
- Step 7 : Remove the pre-made relationships by Power BI between tables to make own.
- Step 8 : In the MODEL view, lookup tables were arranged above the data table, using valid primary/foreign keys data tables are connected to look up tables.
- Step 9 : Connect Stores to Regions as a "snowflake" schema.
- Step 10 : It was made sure that "Filter context" are one way and flow downstream from lookup table to data table, all relationships follow "one to many" cardinality and hide all the foreign keys in the fact table to only use the primary key in the dimension table by using "hide in report view" Option to avoid any ambiguity.
- Step 11 : Now create calculated columns and  DAX measures as needed for :- Total transactions, Total returns, Profit ratio, Return rate, weekend transactions and many others
- Step 12 : In the report view, under the view tab, theme was selected.
- Step 13 : Visual filters (Slicers) were added as needed on the Page.
- Step 14 : Topline performance page is made as shown below using the various visualization and formatting options in the report view.

  


###for creating new column following DAX expression was written;

###for some calculated columns :-

     Weekend = IF('Calendar'[Name of Day] = "Saturday"||'Calendar'[Name of Day] ="Sunday","Y","N")
     
     End of Month = EOMONTH('Calendar'[date],0)
     
     Short_Country = UPPER(LEFT('Customers'[customer_country],3))
     
     House Number = LEFT('Customers'[customer_address],SEARCH(" ",'Customers'[customer_address],1,BLANK()) -1)
     
     Current Age = DATEDIFF('Customers'[birthdate],TODAY(),YEAR)
     
     Priority = IF('Customers'[homeowner] = "Y" &&'Customers'[member_card] = "Golden","High","Standard")
     
###for some DAX measures :-

     Last Month Profit = CALCULATE('Transaction_Data'[Total Profit],DATEADD('Calendar'[date],-1,MONTH))
     
     Profit Margin = AVERAGEX('Transaction_Data',DIVIDE('Transaction_Data'[Total Profit],'Transaction_Data'[Total Revenue],BLANK()))
     
     Revenue Target = 'Transaction_Data'[Last Month Revenue] * 1.05
     
     Total Revenue = SUMX('Transaction_Data','Transaction_Data'[quantity]*RELATED('Products'[product_retail_price]))
     
     YTD Revenue = CALCULATE('Transaction_Data'[Total Revenue],DATESYTD('Calendar'[date]))
     
     Return Rate = DIVIDE('Return_Data'[Quantity Returned],'Transaction_Data'[Quantity Sold],BLANK())
     
     % Weekend Transactions = DIVIDE('Transaction_Data'[Weekend Transactions],'Transaction_Data'[Total Transactions],BLANK())
     
    60-Day Revenue = CALCULATE('Transaction_Data'[Total Revenue],DATESINPERIOD('Calendar'[date],MAX('Calendar'[date]),-60,DAY))   
    

    
##Snap of new calculated column ,



![image](https://github.com/23Priy/-MavenMarket_Report/assets/151018390/716fe48a-86ca-46ed-9c01-f3a20410a430)
![image](https://github.com/23Priy/-MavenMarket_Report/assets/151018390/59ca4169-bdd0-4f8a-97e1-21ed7f60ec2f)
![image](https://github.com/23Priy/-MavenMarket_Report/assets/151018390/93b0dc7f-aaeb-4f8e-8f18-973db1889079)
![image](https://github.com/23Priy/-MavenMarket_Report/assets/151018390/60eb0faf-feee-4bfd-9b19-f7549578bf9c)
![image](https://github.com/23Priy/-MavenMarket_Report/assets/151018390/0e889cfc-f3eb-40e9-9905-5da396d624e1)



##Snap of DATA MODEL,
![image](https://github.com/23Priy/-MavenMarket_Report/assets/151018390/923f434d-e2f8-4229-a7a0-a41880857028)




        
 
 # Report Snapshot (Power BI DESKTOP)

 ![image](https://github.com/23Priy/-MavenMarket_Report/assets/151018390/90be8d59-3637-4acc-a973-0c17d794f47d)



##Outcomes Achieved

This project helped me understand the whole process of Data Analysis with a project that was not as easy as I thought it would be. It revealed areas where I need to work on and definitely will help me to showcase my data cleaning and data visualization skills to the recruiters. I really enjoyed working on this project and that made me realize how I'm moving in the right direction. It is done entirely in Power BI which Pis a great tool to start with because of its user friendly interface and it has so many ever updating features to make beautiful and insight bringing reports and publishing the same using Power BI services. Hence, I chose Power BI for my project. I'm happy that I was able to use the skills I've learned so much more.
