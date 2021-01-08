# Order-Delivery-Django-Application

APPLICATION DESCRIPTION

The AppLine application allows a user to enter and place a order or a delivery for a fictional Medication Warehouse

Firstly, the user searches the item name and the warehouse name from the list of available item names and warehouse names in database. 
After submission, the user is redirected to the page where he can select, from the list of items and warehouses that correspond to his search, the ones that he is interested in. 
After specifying the quantity and the request type (order/delivery) he can submit his request. 

Order line cases:
•If there is item  at the selected warehouse  the request is accepted and the corresponding stock is decreased. 
The user receives adequate message. 
•If there is no item at the selected warehouse, the request is not accepted, and the stock remains unchanged. 
The result message displays additionally the table with the warehouses where the selected item is available.
•In case of “insufficient stock” the request is not accepted, and the stock remains unchanged. 
The result message also displays the table with the warehouses where the selected item in requested quantity is available.
•If the ordered quantity is equal to the quantity in the selected warehouse, the request is accepted.
The row in stock table that corresponds to the selected item and warehouse is deleted.

The delivery line is always accepted, and the corresponding stock is increased.The user receives the adequate massage. 
If the selected item does not exist in the selected warehouse, the new, corresponding row is created in Stock table.


MACHINE SETUP

The application required POSTGRES (https://www.pgadmin.org/download), containing the necessary tables Item, Stock and Warehouse 
(files Schema.sql, Item.sql, Warehouse.sql, Stock.sql). It requires as well Python3 and its Django library. 
