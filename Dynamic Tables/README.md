These are the SQL codes used to create the dynamic tables to be connected to Power BI. We chose dynamic tables over the star schema as our dataset does not have any IDs we can use to identify each record uniquely. This means that implementing a star schema require us to create IDs for all the drivers and races for each year, of which the timeframe given would not allow us to do so.

Therefore, dyanmic tables were implemented. 

Dynamic tables are not only easy to create but to use and connect to other visualization softwares. When new data gets inserted or data get updated, dyanmic tables would get updated as well.  Unlike the star schema system the advantage is that we are able to update our database in real time. This could allow for streamline real time analysis which a nesscary step for the F1 company since in competitions are held year having the ease of use of the dynamic table would make our database feel like ahead of its time. 
