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

