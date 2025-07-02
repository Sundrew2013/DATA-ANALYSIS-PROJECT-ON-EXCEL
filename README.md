# DATA-ANALYSIS-FINAL-PROJECT-ON-EXCEL

![Excel Dash Board](https://github.com/user-attachments/assets/9182d22b-3fe5-45a9-a328-f0ffbac77515)

This is a project executed at the end of my data analysis course under the auspices of Digital Skill Up Africa.

## PROJECT TITLE: DSA DATA ANALYSIS CAPSTONE PROJECT 

Case Study 1: Amazon Product Review Analysis 

-[Project Overview](#project-overview)

-[Analysis Tool](#analysis-tool)

-[Dataset Description](#dataset-description)

-[Dataset Wrangling and Preparation](#data-wrangling-and-preparation)

-[Analysis Tasks](#analysis-tasks)

### PROJECT OVERVIEW

This is a project that is aimed at analysing product and customer review data to generate insights that can guide product improvement, marketing strategies, and customer engagement.s.

### ANALYSIS TOOL

I was requested to use Excel to execute this project and that is what I used.

### DATASET DESCRIPTION

The dataset contains information scraped from Amazon product pages, including: 
•  Product details: name, category, price, discount, and ratings. 
•  Customer engagement: user reviews, titles, and content.
•  Each row represents a unique product, with aggregated reviewer data stored as comma-separated valuess. 

### DATA WRANGLING AND PREPARATION

First of all, read the instructions and requirements given meticculously as this will enable you ascertain what is necessary and what is not. 

Having read thoroughly, I opened the excel data to commence the cleaning by removing unwanted columns that are not necessary for the analysis I intend to conduct. Such columns are About phone, user name, review title, review content, img-link and product link.

I created a column new column for main category considering the fact that, I noticed there are repetitions in contents and seperated by a pipe "|" symbol. Other columns created are S/N which was created by specifing a pattern by typing the first two numbers and used the fill handle to automatically fill others. Potential Revenue  was created by multiplying actual price by rating count (I did only for the first row and then use fill handle). No. of Reviews was created by using the formula below for one cell and then the apply fill handle.

      =LEN(","&$M705)-LEN(SUBSTITUTE(","&$M705,",",""))

To further clean the dataset, in the new category column, I entered the formular below to be able to extract all by the left  with the first pipe symbol as a determinant to stop.

      =LEFT(C2,FIND("|",C2)-1)
C2 represents a cell in the category column. After entering the formular, press enter, then go to the fill handle and double click to replicate same for the cells below.

To create space in between words, I use find and replace option, however you can use other options of your choice.

At this point, I copied all the require columns for the analysis into another sheet.

### ANALYSIS TASKS        

Use pivot tables and calculated columns where necessary to answer the following: 

#### 1. What is the average discount percentage by product category?
   To get this result, click on a cell in the table, click on pivot table, select new worksheet and click ok. Drag category column into rows area and Discount-Perecentage into valuess area. Right click on any of the valuess in the pivot table and summarize valuess by average. Thereafter highlight the pivot table and select any preferred chart e.g Pie chart and format to your satisfaction. Below is the chart to show this.

![Average discount percentage based on category](https://github.com/user-attachments/assets/79908fa7-f0a8-411e-8ccd-4078b0125855)

#### 2. How many products are listed under each category?

Duplicate the existing pivot table , uncheck the fields checked initially, drag category  field into rows area, product_id field into valuess area and summarize valuess by count. select the pivot table and insert the line chart. Below is the chart representation.

![No  of Products per category](https://github.com/user-attachments/assets/d7b368a8-9adc-4555-880a-f7d6f4649946)

#### 3. What is the total number of reviews per category?

Duplicate the existing pivot table, uncheked the fields initially checked, drag category field into rows area while no. of reviews field into values area and summarize by sum. Highlight the pivot table and insert line chart as shown below.

![No  of Reviews per category](https://github.com/user-attachments/assets/b5a924af-3644-458c-ad0f-eb4cd45d0abe)

#### 4. Which products have the highest average ratings?

Duplicate the existing pivot table,  uncheck initially checked field, drag Product_id field into rows area while Rating field into values area and summarize by average. Click the filter handle in the pivot table, select values filter and choose top 10, however reduce it to top five since we need just the highest as seen in the chart below.

![Top 5 products with highest rating](https://github.com/user-attachments/assets/eaca202d-1bef-4ef5-a433-0d127be708de)

#### 5. What is the average actual price vs the discounted price by category?

Duplicate the existing pivot table, uncheck initially checked fields, drag category field into rows area, Actual price and discounted price field into values area and summarize by average. Select the pivot table and insert column chart as seen below.

![Average price vs discount price by category](https://github.com/user-attachments/assets/c9a90789-1ef3-4c4c-87a3-a94568167caf)

#### 6. Which products have the highest number of reviews? 

Duplicate the existing pivot table, uncheck initially checked fields, drag Product_id field into rows area, No_of_Reviews field into values area and summarize by sum to enable you see the review values per product, Product_Id field again into the values area but summarize by count. Considering the volume of products with the highest review amounting to 1296, only the top and bottom sections were captured in the pivot table image below.

Top section of the pivot table

![Products with highest review](https://github.com/user-attachments/assets/023cc223-039c-49d2-aeb4-d17158556ed9)

Bottom section of the pivot table.

![Products with highest review bottom page](https://github.com/user-attachments/assets/751a54e9-abbd-4c68-8aad-3685e5ef2158)

#### 7. How many products have a discount of 50% or more?

Duplicate the existing pivot table, uncheck initially checked fields, drag Product_id field into rows area, Discount_percentage field into values area and summarize by sum to enable you see the review values per product, Product_Id field again into the values area but summarize by count. Considering the volume of products with 50% or more amounting to 662 products, only the top and bottom sections were captured in the pivot table image below.

Top of the table

![Above 50% Top](https://github.com/user-attachments/assets/ba0f400e-eb3c-47a1-9d1e-78c4cb8bc046)

Bottom of the table 

![Above 50% Bottom](https://github.com/user-attachments/assets/a64edca4-bd1b-4dc3-aba1-b32def9e4c3b)

#### 8. What is the distribution of product ratings (e.g., how many products are rated 3.0, 4.0, etc.)?

Duplicate the existing pivot table, uncheck initially checked fields, drag Rating field into rows area, Product_Id field into values area and summarize by count to enable you get the number of products per rating. Select the pivot table and insert a column chart as seen below.

![Distribution of product rating](https://github.com/user-attachments/assets/e5a1e4d6-4376-4e23-9ccd-fc5dab533ab1)

#### 9. What is the total potential revenue (actual_price × rating_count) by category?

Duplicate the existing pivot table, uncheck initially checked field, drag category column into rows area, Potential revenue field into values area and summarize by sum. Select the pivot table and insert line chart as seen below.

![Potential revenue by category](https://github.com/user-attachments/assets/d51bd1e9-411f-4076-be50-25491e4819ba)

#### 10. What is the number of unique products per price range bucket (e.g., <₹200, ₹200–₹500, >₹500)? 

Duplicate the existing pivot table, uncheck initially checked fields, drag Price range field into rows area, Price range field into values and summarize by count. Select the pivot table and insert line chart as seen below.

![No  of unique product per price range](https://github.com/user-attachments/assets/ac1b3c4f-686d-4a76-afff-0b49df122fae)

#### 11. How does the rating relate to the level of discount?

This has to do with Correlation Analysis 

First of all, Duplicate the existing pivot table, uncheck initially checked fields, Rating field into rows area, Discount percentage field into valuess and summarize by average. You will get the table below.

![Relationship](https://github.com/user-attachments/assets/d3e4d027-8791-49ea-9a52-1917778ffc9d)

Calculate the correlation coefficient between Rating and Discount percentage using the Correl function 

      =CORREL(RatingRange,DiscountRange)
     The answer=0.110992008
Interpretation of the correlation coefficient

Close to 1: Strong positive correlation (higher rating= higher discount)

Close to -1: Strong negative correlation (higher rating = lower discount)

Close to 0: Weak or no correlation 

In this case, it is a weak positive correlation.

#### 12. How many products have fewer than 1,000 reviews?
All products have fewer than 1000 reviews because the highest review per product is 8. Take a look at the image in question number 6, you will notice the highest review per product is 8.
    
#### 13. Which categories have products with the highest discounts?

    Duplicate the existing pivot table, uncheck initially checked columns, drag category column into rows area, discount percentage  column into valuess area and summarize by sum. Select the pivot table and insert line chart as seen below. The category with the highest discount is Electronincs.

![Categories and discount](https://github.com/user-attachments/assets/bc647584-06a6-4328-a27c-5a7304c40c2c)

#### 14. Identify the top 5 products in terms of rating and number of reviews combined.

 Duplicate the existing pivot table, uncheck initially checked fields, drag Product_Id column into rows area, Rating column and No. of Review columns into values area and summarize by sum. Select the pivot table and insert a column chart as seen below.

![Top 5 products based on rating and no  of reviews](https://github.com/user-attachments/assets/ca417da9-5c9b-426e-a213-9e8ca79a6d81)
