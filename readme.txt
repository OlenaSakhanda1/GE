1. Setup GE on your computer
$pip install great_expectations
2. Clone this repository
3. Open cmd in this repository
4. To create your own project you need to use command 
$great_expectations init
5. Change great_expectations.yml to connect with your database (datasources block)
6. If you want to open this project use files in current repository
7. In the folder expectations you can find lena_test.json with current expectations. They were created with the command
$great_expectations suite new -p
8. To edit them we can use command
$great_expectations suite edit test_auto
9. You can see results (\great_expectations\uncommitted\data_docs\local_site\index.html) that were created with the command
$great_expectations docs build
10. To create checkpoint we can use notebook that is using for creating suite (file->>save and checkpoint) or use command
$great_expectations checkpoint new <your_checkpoint_name>
\great_expectations\checkpoints\ls1.yml
11. The table Product was modified in such way:
  UPDATE [AdventureWorks2012].[Production].[Product]
SET 
    color = 'Blackko'
WHERE
    ProductID = 317;

  UPDATE [AdventureWorks2012].[Production].[Product]
SET 
    SafetyStockLevel = 1
WHERE
    ProductID = 1;

  UPDATE [AdventureWorks2012].[Production].[Product]
SET 
    [ModifiedDate] = '2044-02-08 10:01:36.827'
WHERE
    ProductID = 3;



