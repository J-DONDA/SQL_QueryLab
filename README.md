<h1>SQL Query Lab</h1>

<h2>Description</h2>
In this lab simulation, I take on the role of a security professional at a large organization. Part of my job is to investigate security issues to help keep the system secure. I recently discovered some potential security issues that involve login attempts and employee machines. My task is to examine the organization’s data in their employees and log_in_attempts tables. I’ll utilize SQL filters to retrieve records from different datasets and investigate the potential security issues.
<br />


<h2>Languages and Utilities Used</h2>

- <b>SQL</b>

<h2>Environments Used </h2>

- <b>Linux</b> 

<h2>Program walk-through:</h2>


<b>Task 1.) Retrieve after hours failed login attempts:</b>

I recently discovered a potential security incident that occurred after business hours. To investigate this, I will run a query to review after hours login activity using SQL filters that identify all failed login attempts that occurred after 18:00. 

First, I ran a query to view all columns available within the log_in_attempts table to see what data I can filter with, this returned 200 login attempts in total, here are the first 5 for example: <br />

![image](https://github.com/J-DONDA/SQL_QueryLab/assets/116527248/80ea88b2-a4b7-4fdf-b5d8-f9a304daa6e5)

<br />

Next, I filtered down to view all failed login attempts after normal business hours:

![image](https://github.com/J-DONDA/SQL_QueryLab/assets/116527248/3e883fcb-0e9f-4931-9cbc-b8a30aeda6d7)

This shows that there were a total of 19 failed attempts in that timeframe.

<br />
<br />
<br />
<br />

<b>Task 2.) Retrieve login attempts on specific dates:</b>  <br />

A suspicious event occurred on 2022-05-09. To investigate this event, I will review all login attempts which occurred on this day and the day before. 
<br />

I ran a query, using the OR operator to pull in only the login attempts during the dates of 5/9/22 as well as 5/8/2022<br />

![image](https://github.com/J-DONDA/SQL_QueryLab/assets/116527248/9af89594-b82c-4053-9f33-4b703dd92dfc)

<br />
This returned 75 login attempts in total within the specified date range, (first 10 above) that can be targeted for further analysis.

<br />
<br />
<br />
<br />
<br />

<b>Task 3.) Retrieve login attempts originating outside of Mexico:</b> <br/>

There’s been suspicious activity with login attempts, but the team has determined that this activity didn't originate in Mexico. I will investigate all login attempts that occurred outside of Mexico.  

I ran a query using the NOT operator to exclude Mexico from the search results. Also, since Mexico is represented as both “MEX” as well as “MEXICO” in the data, I used the LIKE operator combined with the % wildcard to exclude any country starting with the string of “MEX”<br />

![image](https://github.com/J-DONDA/SQL_QueryLab/assets/116527248/db4bd98d-0184-4002-9185-b23c4627976d)

<br />
This returned 144 login attempts that can now be further examined, excluding all attempts originating from Mexico. The first 10 are captured in the screenshot above.

<br />
<br />
<br />
<br />
<br />

<b>Task 4.) Retrieve employees in Marketing:</b>  <br />

My team wants to perform security updates on specific employee machines in the Marketing department. I’m responsible for getting information on these employee machines and will need to query the employees table.

First, I ran a basic query using the SELECT * (select all) operator to view all rows/columns/data available within the employees table: <br />

![image](https://github.com/J-DONDA/SQL_QueryLab/assets/116527248/0e9872a0-78a4-4c65-9c5a-e26e013f9538)

<br />
This returned a total of 200 employees, (first 10 above) and allowed me to view the 5 available columns I have to filter with: employee_id, devide_id, username, department, and office.

<br />
<br />
<br />
<br />
<br />

<b> Task 5.) Retrieve employees in Finance or Sales:</b>  <br/>

My team now needs to perform a different security update on machines for employees in the Sales and Finance departments. I will need to identify all employees in the Sales or Finance departments. 

I ran a query using the OR operator to filter for only employees within the Finance or Sales departments:  <br />

![image](https://github.com/J-DONDA/SQL_QueryLab/assets/116527248/96bd9cb3-4828-464d-8716-082282681bcf)

<br />
This returned 71 employees in total (first 10 above) within either the Finance or Sales departments that will need to recieve the update.

<br />
<br />
<br />
<br />
<br />

<b> Task 6.) Retrieve all employees not in IT:</b>  <br/>

My team needs to make one more update to employee machines. The employees who are in the Information Technology department already had this update, but employees in all other departments need it. I will need to identify all employees that are not in the IT department. 

I ran a query using the NOT operator to exclude all employees listed within the Information Technology department:  <br />

![image](https://github.com/J-DONDA/SQL_QueryLab/assets/116527248/662fd1d8-6bc8-42f2-bb28-e3e20724018e)

<br />
This returned a total of 161 employees from all deparments, excluding the Information Technology department, that will need the update.

<br />
<br />
<br />
<br />
<br />

<b> Summary:</b>  <br/>

Based on the various scenarios provided, I was able to successfully craft a multitude of SQL queries with specific filtering operators in place. These filtered queries helped to efficiently target only the relevant data needed for further analysis of each potential security incident.
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
