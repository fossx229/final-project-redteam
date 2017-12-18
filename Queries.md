# Neo4j Cypher Queries

Here is a list of our queries we created in conjunction with our data model.

* (1) Find average ticket price per date (can be modified to count # of tickets per date)

MATCH (t:Ticket)-[:ASSIGN]->(f:Flight)
RETURN f.date, avg(t.price);

* (2) Return all flights

Match (f:Flight)
Return f;

* (3) Return average ticket price of destination airports

MATCH (f:Flight)-[:ORIGIN]-(a:Airport)
WITH f
MATCH (t:Ticket)-[:ASSIGN]-(f)-[:DESTINATION]-(d:Airport)
RETURN d.name, avg(t.price) AS average ORDER BY average DESC;

* (4) Convert the distance of all flights from airline 19977 to kilometers

MATCH (t:Ticket)
RETURN
[(t)-[:ASSIGN]->(f:Flight) WHERE f.airline CONTAINS '19977' | f.distance * 1.60934] as km_distance

* (5) Add a label to thanksgiving (eve) flights

MATCH (f:Flight) WHERE f.date =~ '11/30/2015.*'
SET f :Thanksgiving
RETURN f

* (6) Return the prices of flights with the new thanksgiving label

MATCH (f:Thanksgiving:Flight)<-[ASSIGN]-(t:Ticket) RETURN t.price;
