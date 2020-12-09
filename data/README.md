#### AdjacencyMatrix_Philosophers.zip: 
Contains the adjacency matrix for the total network of all philosophers that influence one another.
#### data_Philosophers.zip:
Contains all the web scraped data, cleaned and additional data such as year groups, age and so on.
#### pageContent.zip
Contains all the wikipedia pages of each philosopher that is a part of the network.
#### How-to:
To convert the adjacency matrix to a graph, it will be helpful to run the following lines:
```python
A = pd.read_csv('AdjacencyMatrix_Philosophers.csv')
A.index = A['Unnamed: 0']
A = A.drop('Unnamed: 0', axis=1).astype(int)
G = nx.Graph(A)
```
