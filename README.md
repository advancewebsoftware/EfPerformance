# Entity Framework Performance

Check EF perfornace for  Bulk Insertion of records in SQL Server database.

Here We have listed a various way of Inserting bulkd records in database

**Case 1:**  Add recrods to context and SaveChanges inside loop

**Case 2:**
Add and SaveChanges inside loop with new DbContext for every operation

**Case 3:**
Add inside loop, SaveChanges outside loop

**Case 4:** **Recommended : You may get significant performance improvements by turning it off**

Add inside loop, SaveChanges outside loop, AutoDetectionChangesEnabled = false
 
**AutoDetectionChangesEnabled = false** : This code avoids unnecessary calls to DetectChanges that would have occurred while calling the DbSet.Add and SaveChanges methods.

**Case 5:** **Recommended** 

Temporary list inside loop, AddRange at once outside loop, SaveChanges outside loop

**Case 6:** **Recommended If you are trying to insert large amount of data** 

SqlBulkCopy
