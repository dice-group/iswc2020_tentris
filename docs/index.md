# WIP: this is a non-final draft
This page provides access to all the scripts, data and code needed to reproduce the results of the  paper:

> Alexander Bigerl, Felix Conrads, Charlotte Behning, Mohamed Sherif, Muhammad Saleem and Axel-Cyrille Ngonga Ngomo (2020) <span style="font-variant:small-caps;">Tentris</span> – A Tensor-Based Triple Store. In: The Semantic Web – ISWC 2020

'# todo: update when final

## Abstract

The number and size of RDF knowledge graphs grows continuously. Efficient storage solutions for these graphs are indispensable for their use in real applications. 
We present such a storage solution dubbed <span style="font-variant:small-caps;">Tentris</span>.
Our solution represents RDF knowledge graphs as sparse order-3 tensors using a novel data structure, which we dub hypertrie. 
It then uses tensor algebra to carry out SPARQL queries by mapping SPARQL operations to Einstein summation. 
By being able to compute Einstein summations efficiently, <span style="font-variant:small-caps;">Tentris</span> outperforms the commercial and open-source RDF storage solutions evaluated in our experiments by at least 1.8 times with respect to the average number of queries it can serve per second on three datasets of up to 1 billion triples.

## Supplementary Material

Extended Example: [pdf](https://raw.githubusercontent.com/dice-group/iswc2020_tentris/master/suppl/extended_example.pdf)

Proof of Hypertrie Space Complexity: [pdf](https://raw.githubusercontent.com/dice-group/iswc2020_tentris/master/suppl/proof_of_hypertrie_space_complexity.pdf)

Impact of Small and Large Queries: [csv](https://raw.githubusercontent.com/dice-group/iswc2020_tentris/master/suppl/ByResultSize/summary_table_impact_of_small_and_large_queries.csv) | 
[plots](https://github.com/dice-group/iswc2020_tentris/tree/master/suppl/ByResultSize) 

## Evaluation Results
[http bechmarks](https://raw.githubusercontent.com/dice-group/iswc2020_tentris/master/measurements/HTTP_benchmark_results.csv) | 
[cli benchmarks](https://raw.githubusercontent.com/dice-group/iswc2020_tentris/master/measurements/CLI_benchmark_results.csv) | 
[data loading stats](https://raw.githubusercontent.com/dice-group/iswc2020_tentris/master/measurements/dataset_loading_stats.tsv)

## Reproducing Evaluation

We provide an [Ansible](https://docs.ansible.com/ansible/latest/index.html) playbook to automatically setup triple stores, datasets, queries, benchmarking tools and scripts to run the benchmarks on a test machine. The machine should have 32+ cores, 768+ GB RAM and 1+ TB free space on `/home`. We tested the setup on Ubuntu 20.04 and Debian Buster.   
[Visit Ansible playbook](https://github.com/dice-group/tentris-paper-benchmarks/releases/tag/v1.0) 

Direct download links for the benchmarks and <span style="font-variant:small-caps;">Tentris</span>-binaries used in the evaluation are provided below. 
 
<span style="font-variant:small-caps;">Tentris</span> Binaries:  
[v1.0.4](https://raw.githubusercontent.com/dice-group/iswc2020_tentris/master/binaries/tentris_1.0.4.zip) | 
[v1.0.4 2-way join](https://raw.githubusercontent.com/dice-group/iswc2020_tentris/master/binaries/tentris_1.0.4_2way_join.zip) | 
[v1.0.4 rand. label order](https://raw.githubusercontent.com/dice-group/iswc2020_tentris/master/binaries/tentris_1.0.4_random_label_order.zip)  

SWDF Benchmark:  
[rdf data](https://hobbitdata.informatik.uni-leipzig.de/ISWC2020_Tentris/swdf.zip)  | 
[queries](https://raw.githubusercontent.com/dice-group/iswc2020_tentris/master/queries/SWDF-Queries.txt) | 
[queries' stats](https://raw.githubusercontent.com/dice-group/iswc2020_tentris/master/queries/SWDF-Queries.tsv)  

DBpedia 2015-10 en Benchmark:  
[rdf data](https://hobbitdata.informatik.uni-leipzig.de/ISWC2020_Tentris/dbpedia_2015-10_en_wo-comments_c.nt.zst) \[1\] | 
[queries](https://raw.githubusercontent.com/dice-group/iswc2020_tentris/master/queries/DBpedia-Queries.txt)  | 
[queries' stats](https://raw.githubusercontent.com/dice-group/iswc2020_tentris/master/queries/DBpedia-Queries.tsv) 
 
WatDiv Benchmark:  
[generator](https://dsg.uwaterloo.ca/watdiv/watdiv_v06.tar) \[2\] | 
[queries](https://raw.githubusercontent.com/dice-group/iswc2020_tentris/master/queries/WatDiv-Queries.txt) | 
[queries' stats](https://raw.githubusercontent.com/dice-group/iswc2020_tentris/master/queries/WatDiv-Queries.tsv)  

  

---
\[1\] concatination of [those files](https://raw.githubusercontent.com/dice-group/iswc2020_tentris/master/datasets/DBpedia-2015-10-en_links.txt)  
\[2\] run with scale factor 10000

