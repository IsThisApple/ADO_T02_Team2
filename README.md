Simulating F1's physical database via multiple Excel files, this project aims to migrate F1's data from a physical database into a cloud-based database. The cloud-based database we are using is Snowflake. We have chosen Snowflake as it has a wide range of benifits, with easy scalability, fast performance, role based access implementation and can be easily connected to other applications such as GitHub and Power BI. Addtionally, with the fucntionality of SnowSQL, we are able to easily do the ELT pipeline, transforming the data in Snowflake itself.

This repository contains all the SQL codes our team has used for the migration of F1's data into Snowflake, the transformation process (ELT), the Continuous Integration and Continuous Deployment pipeline (CI/CD), Role Based Access Control and Dynamic Tables for Power BI. It also contains the Excel files used to mimic the F1 database.

To navigate this repository easily, below are what each folder contains:

The Creating Database folder contains the SQL code used to create the 4 tables we came up with when changing the database from an Online Transactional Processing database system to a Online Analytical Processing database system.

The Dynamic Tables folder contains the SQL code used to create the 4 dynamic tables to be used in Power BI.

The Integrating GitHub folder contains the SQL code used to establish the CI/CD pipeline to integrate GitHub into Snowflake, allowing us to easily pull and push code into the repository through Snowflake itself.

The Original Database folder contains all the SQL code regarding the creation of the database to store the initial data to do transformation in Snowflake itself. This allows us to use the ELT pipeline efficiently.

The PowerBI Dashboards folder contains all the PowerBI dashboards we made using the newly created database. We did this by establishing a connnection to PowerBI and Snowflake via dynamic tables, allowing us to build visualisations using the data.

The Role Access folder contains all the SQL code regarding the creation of roles in Snowflake and granting them permissions to certain tables in Snowflake, allowing us to restrict access to our database. 

The repo folder is purely used to test if the Snowflake and GitHub integration works and it is not related to any SQL database code at all.

Additioanlly, each of these folders have their own README.md files for further in depth explanation of files in the folder, feel free to read them if there is any confusion.
