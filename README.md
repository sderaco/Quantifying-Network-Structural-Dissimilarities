# Quantifying network structural dissimilarities 

## Tiago A. Schieber, Laura Carpi, Albert Díaz-Guilera, Panos M. Pardalos, Cristina Masoller and Martín G. Ravetti

For information regarding the dataset download, algorithm and codes please read the "readme.txt" file.

Graph's Dissimilarity Measure  (D)


In this repository, you will find the codes and instances used in the article:

Quantifying network structural dissimilarities by Tiago A. Schieber, Laura Carpi, Albert Díaz-Guilera, Panos M. Pardalos, Cristina Masoller and Martín G. Ravetti


## Algorithm

The algorithm is written in R and uses functions from the igraph library (The Network Analysis Package - http://igraph.org/). The program reads two graphs on an edge list format, the weights (w1, w2 and w3) and computes the D-distance, as discussed in the article. 

download algorithm: d_distance.r

Instructions: after running the d_distance.r file make:

D(g,h,w1,w2,w3)

For example, D("net1.txt","net2.txt",0.45,0.45,0.1) computes the D measure considering w1=0.45, w2=0.45 and w3=0.1 between the networks net1.txt and net2.txt in an edgelist format.

As discussed in the article, there is a significant computational drawback in using the alpha-centrality of the complement in large and sparse graphs. The d-function computes the dissimilarity disconsidering the use of the complement. 

For example, d("net1.txt","net2.txt",0.45,0.45,0.1) computes the dissimilarity measure considering w1=0.45, w2=0.45 and w3=0.1 between the networks net1.txt and net2.txt in an edgelist format disconsidering the Jensen-Shannon between the alpha-centrality distribution of the graph's complement.


## Instances for the non-isomorphic test
 
The experiment consists in computing the D-distance between pairs of known non-isomorphic graphs.  

### Generation

Nauty and Traces are programs for computing automorphism groups of graphs and digraphs. They can also produce a canonical labeling. See Brendan McKay and Adolfo Piperno's web page (http://pallini.di.uniroma1.it/) for more information.
Here, we use geng to generate all graphs of a specified class and showg to write graphs in human-readable format.

Our distance returns a positive value for all the cases here considered.

Some files are in 7zip format (see http://www.7-zip.org/ for more information).

|Nodes| #graphs| Files |
|:-------------:|:-------------:| -----:| 
| 4 | 11|[graph_n=4](https://drive.google.com/file/d/0B92qPSf2Wn1LYnk0b0IteW9ISXM/view) |
|5|34|[graph_n=5](https://drive.google.com/file/d/0B92qPSf2Wn1LZDFYYmVES01WZEk/view)|
|6|156|[graph_n=6](https://drive.google.com/file/d/0B92qPSf2Wn1LdGRZR1diNy1DYUk/view)|
|7|1044|[graph_n=7](https://drive.google.com/file/d/0B92qPSf2Wn1LNk4ySVVJOGo5cEE/view)|
|8|12346|[graph_n=8](https://drive.google.com/file/d/0B92qPSf2Wn1Ld1lZeW83X0pENm8/view)|
|9|274668|[graph_n=9](https://drive.google.com/file/d/0B92qPSf2Wn1LNC1GX1RIdG1xUk0/view)|
|10|12005168|[graph_n=10](https://drive.google.com/file/d/0B92qPSf2Wn1LNzVQQjJ2VjhRWFE/view)|

#### 20 Nodes

When considering 20 nodes, the complete set of non-isomorphic graphs has approximately 6.4 x 10^38 graphs. In this case, we focus on trees and connected k-regular graphs. 

#### k-regular graphs

|k| # graphs|Files|
|:------:|:-----:|:------:|
|2|1|[regular_graph_n=20_k=2](https://drive.google.com/file/d/0B92qPSf2Wn1LM2l0OVpvNURSZDQ/view)   (34 bytes)
|3|5104|            [regular_graph_n=20_k=3](https://drive.google.com/file/d/0B92qPSf2Wn1LQnMyTzhjcXlUQm8/view)   (17 MB)
|4|1533866586| [regular_graph_n=20_k=4](https://drive.google.com/file/d/0B92qPSf2Wn1LOTBuMXVuVFEtWGc/view)   (7 GB)
|5 |476565504 |[regular_graph_n=20_k=5](https://drive.google.com/file/d/0B92qPSf2Wn1LdHFDUl81NldWZG8/view)   (2 GB)
|6| 188290831| [regular_graph_n=20_k=6](https://drive.google.com/file/d/0B92qPSf2Wn1LQVo3UFpwdGtOTXM/view)   (731 MB)
|7| 93595527 |[regular_graph_n=20_k=7](https://drive.google.com/file/d/0B92qPSf2Wn1LWUxoWEhNSk93TEk/view)   (374 MB)
|8| 25954544 |[regular_graph_n=20_k=8](https://drive.google.com/file/d/0B92qPSf2Wn1LWWt4ZDFPdUtnekk/view)   (99 MB)
|9| 15752252 |[regular_graph_n=20_k=9](https://drive.google.com/file/d/0B92qPSf2Wn1LZS1remdOWkJLN1E/view)   (76 MB)
|10| 8998309 |[regular_graph_n=20_k=10](https://drive.google.com/file/d/0B92qPSf2Wn1LVUdCWGdnN2xRYWM/view)  (49 MB)
|11| 10245059| [regular_graph_n=20_k=11](https://drive.google.com/file/d/0B92qPSf2Wn1LcTloUWJPQmZTeTA/view)  (52 MB)
|12| 14024101| [regular_graph_n=20_k=12](https://drive.google.com/file/d/0B92qPSf2Wn1LWWVkLTQ1Y3JMVzA/view)  (69 MB)


#### Non-isomorphic connected trees


|Nodes| # graphs| Files|
|:-----:|:-----:|:-----:|
|18|123867|[connected_trees_n=18](https://drive.google.com/file/d/0B92qPSf2Wn1LNFlzZUtfd2ZQTDA/view) (3 MB)| 
|20|823065|[connected_trees_n=20](https://drive.google.com/file/d/0B92qPSf2Wn1LRmpzYkFKcnRPWWM/view) (27 MB)| 
|21|2144505| [connected_trees_n=21](https://drive.google.com/file/d/0B92qPSf2Wn1LVVhnRWJuU2tib0E/view) (76 MB)|

 


# Contact information

Martin Gómez Ravetti - martin.ravetti at dep.ufmg.br
Tiago Schieber - tischieber@gmail.com
