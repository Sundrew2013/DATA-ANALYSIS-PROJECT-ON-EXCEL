# DATA-ANALYSIS-FINAL-PROJECT-ON-EXCEL

This is a project executed at the end of my data analysis course under the auspices of Digital Skill Up Africa.

## PROJECT TITLE: DSA DATA ANALYSIS CAPSTONE PROJECT 

Case Study 1: Amazon Product Review Analysis 

-[Project Overview](#project-overview)

-[Analysis Tool](#analysis-tool)

-[Dataset Description](dataset-description)

-[Data Wrangling and preparation](data-wrangling-and-prepartion)

-[Analysis Tasks](analysis-task)

-[Conclusion and Recommendation](conclusion-and-recommendation)

### PROJECT OVERVIEW

This is a project that is aimed at analysing product and customer review data to generate insights that can guide product improvement, marketing strategies, and customer engagement.s.

### ANALYSIS TOOL
I was requested to use Excel to execute this project and that is what I used.

### DATASET DESCRIPTION
The dataset contains information scraped from Amazon product pages, including: 
•  Product details: name, category, price, discount, and ratings. 
•  Customer engagement: user reviews, titles, and content.
•  Each row represents a unique product, with aggregated reviewer data stored as comma-separated values. 

### DATA WRANGLING AND PREPARATION
First of all, I read the instructions and requirements given to me as this will enable ascertain what is necessary and what is not. 

Having read thoroughly, I opened the excel data to commence the cleaning by removing unwanted columns that are not necessary for the analysis I intend to conduct. Such columns are About phone, user name, review title, review content, img-link and product link.

I created a column new column for main category considering the fact that, I noticed that there are repetitions in content and seperated by a pipe "|" symbol. Other columns created are S/N (specifing a pattern by typing the first two numbers and used the fill handle to automatically fill others). Potential Revenue  was created by multiplying actual price by rating count (I did this one and then use fill handle). No. of Reviews was created by using the formula below for one cell and then the fill handle operation 

=LEN(","&$M705)-LEN(SUBSTITUTE(","&$M705,",",""))

To further clean the dataset, in the new category column, I entered the formular below to be able to extract all by the left  with the first pipe symbol as a determinant to stop.

      =LEFT(C2,FIND("|",C2)-1)
C2 represents a cell in the category column. After entering the formular, press enter, then go to the fill handle and double click to replicate same for the cells below.

To create space in between words, I use find and replace option, however you can use other options of your choice.

At this point, I copied all the require columns for the analysis into another sheet.

### ANALYSIS TASKS        

Use pivot tables and calculated columns where necessary to answer the following: 

1. What is the average discount percentage by product category?
   To get this result, click on a cell in the table, click on pivot table, select new worksheet and click ok. Drag category column into rows area and Discount-Perecentage into values area. Right click on any of the values in the pivot table and summarize values by average. Thereafter highlight the pivot table and select any preferred chart e.g Pie chart and format to your satisfaction. Below is the chart to show this.

![Average discount percentage based on category](https://github.com/user-attachments/assets/79908fa7-f0a8-411e-8ccd-4078b0125855)

2. How many products are listed under each category?

Duplicate the existing pivot table , uncheck the columns checked initially, drage category column field into rows area, product-id into values area and summarize values by count. select the pivot table and insert the line chart. Below is the chart representation.

![No  of Products per category](https://github.com/user-attachments/assets/d7b368a8-9adc-4555-880a-f7d6f4649946)

3. What is the total number of reviews per category?

Duplicate the existing pivot table, drag category column into rows field while no. of reviews column into value area and summarize by sum. Highlight the pivot table and insert line chart as shown below.

![No  of Reviews per category](https://github.com/user-attachments/assets/b5a924af-3644-458c-ad0f-eb4cd45d0abe)

4. Which products have the highest average ratings?

Duplicate the existing pivot table,  uncheck initially checked columns, drag Product_id column into rows field while Rating column into value area and summarize by average. Click the filter handle in the pivot table, select value filter and choose top 10, however reduce it to top five since we need just the highest as seen in the chart below.

![Top 5 products with highest rating](https://github.com/user-attachments/assets/eaca202d-1bef-4ef5-a433-0d127be708de)

5. What is the average actual price vs the discounted price by category?

Duplicate the existing pivot table, uncheck initially checked columns, drag category column into rows area, Actual price and discounted price column into value area and summarize by average. Select the pivot table and insert column chart as seen below.

![Average price vs discount price by category](https://github.com/user-attachments/assets/c9a90789-1ef3-4c4c-87a3-a94568167caf)

6. Which products have the highest number of reviews? 

Duplicate the existing pivot table, uncheck initially checked columns, drag Product_id column into rows area, No_of_Reviews column into value area and summarize by sum to enable you see the review value per product, Product_Id again into the value area but summarize by count. Considering the volume of products with the highest review amounting to 1296, only the top and bottom sections only were captured in the pivot table image below.

Top section of the pivot table
![Products with highest review](https://github.com/user-attachments/assets/023cc223-039c-49d2-aeb4-d17158556ed9)

Bottom section of the pivot table.
![Products with highest review bottom page](https://github.com/user-attachments/assets/751a54e9-abbd-4c68-8aad-3685e5ef2158)

7. How many products have a discount of 50% or more?

Duplicate the existing pivot table, uncheck initially checked columns, drag Product_id column into rows area, Discount_percentage column into value area and summarize by sum to enable you see the review value per product, Product_Id again into the value area but summarize by count. Considering the volume of products with 50% or more amounting to 662 products, only the top and bottom sections only will be captured in the pivot table image below.

Top of the table

![Above 50% Top](https://github.com/user-attachments/assets/ba0f400e-eb3c-47a1-9d1e-78c4cb8bc046)

Bottom of the table 

![Above 50% Bottom](https://github.com/user-attachments/assets/a64edca4-bd1b-4dc3-aba1-b32def9e4c3b)

8. What is the distribution of product ratings (e.g., how many products are rated 3.0, 4.0, etc.)?

Duplicate the existing pivot table, uncheck initially checked columns, drag Product_id column into rows area, Rating column into value area and summarize by count to enable you get the number of products per rating. Insert Slicer and check the Rating column and increase the slicer column to three as seen in the pivot table below. Using the slicer, you only have to click on any rating and the number of product will be counted 

9. What is the total potential revenue (actual_price × rating_count) by category?

Duplicate the existing pivot table, uncheck initially checked columns, drag category column into rows area, Potential revenue column into values and summarize by sum. Select the pivot table and insert line chart as seen below.

![Potential revenue by category](https://github.com/user-attachments/assets/d51bd1e9-411f-4076-be50-25491e4819ba)

10. What is the number of unique products per price range bucket (e.g., <₹200, ₹200–₹500, >₹500)? 

Duplicate the existing pivot table, uncheck initially checked columns, drag Price range column into rows area, Price range column into values and summarize by count. Select the pivot table and insert line chart as seen below.

![No  of unique product per price range](https://github.com/user-attachments/assets/ac1b3c4f-686d-4a76-afff-0b49df122fae)

11. How does the rating relate to the level of discount?

12. How many products have fewer than 1,000 reviews?
All products have fewer than 1000 reviews because the highest review per product is 8.
    
13. Which categories have products with the highest discounts?

    Duplicate the existing pivot table, uncheck initially checked columns, drag Price range column into rows area, Price range column into values and summarize by count. Select the pivot table and insert line chart as seen below. The are 6 in the chart because there is a tie.
    
14. Identify the top 5 products in terms of rating and number of reviews combined.

 Duplicate the existing pivot table, uncheck initially checked columns, drag Product_Id column into rows area, Rating column and No. of Review columns into values area and summarize by sum. Select the pivot table and insert a column chart as seen below.

![Top 5 products based on rating and no  of reviews](https://github.com/user-attachments/assets/ca417da9-5c9b-426e-a213-9e8ca79a6d81)
