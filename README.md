# ASSINMENT-ISHIMWE-ERIC--27744

Here is the concise, high-scoring answer for Step 1: Problem Definition of your assignment, covering all required elements for a Mastery Project.

Step 1: Problem Definition (2 pts)
Business Context
East African E-Retail is an e-commerce platform operating in the Retail industry across two key regions: Kigali and Musanze.

Data Challenge
The current static sales reports fail to provide the dynamic analytical insights needed to optimize operations, requiring advanced analysis using Window Functions to find regional product performance, measure sales volatility, and segment high-value customers.

Expected Outcome
To achieve data-driven decision-making by providing actionable insights for inventory optimization, precise financial forecasting, and the launch of a segmented customer loyalty program.

Success Criteria


1. Top 5 products per region/quarter → `RANK()`**This will show top products per region per month.**<img width="1190" height="876" alt="image" src="https://github.com/user-attachments/assets/6b0b4852-632e-4c3a-a18c-eb470a762e06" />

 
3. Running monthly sales totals per region → `SUM() OVER()`;**calculate running monthly sales totals per region**<img width="1153" height="748" alt="image" src="https://github.com/user-attachments/assets/aa77bbb2-b748-46bb-a83b-9937da6d6352" />

4. Month-over-month growth → `LAG()` / `LEAD()**`are perfect for calculating month-over-month (MoM) growth**<img width="1171" height="847" alt="image" src="https://github.com/user-attachments/assets/d6c181e4-10ab-4fb9-adf1-603804e864ca" />

5. Customer quartiles → `NTILE(4)`; **divide customers into quartiles based on total spending**<img width="873" height="701" alt="image" src="https://github.com/user-attachments/assets/1f79e438-fc58-44fc-9946-0e1246a92d78" />

6. 3-month moving averages → `AVG() OVER()`;**calculate a 3-month moving average**<img width="868" height="889" alt="image" src="https://github.com/user-attachments/assets/85890a1d-93db-4864-b67e-4ee17814ed57" />



##  Database Schema
### Tables
- **customers**: customer_id (PK), name, email, region
- <img width="1158" height="294" alt="image" src="https://github.com/user-attachments/assets/a3dec9ef-9566-49c7-85d5-365d426e2657" />
  
- **products**: product_id (PK), name, category, unit_price
- <img width="1231" height="302" alt="image" src="https://github.com/user-attachments/assets/350c85f8-83f7-4428-83f3-81262720c2c6" />
 
- **transactions**: transaction_id (PK), customer_id (FK), product_id (FK), sale_date, quantity, amount
- <img width="1235" height="427" alt="image" src="https://github.com/user-attachments/assets/a28f6c7b-1242-487b-8db9-ec7bd9bcdedf" />


### ER Diagram
<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/f5285382-72b3-40aa-87ca-77c8b2055246" />
