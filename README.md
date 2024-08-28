# SQL

1. Oskars
2. Anna
3. Laila
4. Andrey

Delete where id = 3

1. Oskars
2. Anna
4. Andrey

Add Laila

1. Oskars
2. Anna
4. Andrey
5. Laila

Delete where id = 5

1. Oskars
2. Anna
4. Andrey

Add Laila again

1. Oskars
2. Anna
4. Andrey
6. Laila


CREATE TABLE, DROP TABLE

-- SELECT * FROM Pets WHERE Age<11 AND Kind='Dog'; // all pets whose age is < 11 and kind is dog 

-- SELECT * FROM Pets WHERE Name LIKE '%s%'; // all data from pets when name contains S // making name case sensitive (AND Name GLOB '*Si*');

-- SELECT * FROM Pets WHERE LENGTH(Name) =4 AND Name LIKE 'B%' AND SEX='female';

-- SELECT * FROM Pets GROUP BY Kind;

-- SELECT * FROM Pets ORDER BY Age DESC LIMIT 12; // Ordered by dscending age 

-- SELECT * FROM Pets WHERE Age < (SELECT AVG(8) FROM Pets);

-- SELECT * FROM Pets WHERE Length(Name) <5;

-- SELECT Pets.*, Owners.City // all from pets but only City from Owners

-- SELECT Pets.*, Owners.City FROM Pets LEFT JOIN Owners //  all from pets but only City from Owners, Pets and Owners table are joined

-- SELECT Pets.*, Owners.City FROM Pets LEFT JOIN Owners ON Pets.OwnerID = Owners.OwnerID // matching OwnerID in the Pets table with the ID in the owners table

-- SELECT Pets.*, Owners.City FROM Pets LEFT JOIN Owners ON Pets.OwnerID = Owners.OwnerID WHERE Owners.City = 'Flint';

-- SELECT Kind COUNT(*) AS Count FROM Pets GROUP BY Kind, ORDER BY Count DESC; // selecting only kinds and how many is in each kind (eg Birds = 242, Dogs = 113)

-- SELECT Owners.City COUNT(*) AS PetCount FROM Pets JOIN Owners ON Pets.OwnerID = Owners.OwnerID GROUP BY Owners.City ORDER BY PetCount DESC; // selecting the city of the owner, count of pets grouped by owners city in descending order

-- SELECT Pets.* FROM Pets LEFT JOIN Owners ON Pets.OwnerID = Owners.OwnerID WHERE Owners.OwnerID IS NULL; // list of all pets with no owners (anti-join)

-- SELECT Owners.* FROM Owners LEFT JOIN Pets ON Owners.OwnerID = Pets.OwnerID WHERE Pets.OwnerID IS NULL;// all owners who have no pets 

-- SELECT Sales.ProcedureCode SUM(Procedures.Price) AS TotalSales FROM Sales LEFT JOIN Procedures ON Sales.ProcedureCode = Procedure.ProcedureCode GROUP BY Sales.ProcedureCode ORDER BY TotalSales DESC; // Calculate the amount of sales by procedurecode

-- CREATE TABLE persons (id INTEGER PRIMARY KEY AUTOINCREMENT, name varchar); // automatically increments the id number

-- varchar == string

--  INSERT INTO persons (name) VALUES ('lilian'); // inserting name into the table 

-- 

-- fundamental basics of SQL operations
--
