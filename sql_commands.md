CREATE TABLE receipts (id INTEGER PRIMARY KEY, store TEXT, item TEXT, number_of_items INTEGER, price INTEGER, buy_date TEXT);

All the attributes from all the receipts
**answer**-- SELECT * FROM receipts;
The store and item names from all the receipts
**answer**-- SELECT store, item FROM receipts; 
All the attributes from all purchases made at Toys R Us
**answer**-- SELECT * FROM receipts WHERE store = "Toys R Us";
The item name of each purchase made at Strand.
**answer**-- SELECT item FROM receipts WHERE store = "Strand";
The total number of items Peter purchased
**answer**-- SELECT SUM(number_of_items) FROM receipts;
The total number of items purchased at Sears
**answer**-- SELECT SUM(number_of_items) FROM receipts WHERE store="Sears";
All the attributes of receipts where Peter bought multiple items.
**answer**-- SELECT * FROM receipts WHERE number_of_items > 1;
The average number of items purchased on a trip to JC Penny
**answer**-- SELECT AVG(number_of_items) FROM receipts WHERE store = "JC Penny";
Great, now add a new receipt representing the purchase of a single "Heatstreet Maple Bourbon", purchased for $40.99 at "Schnapps Haus" on the most recent fourth of July.
**answer**-- INSERT INTO receipts (store, item, number_of_items, price, buy_date) VALUES ("Schnapps Haus", "Heatstreet Maple Bourbon", 1, 40.99, "July 4 2014");