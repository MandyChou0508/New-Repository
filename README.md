<h2>Project: Advanced SQL</h2>

Database Used in this Lab
Mysql_learners database has been used in this lab.

<h3>Create a database</h3>
Downloaded the datasets available in ‘.sql ‘ format and imported all the tables one by one in MySQL database ‘Mysql_Learners’ by running the SQL script.<br>
<img width="346" alt="截圖 2025-03-02 19 31 15" src="https://github.com/user-attachments/assets/b3a4db37-9113-4480-9532-808938e83e3b" /><br>
<h3>Exercise 1: Using Joins</h3>
You have been asked to produce some reports about the communities and crimes in the Chicago area.<br>
<h4>Question 1: <br>
Write and execute a SQL query to list the school names, community names and average attendance for communities with a hardship index of 98.</h4><br>
<img width="916" alt="ex-1:q-1" src="https://github.com/user-attachments/assets/7b9e4852-f2dc-4755-9855-385f955e0a40" />
<h4>Question 2: <br>
Write and execute a SQL query to list all crimes that took place at a school. Include case number, crime type and community name.</h4><br>
<img width="1087" alt="ex-1:q-2" src="https://github.com/user-attachments/assets/5ec02b0d-0479-4b47-9860-f90153a97b78" />
<h3>Exercise 2: Creating a View</h3>
For privacy reasons, you have been asked to create a view that enables users to select just the school name and the icon fields from the CHICAGO_PUBLIC_SCHOOLS table. By providing a view, you can ensure that users cannot see the actual scores given to a school, just the icon associated with their score. You should define new names for the view columns to obscure the use of scores and icons in the original table.
<h4>Question 1: <br>
Write and execute a SQL statement to create a view showing the columns listed in the following table, with new column names as shown in the second column.<br>
<img width="526" alt="截圖 2025-03-02 21 07 32" src="https://github.com/user-attachments/assets/ef4a5a2f-4cf5-4433-a24b-26d899a3b262" /><br>
Write and execute a SQL statement that returns all of the columns from the view.<br><br>
<img width="1347" alt="ex2-1" src="https://github.com/user-attachments/assets/08c6954e-3f65-45c9-a825-5bbe97c9e662" /><br><br>
Write and execute a SQL statement that returns just the school name and leaders rating from the view.<br><br>
<img width="669" alt="ex-2-2" src="https://github.com/user-attachments/assets/bf21b969-2a32-4b67-ba80-72a23b83dc6c" /><br><br>
<h3>Exercise 3: Creating a Stored Procedure</h3>
The icon fields are calculated based on the value in the corresponding score field. You need to make sure that when a score field is updated, the icon field is updated too. To do this, you will write a stored procedure that receives the school id and a leaders score as input parameters, calculates the icon setting and updates the fields appropriately.
<h4>Question 1: <br>
Write the structure of a query to create or replace a stored procedure called UPDATE_LEADERS_SCORE that takes a in_School_ID parameter as an integer and a in_Leader_Score parameter as an integer.<br><br>
Inside your stored procedure, write a SQL statement to update the Leaders_Score field in the CHICAGO_PUBLIC_SCHOOLS table for the school identified by in_School_ID to the value in the in_Leader_Score parameter.<br><br>
<img width="907" alt="ex3-1" src="https://github.com/user-attachments/assets/e22be8ec-367b-4f87-ae3b-5dcaa4ab61ab" /><br>
<img width="314" alt="截圖 2025-03-02 21 48 29" src="https://github.com/user-attachments/assets/ffcaa8d8-8fb2-431b-abd4-19a2da5412d0" />
<h4>Question 2: <br>
Inside your stored procedure, write a SQL IF statement to update the Leaders_Icon field in the CHICAGO_PUBLIC_SCHOOLS table for the school identified by in_School_ID using the following information.<br><br>
<img width="385" alt="截圖 2025-03-02 21 17 15" src="https://github.com/user-attachments/assets/a8ea5ca1-57cf-412b-86d5-1d4a25f1b357" />
<img width="586" alt="ex3-3" src="https://github.com/user-attachments/assets/14fac5f1-ad7b-4386-b89f-e07e57d60667" />
<h4>Question 3: <br>
Run your code to create the stored procedure.<br><br>
Write a query to call the stored procedure, passing a valid school ID and a leader score of 50, to check that the procedure works as expected.<br><br>
<img width="662" alt="ex3-4" src="https://github.com/user-attachments/assets/3f47f982-68e9-4c85-8d57-89ca6df07b00" />
<h3>Exercise 4: Using Transactions</h3>
You realise that if someone calls your code with a score outside of the allowed range (0-99), then the score will be updated with the invalid data and the icon will remain at its previous value. There are various ways to avoid this problem, one of which is using a transaction.
<h4>Question 1: <br>
Update your stored procedure definition. Add a generic ELSE clause to the IF statement that rolls back the current work if the score did not fit any of the preceding categories.<br><br>
Update your stored procedure definition again. Add a statement to commit the current unit of work at the end of the procedure.<br><br>
<img width="608" alt="截圖 2025-03-02 01 18 32" src="https://github.com/user-attachments/assets/91f23b22-7cfc-4a2b-97b7-5205f38aaf5c" />
<h4>Question 1: <br>
Write and run one query to check that the updated stored procedure works as expected when you use a valid score of 38.<br><br>
<img width="275" alt="截圖 2025-03-02 01 19 41" src="https://github.com/user-attachments/assets/feb0d1b1-3403-4f80-abef-d9ff997b4ea1" /><br><br>
Write and run another query to check that the updated stored procedure works as expected when you use an invalid score of 101.<br><br>
<img width="531" alt="截圖 2025-03-02 21 51 50" src="https://github.com/user-attachments/assets/ce63ffa3-6499-4260-bc53-b6a338812bc7" />
<img width="275" alt="截圖 2025-03-02 01 19 41" src="https://github.com/user-attachments/assets/4e9c0d8a-537e-4952-bcc7-458b013ce5d3" /><br><br>
When I provided a score of 101 to the function it ran successfully but no changes were made.










