Simulating F1's physical database via multiple Excel files, this project aims to migrate F1's data from a physical database into a cloud-based database. The cloud-based database we are using is Snowflake. We have chosen Snowflake as it has a wide range of benifits, with easy scalability, fast performance, role based access implementation and can be easily connected to other applications such as GitHub and Power BI.

This repository contains all the SQL codes our team has used for the migration of F1's data into Snowflake, the transformation process (ELT), the Continuous Integration and Continuous Deployment pipeline (CI/CD), Role Based Access Control and Dynamic Tables for Power BI. It also contains the Excel files used to mimic the F1 database.

To navigate the repository easily, below are what each folder contains.

The Creating Database folder contains the SQL code used to create the 4 tables we came up with when changing the database from an Online Transactional Processing database system to a Online Analytical Processing database system.

The Dynamic Tables folder contains the SQL code used to create the 4 dynamic tables to be used in Power BI.

The repo folder here is purely used to test if the Snowflake and GitHub integration works, it is not related to any database code at all.
