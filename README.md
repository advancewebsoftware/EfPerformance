# Entity Framework Performance
EF Performance
Check EF perfornace for  Bulk Insertion of records in SQL Server database.

Here We have listed a various way of Inserting bulkd records in database

Case 1:
//Add recrods to context and SaveChanges inside loop

Case 2:
//Add and SaveChanges inside loop with new DbContext for every operation

Case 3:
//Add inside loop, SaveChanges outside loop

Case 4:
//Add inside loop, SaveChanges outside loop, AutoDetectionChangesEnabled = false

Case 5:
//Temporary list inside loop, AddRange at once outside loop, SaveChanges outside loop

Case 6:
//SqlBulkCopy
