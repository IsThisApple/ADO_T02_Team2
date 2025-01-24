RABC also known as the Role based control for the dataset.
For the RBAC i would set the roles in this following heirarchy, which is analyst, developer and CI
analyst would be the lowest role on the RBAC only being allowed to access the dynamic tables created in sprint 5 
originally, the analyst role was able to view all the tables and not able to insert, update or delete any infomation on the table.
After the implementation of the dynamic tables, the access of the analyst role is in this current state. 

Next on the heirachy of the roles is developer. The current access of the develop is everything the analyst can do plus, the developer can view all the tables and the dynamic tables.Notonly that the develop can insert new rows into the tables updating the dynamic tables with each new entry. 

Next on the heriachy of the roles before the account admin, is the CI role. The CI role is the higher teir than a developer and it has access of both the developer and analyst. The new access for the CI is that the CI is able to update the data of the role and delete rows if needed. The reason for the access is that since the CI has a high access, the person with the CI is most trusted and experience would not easily delete the whole database. 
