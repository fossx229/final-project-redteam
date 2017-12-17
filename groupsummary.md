# Group Summary


## Description

Our project was to provide a broad overview of Neo4j which described how it is used, its capabilities, its internal architecture,
how it is similar and dissimliar to both RDBMS (MariaDB) and Document Oriented (MongoDB) database technologies, and provide
some of its advantages and disadvantages of using it compared to other options. This was accomplished in the form of a
paper which contains sections to address these topics.

## Goals

Our goals were mostly to discuss the above aspects with sufficient depth, which we feel that we achived. We had originally
wanted to discuss a rest api aspect to neo4j, but ultimately decided to explore other areas in more depth.
Another goal which was not attained was to time Neo4j and MariaDB at joining tasks using interrelated tables
described on the Neo4j site, but we were having difficulty importing a large and randomized data set into Neo4j.
Finally, we would have liked our data model to be based on the content of Stack Overflow (all of the current users, tags,
and post history would be represented) but due to a combination of outdated documentation and difficulty installing
required libraries, we decided to use a different model.

## Data Model

Our data model was sourced from the Neo4j website, and is available here https://neo4j.com/graphgist/flight-analyzer
Pictured below is an abstract representation of the model.

![Screenshot](datamodel.png)

As you can see, there are three basic entities: Flights, Airports, and Tickets which are modeled by nodes.
In terms of relationships, Flights have origin and destination of Airports, and Tickets are assigned to Flights.

## Future Work

Hypothetically, we think there is room to continue work on our project, but practically we don't think we will continue.
For instance, security measures are an area we think we could have touched more on. It also would have been cool
to analyze specific queries and describe what was going on behind the scenes internally.

## Overall Reaction

In retrospect, we both feel that we would have preferred working on an actual implementation project rather than a paper.
An implementation project, depending on how well we did, would have more potential to include in a portfolio for 
employers and could also (perhaps) help us to absorb and retain the material better. We thought we were probably too
general in certain sections, which led to an overlap of content for some of the sections we were indvidually responsible for,
so we think being more specific about what our responsibilities were could have been beneficial. Related to this,
we probably should have communicated better about how individual tasks of the project were going in case our
expectations needed to change earlier. Overall though, we do think that this project greatly increased our familiarity with Neo4j
and also helped us revisit many (especially general) concepts from earlier in the course.
