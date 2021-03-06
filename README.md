# Nashville Music Hackathon 2018

## Getting Started

To get started download the test data set here: 

https://www.dropbox.com/s/6ca927k9rqjwaq4/input.csv?dl=0 

Clone this repo and place the "input.csv" file into the root of this repository on your machine. 

This challenge uses Pandas as a requirement, so make sure you install the requirements: 

```
pip install -r requirements.txt
```

## Challenge

Given a bipartite graph, you must write a function connected_components(filepath) that takes 
a filepath of a csv (format: node_x, node_y), computes the connected components, and
outputs to a new csv called "output.csv". (format: cluster_id, node_x, node_y).

For example, given the following input csv:

| node_x | node_y |
| -------| -------|
| 1      | 2      |
| 2      | 4      |
| 5      | 7      |
| 7      | 9      |
| 11     | 12     |


Your script should create the following output file, called "output.csv" using the "input.csv" provided:

|   cluster_id  |	node_x  |	node_y  |
| ------------- | ------- | ------- |
|   1           |	1       |	2       |
|   1           |	2       |	4       |
|   5           |	5       |	7       |
|   5           |	7       |	9       |
|   11          |	11      |	12      |

Your solution must optimize memory consumption. An artificial memory constraint of 100 MB has been placed on the process so that all of the data cannot be loaded into memory. Implement your solution in the connected_components.py file provided in this repository. 


## Testing Your Results:

To test your results run the unittest in hackathon_tests.py:
```
python -m hackathon_tests
```
Good luck!
