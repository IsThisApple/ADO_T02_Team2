The following .ipynb files stored here are the 4 new tables created for the new database. Since the database is meant to be built for helping the data analysts in F1, we need to create a new database to change data processing systems from Online Transactional Processing (OLTP) to Online Analytical Processing (OLAP). These new tables were created by joining tables from the original database.

Driver Table:

Grid Table:
- Key Definition
  - Defined the purpose of symbols used in comments (`/` for joining and `-` for removing nulls).
- Created and Populated Table
  - Created the `RAW3.F1_3.GRID_STATS` table.  
  - Joined data from `RAW3.F1_3.SPRINT_GRID` and `RAW3.F1_3.STARTING_GRIDS` based on matching `DRIVERCODE`, `YEAR`, and `GRAND_PRIX`.  
  - Selected specific fields from both tables to populate the new table.
- Cleaned Data
  - Deleted rows from `RAW3.F1_3.GRID_STATS` where any key field (e.g., `STARTING_POS`, `NO`, `DRIVER`, etc.) was `NULL`.
  - Updated the `SPRINT_TIME` column to replace `NULL` values with `'N/A'`.
- Validated Data
  - Verified the contents of `RAW3.F1_3.GRID_STATS` with `SELECT` queries after each step.
- Checked for Nulls
  - Counted rows with `NULL` values in any key field to ensure data integrity after cleaning.

Race Table
- Create and Populate RACE_TABLE
  - Created the RACE_TABLE using a combination of joins between the FASTEST_LAPS, FASTESTLAPS_DETAILED, QUALIFYINGS, and RACE_SUMMARIES tables.
  - Leveraged LEFT JOIN to merge data while ensuring all relevant information was included in the table, even when some datasets were incomplete.
  - Added logic to calculate the median of numeric columns (TIME and LAPS) and used the most frequent values for categorical columns (e.g., CAR, DRIVER,                DRIVERCODE, GRAND_PRIX) to handle missing values.
- Data Cleaning and Imputation
  - Imputed missing values in non-numeric columns with 'unknown'.
  - Replaced missing numeric values with -999 to act as a clear placeholder for filtering.
  - Set missing dates to '9999-12-31' to distinguish them from actual data.
  - Ensured consistency in TIME formatting by converting time values containing : to seconds.
- Primary and Foreign Key Constraints
  - Added a primary key constraint on YEAR, GRAND_PRIX, and DRIVERCODE to uniquely identify each record.
  - Established a foreign key constraint linking the DRIVER and YEAR columns in RACE_TABLE to the DRIVER_TABLE for data integrity.
- Validation and Verification
  - Checked for duplicate records and ensured the uniqueness of constraints by dropping and re-adding necessary keys.
  - Verified the final table using INFORMATION_SCHEMA.TABLE_CONSTRAINTS to confirm constraints were correctly implemented.
  - Selected data from RACE_TABLE to validate that all expected columns and rows were correctly populated and formatted.

Team Table:
- Create and Populate `TEAM_STATS` Table
  - Created the `TEAM_STATS` table using joins between two tables
  - Using left join, I joined the `CONSTRUCTOR_STANDINGS` to the `TEAM_DETAILS` table to populate the dataset while creating the new TEAM_STATS table
- Cleaned Data
  - Used `UPPER()` on `TEAM` column when joining the tables to ensure more consistency in properly mapping the respective values.
  - Check for nulls in the tables by selecting nulls in the database for each column.
  - Updated the null values in the `TEAM_OVERALL_POS` and `TOTAL_PTS` with their respective values from the original dataset as there were only 12 nulls and all of them belonged to the same year and team
- Validated Data
  - Check for nulls again by printing rows with nulls to ensure that the table does not contain any more null values
  - Showed the entire table using the `SELECT` query to ensure all the  columns are in the dataset
