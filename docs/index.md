# Tentris -- A Tensor-Based Triple Store

The number and size of RDF knowledge graphs grows continuously. Efficient storage solutions for these graphs are indispensable for their use in real applications. 
We present such a storage solution dubbed Tentris.
Our solution represents RDF knowledge graphs as sparse order-3 tensors using a novel data structure, which we dub hypertrie. 
It then uses tensor algebra to carry out SPARQL queries by mapping SPARQL operations to Einstein summation. 
By being able to compute Einstein summations efficiently, Tentris outperforms the commercial and open-source RDF storage solutions evaluated in our experiments by at least 1.8 times with respect to the average number of queries it can serve per second on three datasets of up to 1 billion triples.
