# Data Structures Capstone: Bacon Number BFS

An actor's **Bacon Number** is the number of degrees of separation they are from Kevin Bacon.

For example, Kevin Bacon's Bacon number is 0. If an actor works in a movie with Kevin Bacon, the actor's Bacon number is 1. 
If an actor works with an actor who worked with Kevin Bacon in a movie, the first actor's Bacon number is 2, and so forth.

Feel free to play with the [Oracle of Bacon](https://oracleofbacon.org) and read the *How* section to get an overview of the project.

IMDB maintains several updated lists of data as TSV (Tab Separated Values) files for all of its actors, movies/tv shows and how they relate.
[IMDB Databases](https://www.imdb.com/interfaces/)

We want the databases that contain lists of actors with all movies that they have been in, 
and the list of all movies with principal actors in each movie.

You will create a graph data structure that stores two types of nodes: Actor Nodes and Movie Nodes

You will read in all actors and movies from the tsv files to populate the graphs and then allow the user to query the database for:

1. An actor's Bacon number
2. An actor's ACTOR number (give a second actor- ACTOR)
3. The Average Bacon number of all actors
4. The Hollywood number (average ACTOR number across all actors)

You may want to calculate the last two values only once and save them in a cache (persistent data file)

## REQUIREMENTS:
### 1. (1 pts) Download the appropriate TSV files. (Suggestion: DO NOT OPEN IN TEXT EDIT YIKES)
### 2. (1 pts) Explore the format of the TSV files using terminal commands:
```
head -50 MYFIRSTTSV.tsv
head -50 MYFIRSTTSV.tsv | grep -Eo "YOURREGEX"
head -50 MYFIRSTTSV.tsv | grep -Eoc "YOURREGEX"
grep -Eoc "BACONNCONST" MYFIRSTTSV.tsv
```
You should answer the following questions to figure out how to read and process these data files (put answers in Github README)
  *   What are tconst and nconst and how are they formatted in the files? 
  *   Can you get the list of movies for each actor, and the list of actors for each movie? How are these lists formatted?
  *   How many times does Kevin Bacon's nconst appear in the database files for actors? for movies?

### 3. (5 pts)Create a GraphNode class for graph nodes and two sub classes- ActorNodes and MovieNodes
  * Actor Nodes should contain zero or more Movie Node pointers and keep track of their nconst and any other data you see fit.
  * Movie Nodes should contain zero or more Actor Node pointers and keep track of their tconst and any other data you see fit.
  
### 4. (3 pts) Create a Bi-Partite Graph class that stores ActorNodes and MovieNodes. 
You should be able to add a Node to the graph by passing in some details about the node to be created, and have the Graph create either
an Actor or Movie node as appropriate.

#### YOUR DECISION: How to store ActorNodes and MovieNodes in the graph? 
* You will need to search through Actor nodes to accomplish the ACTOR number query
* You will need to search and iterate through Actors to accomplish the Hollywood number query
* Your most common query will most likely be from Kevin Bacon to another actor.

### Required Methods: (10 pts)
```java 
public void addActor(<arguments for you to determine>)
public void addMovie(<arguments for you to determine>)
private int BFS(String actor, String target) \\returns the degrees of separation between actor and target
public int calculateNumber(String actor) \\calculates the Bacon number of an actor using Breadth First Search
public int calculateNumber(String actor, String targetActor) \\calculates the degrees of separation between the actor and targetActor using Breadth First Search
```
### Challenge Methods:(2.5 pts each)
```java
int calculateAvgBacon() \\calculates the average Bacon number across all actors
int calculateAvgHollyWood(String actor) \\calculates the average degrees of separation between the actor and all other actors 
```
### Optional Bonus Method: (up to 2 replacement points for other missed points)
```java
ArrayList<String> centralActors() \\Sorts actors by their Hollywood number and returns the top 10 lowest
```
4. (5 pts.) Driver: Read in all actors and movies from the .tsv file and add them to the graph.
5. (5 pts.) Driver: Perform required calculations for the user. (Consider caching their queries to make your program run faster)
6. (5 pts.) Analyse runtime for all methods attempted and write analysis in comments above each method. 


