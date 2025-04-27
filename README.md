# Data-analysis-and-Visualization-inExcel
This is to show how MS Excel can be used for Data analysis, Visualization, and other Basic Functions
# 1. Data Transformation
1. Ensuring that the raw data is in a usable format for analysis. 
1.1 Formatting the 'sales_date' field into a proper date format so Excel can handle it in calculations and analysis.
   This can be done by simply highlighting the 'sales_date' column and changing the data type on the number format row into date and time and ok.
1.2 Verifying that 'sales_value' and 'sales_quantity' are numeric.
     1.2.1 This one you use ISNUMBER() function where by Use ISNUMBER function that is =ISNUMBER(B:B) to check the Sales_value row and =ISNUMBER(F:F) to check the Sales_quantity row.
        N.B. If TRUE → it's a number.
         If FALSE → not a number (needs fixing).
1.3 Identify any missing or invalid data entries and handle them by either filling them in if possible or removing the affected rows to ensure that your data is clean and structured in a way that allows for efficient analysis.
     1.4 Select your dataset. Go to the Home tab - Find & Select - Go To Special - Choose Blanks - Click OK. Excel will highlight all the blank cells and in this case there was none.
#Conclusion on Data Transformation: The Excel workbook was clean for Data Analysis to begin

# 2.Statistical Analysis
#Once the data is clean, we calculate basic statistics that provide an overview of the dataset:
2.1 Total Sales Value: Sum the values in the 'sales_value' column to get the overall sales revenue.
    2.1.1 To get the SUM OF "sales_value' I used the formulae =SUM(B2:B1001)
    Or you can use a Pivot table by:-
    2.1.1.1 Go to the Insert tab - Click PivotTable. Choose where you want the Pivot Table (New Worksheet is best) - Click OK. Build the Pivot Table. In the PivotTable Fields panel, drag         sales_value into the Values area. It will automatically SUM the sales values. Now you will see the Total Sales Value displayed.
  2.2 Average Sales Value: Calculating the average sales value to understand the typical value of a sale.
      2.2.1 To get the Average OF "sales_value' I used the formulae =AVERAGE(B2:B1001)
      2.2.1.2 Or you can use pivot tables. That is by Inserting a Pivot Table, Go to Insert - PivotTable. Choose New Worksheet (recommended) - Click OK. Build the Pivot Table. In the   
              PivotTable Fields panel, drag sales_value into the Values area. Change the Calculation to Average. In the Pivot Table, click the drop-down arrow on Sum of sales_value.     
                Select Value Field Settings. Choose Average instead of Sum. Click OK. Now, the Pivot Table will show the Average Sales Value.
   2.3 Total Quantity Sold: Sum the 'sales_quantity' column to understand how many products were sold in total.
       2.3.1 To get the SUM of 'sales_quantity' I used formulae =SUM(E2:E1001) or 
       2.3.1.1 Uisng Pivot Tables by:- Go to the Insert tab - Click PivotTable. Choose where you want the Pivot Table (New Worksheet is best) - Click OK. Build the Pivot Table. In the   
               PivotTable Fields panel, Drag sales_quantity into the Values area. It will automatically SUM the sales quantity. Now you will see the Total Sales Quantity displayed.
       2.3.2 Average Quantity Sold: Calculate the average quantity sold to see typical sales volume per transaction. For this I used formulae =AVERAGE(E2:E1001) or
         2.3.2.1 Or you can use pivot tables. That is by Inserting a Pivot Table, Go to Insert - PivotTable. Choose New Worksheet (recommended) - Click OK. Build the Pivot Table. In the 
             PivotTable Fields panel, drag sales_quantity into the Values area. Change the Calculation to Average. In the Pivot Table, click the drop-down arrow on Sum of sales_quantity. 
              Select Value Field Settings. Choose Average instead of Sum. Click OK. Now,the Pivot Table will show the Average Sales quantity.

# In Conclusion These calculations give a high-level view of the performance, both in terms of revenue and units sold.

