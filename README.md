
Name: Manzi Arsene
Student ID: 27435
Group: Group A

------------------------------------------------------------

1. BUSINESS PROBLEM

Business Context
The organization is a retail company selling consumer products across multiple regions. The sales department needs analytical reports to evaluate product performance, understand customer purchasing behavior, and track sales trends over time.

Data Challenge
The company has transactional sales data, but it is not organized for advanced analysis. Management cannot easily determine best-selling products, customer segments, or changes in sales over time.

Expected Outcome
Develop SQL JOIN and Window Function queries that produce ranked results, running totals, growth comparisons, and customer segmentation to support business decision-making.

------------------------------------------------------------

2. SUCCESS CRITERIA

1. Identify top-selling products using RANK()
2. Calculate running totals using SUM() OVER()
3. Compare current and previous sales using LAG()
4. Segment customers into quartiles using NTILE(4)
5. Compute average sales trends using AVG() OVER()

------------------------------------------------------------

3. DATABASE SCHEMA

Tables Used:
- customers
- products
- sales

Relationships:
- One customer can have many sales
- One product can have many sales

ER Diagram Location:
screenshots/ERD_window_assignment.png

------------------------------------------------------------

4. PART A – SQL JOINS

Each JOIN query has a screenshot showing execution and result in the screenshot file.

INNER JOIN
Purpose: Retrieve transactions with valid customers and products.
Interpretation:
This query returns only records where both customer and product exist, ensuring valid transactions.

LEFT JOIN
Purpose: Identify customers who never purchased.
Interpretation:
Customers with NULL sales values represent customers with no transactions.

RIGHT JOIN
Purpose: Identify products with no sales.
Interpretation:
Products with NULL sale values indicate items that have not been sold.

FULL OUTER JOIN
Purpose: Display matched and unmatched customers and products.
Interpretation:
Shows complete coverage of customers and products, including missing matches.

SELF JOIN
Purpose: Compare customers within the same region.
Interpretation:
Pairs customers belonging to the same region for comparison.

------------------------------------------------------------

5. PART B – WINDOW FUNCTIONS
Screenshots Location:
screenshots/window_functions/

Ranking Functions (RANK)
Interpretation:
Products are ranked by quantity sold to identify top performers.

Aggregate Window Functions (SUM, AVG)
Interpretation:
Running totals show cumulative sales, while averages highlight trends.

Navigation Functions (LAG)
Interpretation:
Displays previous sales values to observe growth or decline.

Distribution Functions (NTILE)
Interpretation:
Customers are divided into four groups based on purchase volume.

------------------------------------------------------------

6. RESULTS ANALYSIS

Descriptive:
Certain products and customers generate higher sales.

Diagnostic:
High demand and pricing strategies influence better performance.

Prescriptive:
Promote high-performing products and improve low-performing ones.

------------------------------------------------------------

7. REPOSITORY STRUCTURE

plsql_window_functions_[studentId]_[firstname]
|-- sql
|   |-- joins.sql
|   |-- window_functions.sql
|
|-- screenshots
|   |-- ERD_window_assignment.png
|   |-- joins
|   |-- window_functions


------------------------------------------------------------

8. REFERENCES

PostgreSQL Documentation
W3Schools SQL Tutorial
Mode Analytics SQL Window Functions

------------------------------------------------------------

9. INTEGRITY STATEMENT

All sources were properly cited. Implementations and analysis represent original work. No AI-generated content was copied without attribution or adaptation.

