# Ecommerce Sales Report

## Problem Statement

This dashboard helps the Ecommerce company to understand well about their sales better. It helps the Ecommerce company know if their customers are satisfied with their products. Through different comparisons, they get to know their improvement area, & thus they can improve their product sales by identifying these areas. It also let them know the profit by product, region wise sales delay & departure time for delivery, thus since by using this dashboard they have identified this problem, they can further work on factors responsible for losing the profit and unwanted delays deliveries with respect to the region.

Since, number of customers in count are more in Consumer category and less in other categories and hence all they must work on improving on their sales on different products and other shipping types.

Also since discounts need to be based on the type of product and different regions including the segment types, hence need to focus on discount level for different regions.

### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a xlsx file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
- Step 4 : Clearing all the empty spaces in the tabular columns and most of the table's data accurate enough with less errors.
- Step 5 : Creating the Table for Calendar for the period of sales. 
- Step 6 : In the report view, under the view tab, theme was selected.
- Step 7 : Applying the visuals and filtered out the data with the given title and visualization format.
- Step 8 : Visual filters, Donut chart, filled map and Pie charts were added for the fields named "Region sales", "Sales by month", "Sales by product name" & "Shipping type".
- Step 9 : Three card visuals were added to the canvas, one representing Order Quantity, Overall Profit & Profit per Order
           Using visual level filter from the filters pane, basic filtering was used & null values were unselected 
- Step 10 : Stacked Column & Bar Charts were added to the Customer segment profit and Discount by Product.
- Step 11 : Line Chart was used to represent Sales for different Products.
 
- Step 12 : Calendar table was created in which, sales period depends on [Order date] was added:

	Following DAX expression was written:

		Calendar = 
		
		CALENDAR(MIN
			(ecommerce_data[order_date]
				),
			MAX(ecommerce_data[order_date]
				)
			)
Snap of Calender Table
![Snap_calender](https://github.com/user-attachments/assets/266d4e20-d0b7-4628-85b1-10fd0e8d387e)

        
 - Step 13 : New measure was created to find Sum Sales,
 
 Following DAX expression was written to find Sales,
 
         Sales = CALCULATE(SUM(ecommerce_data[sales_per_order]), 'Calendar'[Month_number])
 
 A card visual was used to represent this Sales.
 
 Snap of Sales as per Sales per order with respect to month,
 
 ![Snap_Sales](https://github.com/user-attachments/assets/a9e19179-f914-44bf-b5b3-744915bc2dfd)


 # Report Snapshot (Power BI DESKTOP)

 
![Snap_Dashboard](https://github.com/user-attachments/assets/db380ff3-27d2-4f24-8506-0facde940399)

# Insights

A single page report was created on Power BI DESKTOP.
Following inferences can be drawn from the Report;

### [1] Total Number of Sales = 23.16 M

   Number of sales  (Standard) = 13.85 M (59.78 %)

   Number of sales  (Second class) = 4.5 M (19.41 %)

   Number of sales  (First Class) = 3.6 M (15.52 %)

   Number of sales  (Same Day) = 1.2 M (5.29 %)


           Thus, higher number of sales are in Standard.
           
### [2] Profit by Customer segment

    a) Consumer = $ 1.37 M
    b) Corporate = $ 0.79 M
    c) Home Office = $ 0.45 M
  
    
  
  ### [3] Top 5 Products 
  
      a) Staples
      b) Staple Envelope
      c) Easy-staple paper
      d) Ki- Adjustable Table
      e) Avery Non-stick binders

 ### [4] Some other insights

    Sales by Region

    Central  = 5.3 M (23.29 %)
    East     = 6.59 M (28.46 %)
    West     = 7.42 M (32.03 %)
    South    = 3.76 M (16.21 %)



# Ecommerce Sales Report.md.txt
Displaying # Ecommerce Sales Report.md.txt.