# 3. Data Analysis
Now, focused on more granular analysis to uncover trends and patterns:
     3.1 Sales by Region: Group the data by 'sales_region' and calculate the total sales value and quantity sold for each region.
       To group data as above, you use A Pivot Table. Therefore, I Insert a Pivot Table. Go to the Insert tab - Click PivotTable. Ensure the Data in well selected on the sheet and  
         Choose "New Worksheet" - Click OK. Build the Pivot Table. In the PivotTable Fields pane, drag sales_region to the Rows area. Drag sales_value - to the Values area (it will 
           automatically sum). Drag sales_quantity to the Values area (also sums automatically).
           Sales by Region Pivot Table.
  # Findings from the Pivot Table analysis, we observe that North America and South America are the top-performing regions, contributing the highest sales values of $1,080,783.89 
  # and $1,062,211.97 respectively. Together, they account for a significant portion of the total global sales revenue. Europe and Asia show similar performance levels, each 
  # generating around $975,000 to $979,000 in sales value, indicating stable markets with potential for further growth. Africa, while contributing a slightly lower sales value 
  # of $939,968.06, still maintains a strong sales quantity relative to the other regions, suggesting a high volume but potentially lower-value transactions. In total, all 
  # regions combined achieved a grand sales value of $5,038,148.02 across 483,300 units sold. This distribution highlights that while sales quantities are relatively close 
  # across regions, the value of sales varies, with North and South America leading in terms of revenue generation.
  
  3.2 Sales by Channel: Group by 'sales_channel' (e.g., Direct Sales, Distributor) to see how each sales channel is performing.
     Insert a Pivot Table. Go to the Insert tab - click PivotTable and Select the Data. Choose where you want the Pivot Table to be placed (New Worksheet is recommended). Set Up the 
      Pivot Table. Drag sales_channel to the Rows area. Drag sales_value to the Values area (set to Sum of sales_value). Drag sales_quantity to the Values area too.
      From the analysis of sales performance across different channels reveals the following: 
       - In-store sales contributed the highest sales value at 1,306,267.82, with the highest sales quantity of 122,097 units sold.
       - Direct sales closely followed, generating 1,304,220.94 in sales value and 117,736 units sold.
       - Online sales performed strongly as well, with 1,259,954.68 in total sales value and 125,585 units sold.
       - Distributors had the lowest total sales value among the channels at 1,167,704.58, but interestingly sold 117,882 units, slightly more than Direct sales.
  # Overall, In-store and Direct sales channels are the leading contributors to total revenue, while Online channels show solid volume performance, highlighting a potential area for 
  # further growth and investment. The Grand Total across all channels stands at 5,038,148.02 in sales value and 483,300 units sold.
   
   3.3 Sales by Salesperson: Evaluate the performance of individual salespeople by grouping the data by 'salesperson_id' and calculating total sales and quantities sold per 
         salesperson. Insert a Pivot Table. Go to the Insert tab - Click PivotTable. In the dialog box: Ensure your data range is selected. Choose New Worksheet or Existing Worksheet 
          depending on where you want the PivotTable to appear. Click OK. Build Your Pivot Table. In the PivotTable Field List:- Drag salesperson_id into the Rows area. Drag sales_value 
          into the Values area. Drag sales_quantity into the Values area.
  # Overall, Sales Person ID 846 has the most Sales compared to the rest of the Sales person and 323 having the least amount of sales.
    
# In conclusion, this analysis will help you understand which regions, channels, and salespeople are the most successful, and where there might be room for improvement.

# 4. Data Visualization (Dashboard)
To make the data insights more accessible, I created a dashboard that visualizes key metrics:
4.1 Bar Charts: Use bar charts to compare total sales values by region, sales channel, and salesperson. This will help highlight the biggest contributors to sales.
    4.1.1 Sales value by Region Bar Chart
    ![image](https://github.com/user-attachments/assets/55eaf43c-8724-4092-a556-16bb78033806)
    The above graph shows the Sales value for the various regions. North America has the highest number of sales while Africa has the lowest number. The graph was generated from the 
      pivot tables above.
    4.1.2 Sales Value by Sales Channel.
    ![image](https://github.com/user-attachments/assets/0ff5cb02-516e-4b25-9acf-1d02a0a466aa)
      From the above bar graph we can conclude that Instore distributors sell the most followed closely by Direct Sales. The least number of sales is obtained from the distributors. As           above the graph was generated from Pivot table.
    4.1.3 Sales Value by Salesperson
    ![image](https://github.com/user-attachments/assets/a0e43a46-0a68-4470-a18f-b73ae1620e5d).
    The graph above shows the various levels of sales made by the various salesperson. Sales Person ID 846 has the most Sales compared to the rest of the Sales person and 323 having 
     the least amount of sales.
     
4.2 Trend Charts: Plot the data over time to identify trends, such as rising or falling sales in certain periods.
    4.2.1 Trends chart to show the trends rising and falling sales periods
    ![image](https://github.com/user-attachments/assets/fcff7fd4-9e50-4c0d-abf6-8f1abe066690)
    From the above line graph, August has the highest spike in sales, and December has the least number of sales as per  the trend. The graph was also generated from a pivot table.
    
4.3 Pie Charts: Use pie charts to show how sales are distributed by channel or region, helping to visualize the market share and areas of focus.
      4.3.1 Sales distribution by Region pie chart
      ![image](https://github.com/user-attachments/assets/ca43dd8b-29b7-4d14-9248-a6f0c4e30128)
      The Pie chart graph shows the distribution of sales among the various Regions. North America has the highest number of sales, while Africa has the lowest number. The graph was 
       generated from the pivot tables above.

4.3.2 Sales distribution by Channel pie chart
![image](https://github.com/user-attachments/assets/94754b27-b486-42f1-abe6-738f7951a89c)
      From the above pie chart, we can conclude that Instore distributors sell the most, followed closely by Direct Sales. The least number of sales is obtained from the distributors. 
       as above, the graph was generated from Pivot table.

      
  # The visual dashboard is crucial for providing clear and concise insights that are easy to interpret for stakeholders.

