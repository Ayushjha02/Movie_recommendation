Movie Recommendation System using Neo4j and NLP
Overview

This project builds a graph-based movie recommendation system using Neo4j. It processes Bollywood movie data, extracts keywords using NLP, and models relationships between movies, actors, directors, and keywords for recommendation.

Dataset
Bollywood movie dataset (CSV)
Features include:
Movie title, year, runtime
IMDB rating, votes
Actors, directors
Plot description
Data Preprocessing
Removed unnecessary columns
Handled missing values
Converted ratings and votes to numeric format
Split actors and directors into structured lists
Extracted keywords from plot descriptions using YAKE
Graph Data Model

Nodes:

Movie
Actor
Director
Keyword

Relationships:

Movie → Actor (ACTED_BY)
Actor → Movie (ACTED_IN)
Movie → Director (DIRECTED_BY)
Movie → Keyword (HAS_KEYWORD)
Implementation Steps
Cleaned and transformed raw dataset
Created separate CSV files for nodes and relationships
Connected to Neo4j database
Loaded data into Neo4j using Cypher queries
Created nodes and relationships using MERGE
Verified graph using node and relationship counts
Recommendation Logic
Actor-based recommendation:
Finds movies sharing common actors
Ranks recommendations based on:
Number of shared actors
Movie rating
Technologies Used
Python
Pandas, NumPy
YAKE (keyword extraction)
Neo4j Graph Database
Cypher Query Language
How to Run
Mount Google Drive and load dataset

Install dependencies:

pip install pandas numpy yake neo4j tqdm
Run preprocessing scripts
Generate CSV files for nodes and relationships
Connect to Neo4j and execute queries
Run recommendation function
Output
Graph database with movies and relationships
Actor-based movie recommendations
Node and relationship statistics
Future Improvements
Add genre-based recommendations
Use embeddings for semantic similarity
Build API or web interface
Optimize queries for performance
