Hello,

This is my project for the Digital Humanities course, entitled "Creating a Semantic Map of Cities in the Czech Republic".

I am very interested in the possibilities of language models to represent text in vector space. I came up with the idea of comparing this vector space with the real world, and I decided to try it out using Czech cities as an example. The key question of my project is: how is the position of an object (in our case, a city) in space related to its position (in relation to other objects) in the embedding space?

My project is divided into two main parts:
1. Data extraction and cleaning
- I parsed Wikipedia pages about Czech cities (610 in total)
- data cleaning
- I had to resolve special cases of cities whose names refer to other things (e.g., Lom, Solnice)

2. Creating a semantic map of cities
- keyword extraction: I extracted keywords that make each city “unique” using TF-iDF
- creating an embedding using a sentence transformer
- reducing the dimension using U-MAP
- 2D visualization using Plotly: displaying the map itself
- finding the closest neighbors: a function that finds cities most similar to a given city by calculating the cosine similarity between their vector embeddings.

Results:

The main result of the project is the interactive semantic map of Czech cities which you can look through and discover similarities in cities that are far away from each other in reality. Also the Nearest Neighbor Search function lets the user enter a city name and discover what cities are semantically most similar to his city. This semantic processing can just be entertaining and maybe show some patterns or insights about the cities that had similar historical development or geography.

(!) You can see some examples of interesting groups of cities on the map in the **city_group_examples** folder.
- There is a group ambi - group of cities that I didn't yet include in the ambiguous list to reparse correctly. However it is clearly seen that they get different embeddings than other cities.

My notes:

- I believe that my project is based on a truly interesting idea and has some interesting results, but for it to be used more effectively, it is necessary to use other sources besides Wikipedia and, possibly, divide this task into several subtasks in order to cover the entire complexity of this "real-world position -> the problem in the semantic coordinates".
- Further operations with the input data (e.g. summarization of info about each city) could benefit in more clear and precise results.


- Yevhenii Kaprizenkov
