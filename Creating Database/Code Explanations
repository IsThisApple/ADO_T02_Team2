Driver Table:
1. Primary Keys and foreign keys
- primary key i made the driver year and grand prix as the primary key so that the key is more precise and unique
- foreign keys is the same because there are the same columns in other tables as well
2. Creating of the driver table
- joined the tables on driver, year, grand_prix, car, race position in total
- This were the columns that were being used to join the tables
- This allowed the data to have a reasonable number of columns in the dataset with some null values that will be dealt with later on
- Made sure that the data has reasonable number of rows so that there wont be too many or too little due to insufficient joining of tables
3. Cleaning of the data
- For the numerical columns such as time, year etc, I used -999 so that it is an extreme value and can be easily filtered out in the future
- we did not want to use the median or mean to impute the null values because we did not want to impute the wrong values to show the wrong data
- For the categorical columns, the null values were imputed with a 'unknown'. Same reason as before, we did not want to show incorrect values.
4. Null values and checking values
- Select statement has been put at the bottom of the code so that when it has been ran, the output shows the overall details of the data in the new window popup
below showing all the unqiue values and seeing if there is any more null values in the dataset. 


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
