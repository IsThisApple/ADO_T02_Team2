The following .ipynb files stored here are the 4 new tables created for the new database. Since the database is meant to be built for helping the data analysts in F1, we need to create a new database to change data processing systems from Online Transactional Processing (OLTP) to Online Analytical Processing (OLAP). These new tables were created by joining tables from the original database.

Driver Table:

Grid Table:
1. Key Definition
  - Defined the purpose of symbols used in comments (`/` for joining and `-` for removing nulls).
2. Created and Populated Table
  - Created the `RAW3.F1_3.GRID_STATS` table.  
  - Joined data from `RAW3.F1_3.SPRINT_GRID` and `RAW3.F1_3.STARTING_GRIDS` based on matching `DRIVERCODE`, `YEAR`, and `GRAND_PRIX`.  
  - Selected specific fields from both tables to populate the new table.
3. Cleaned Data
  - Deleted rows from `RAW3.F1_3.GRID_STATS` where any key field (e.g., `STARTING_POS`, `NO`, `DRIVER`, etc.) was `NULL`.
  - Updated the `SPRINT_TIME` column to replace `NULL` values with `'N/A'`.
4. Validated Data
  - Verified the contents of `RAW3.F1_3.GRID_STATS` with `SELECT` queries after each step.
5. Checked for Nulls
  - Counted rows with `NULL` values in any key field to ensure data integrity after cleaning.

Race Table:

Team Table:
1. Create and Populate TEAM_STATS Table
  - Created the TEAM_STATS table using joins between two tables
  - Using left join, I joined the CONSTRUCTOR_STANDINGS to the TEAM_DETAILS table to populate the dataset while creating the new TEAM_STATS table
2. Cleaned Data
  - Used UPPER() on TEAM column when joining the tables to ensure more consistency in properly mapping the respective values.
  - Check for nulls in the tables by selecting nulls in the database for each column.
  - Updated the null values in the TEAM_OVERALL_POS and TOTAL_PTS with their respective values from the original dataset as there were only 12 nulls and all of them belonged to the same year and team
3. Validated Data
  - Check for nulls again by printing rows with nulls to ensure that the table does not contain any more null values
  - Showed the entire table using the 'SELECT' query to ensure all the  columns are in the dataset
