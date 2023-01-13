# CustomerLifetimeValue

Calculating Customer Lifetime Value (CLV

Background: In marketing, customer lifetime value (CLV or often CLTV), lifetime customer value (LCV), or life- time value (LTV) is a prediction of the net profit attributed to the entire future relationship with a customer. Customer lifetime value can also be defined as the dollar value of a customer relationship, based on the present value of the projected future cash flows from the customer relationship. Customer lifetime value is an important concept in that it encourages firms to shift their focus from quarterly profits to the long-term health of their customer relationships. Customer lifetime value is an important number because it represents an upper limit on spending to acquire new customers. For this reason it is an important element in calculating payback of advertising spent in marketing mix modeling.[1] 

Dataset : The dataset is provided in CSV format in the file clv_transactions.csv. and contains roughly 4,200 transactions records. Each row in the dataset represent a single transaction. There are four columns in the dataset. The TransactionID is a unique identifier of individual transactions. The TransactionDate is the date of the transaction. The CustomerID is the identifier of the customer who made the transaction. And the Amount is the recorded amount of transaction in US dollars.


Recommended Reading - 
https://usermanual.wiki/Pdf/gormanalysiscomPractical20Guide20to20Calculating20Customer20Lifetim e20Value20CLV.2014990060


STEPS 

Step 1: Understand the dataset
The first thing you should do is to load the CSV file and understand the dataset. It is important to understand the dataset and examine if there is any missing values or outliers before doing analysis. In this step, you should write Python scripts to answer the following questions.
1. Are there any missing values in the dataset?
2. What is the range of dates in the dataset?
3. How many unique customers are there in the dataset?
4. Profile the data to give the standard descriptive statistics for the Amount field. What is
the min, max, variance, and standard deviations?
5. Do transaction amounts in general increase over time (perhaps due to inflation)?

Step 2: Explore the dataset
Next, explore the dataset to check if there are any outlier or if there are values that don’t make sense. You can use statistical tests to check for outliers. Or, you can simply plot the histogram of the Amount and see if there is any value that appears to be abnormal. (Hint, is there any value that appears to be abnormally large or small? Could it be caused by bad entries (e.g. forgetting decimal separator?). In this step, you should write python scripts to help you answer the following questions.
1. Are there any outliers?
2. If so how would you treat them?

Step 3: Determine origin year of customers
Some of the underlying customers are brand new and others have been customers for almost five years. Obviously the newer customers will have (generally) spent less on average than the old ones. So, we need to separate the customers into groups based on how long ago they were acquired (e.g. customers acquired in 2010, vs customers acquired in 2011, ...). First, assign customers into different groups based on the date of acquisition (origin year). For instance, the earliest transaction date that can be found for customer 2 in the dataset is 5/15/12. Then we assign customer 2 into group 2012 as this customer was acquired in the year 2012. Write Python scripts to assign the appropriate origin year to all customers,
   
Step 4: Calculate cumulative transaction amounts
Now, calculate the cumulative transaction amounts for customers in each group of origin year. 
To obtain this value:
• First, find the transaction records for customers with the origin year 2010 (use your result from step 3)
• Then, sum up the amounts made by these customers up to 12 months later than the origin year. Therefore, you should check the TransactionDate to determine if you should include a particular transaction into the sum (e.g. you sum the amount only if the TransactionDate is no greater than 12 months since the start of 2010). Now, do the same calculations for the rest of the entries in the table and print your table to standard output (or document it in comments block).
 
Step 5: Calculate cumulative transaction amounts
Again using Python, calculate the number of new customers by origin year in each year. 
In this table, each entry represents the number of new customers acquired during each origin year. Since this number is irrelevant to age, values for each column in the same row should be the same. Print your table to standard output (or document it in comments block).

Step 6: Historic CLV
Finally, you are ready to calculate the Historic CLV. Dividing the Amount.cmltv triangle by the NewCustomers.cmltv triangle will give us annual measurements of the cumulative amount spent per customer in each group of annually acquired customers. This is also known as Historic CLV. Print your table to standard output (or document it in comments block). 

 Step 7: Interpreting your results
Interpret the historic CLV and briefly answer the following question: 
- How much have customers acquired in 2011 spent to date?
- Do each group of customers exhibit similar or different patterns of spending? What’s the implication for the business?



External Sources
[1] https://en.wikipedia.org/wiki/Customer_lifetime_value
       
[2]https://usermanual.wiki/Pdf/gormanalysiscomPractical20Guide20to20Calculating20Customer20Lifetim e20Value20CLV.2014990060
