# Ahamazon Database

## Objectives
Upon completion of this assignment, you should be able to:

a. Construct an entity-relationship model at a conceptual level.\
b. Map the model into a schema of a relational DBMS.\
c. Implement the given schema on a relational DBMS.\
d. Use a database language (SQL) to retrieve data from a relational DBMS.


## Introduction
This assignment focuses on data modeling, database design, and implementation from a user's perspective. It involves modeling and implementation aspects of the database course. The objective is to develop an application based on a given data model using a specified database management system (DBMS).


## Application Description
Suppose you are asked to construct a database for Ahamazon, a hardcopy book and magazine supplier hosting an e-commerce website. The requirements are as follows:

1. Ahamazon supplies publications (books and magazines) to many bookstores. These bookstores are hosted on Ahamazon’s website. Each bookstore has a unique company ID. Each bookstore sells a selection of publications, each of which has a publication ID, year of publication, publisher, selling price, and quantity in stock. For a book publication, there is a book title. A magazine publication has an issue number in addition to a magazine title.

2. Each bookstore gives a unique ID to each publication it sells. The same publication may have different IDs under different bookstores. The same publication can be sold at multiple bookstores at difference prices. In addition, the price of a publication in a bookstore may change over time. We need to record the history of price changes.

3. Ahamazon’s website allows customers to place purchase orders. Each customer has an ID and a name. Each order has an ID and timestamp. Each order has one or more publications, which could be from different bookstores. For each publication in a purchase order, its price and quantity are recorded. Each order has a total shipping cost and a shipping address.

4. After a purchase order has been submitted, the customer may track the status of the order on Ahamazon’s website. Initially, the status of each publication in the order is shown to be “being processed”. After the respective bookstore ships the publication, the status is be changed to “shipped”. Once a publication is delivered to the customer (as reported by the courier), the status is changed to “delivered”, and the delivery date is recorded. Within 30 days from the delivery date of a publication, the customer may return the publication for a refund. Once the bookstore refunds the publication, its status is changed to “returned”.

5. After a customer purchases a publication, he/she is allowed to rate and comment on the publication once. There are five possible ratings: 1, 2, 3, 4, and 5, with 5 being the highest. The average rating for a publication, as well as the number of users that have rated the publication, are shown on the web page that displays the publication information to customers. In addition, a customer can modify his/her ratings and comments anytime.

6. Ahamazon customers are allowed to file complaints on any publication and bookstore. For example, if a customer did not receive a publication whose status is “delivered”, he/she can file a complaint to Ahamazon. If he/she is not happy about a certain bookstore, he/she can file a complaint. After a complaint is filed, the customer can check the status of his/her complaint. Initially, the status of the complaint is set to “pending”. After the complaint is picked up by a Ahamazon employee, the status is changed to “being handled”, and the name of the employee is shown. Once the complaint is addressed, its status is changed to “addressed”.

7. Ahamazon has a number of employees that handles complaints from users. Each employee has an ID, a name, and a monthly salary. Each complaint is handled by one employee.

8. The database should support the queries listed below. Note that the information above may not be complete. Some aspects of the database application’s details may have been omitted. It is expected that you come up with their own solution(s) in case of inconsistencies or missing information. However, you have to keep track of these aspects and explain your assumptions in your submitted report. Extensions to the implementation of the basic system are encouraged.


## Queries

1. Find the average price of “Harry Porter Finale” on Ahamazon from 1 August 2022 to 31 August 2022.
2. Find publications that received at least 10 ratings of “5” in August 2022, and rank them by their average
ratings.
3. For all publications purchased in June 2022 that have been delivered, find the average time from the
ordering date to the delivery date.
4. Let us define the “latency” of an employee by the average that he/she takes to process a complaint.
Find the employee with the smallest latency.
5. Produce a list that contains (i) all publications published by Nanyang Publisher Company, and (ii) for
each of them, the number of bookstores on Ahamazon that sell them.
6. Find bookstores that made the most revenue in August 2022.
7. For customers that made the most number of complaints, find the most expensive publication he/she
has ever purchased.
8. Find publications that have never been purchased by any customer in July 2022, but are the top 3
most purchased publications in August 2022.
9. Find publications that are increasingly being purchased over at least 3 months.
