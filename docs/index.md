# WIP: this is a non-final draft
This page provides access to all the scripts, data and code needed to reproduce the results of the  paper:

> Alexander Bigerl, Felix Conrads, Charlotte Behning, Mohamed Sherif, Muhammad Saleem and Axel-Cyrille Ngonga Ngomo (2020) Tentris – A Tensor-Based Triple Store. In: The Semantic Web – ISWC 2020

'# todo: update when final

## abstract

The number and size of RDF knowledge graphs grows continuously. Efficient storage solutions for these graphs are indispensable for their use in real applications. 
We present such a storage solution dubbed Tentris.
Our solution represents RDF knowledge graphs as sparse order-3 tensors using a novel data structure, which we dub hypertrie. 
It then uses tensor algebra to carry out SPARQL queries by mapping SPARQL operations to Einstein summation. 
By being able to compute Einstein summations efficiently, Tentris outperforms the commercial and open-source RDF storage solutions evaluated in our experiments by at least 1.8 times with respect to the average number of queries it can serve per second on three datasets of up to 1 billion triples.

## Paper 

Find the paper [here]() #todo: add link when available

## Supplementary Material

**Benchmarking data:**  
SWDF: 
[data](https://hobbitdata.informatik.uni-leipzig.de/ISWC2020_Tentris/swdf.zip) | 
[queries](https://raw.githubusercontent.com/dice-group/iswc2020_tentris/master/queries/SWDF-Queries.txt) | 
[queries' stats](https://raw.githubusercontent.com/dice-group/iswc2020_tentris/master/queries/SWDF-Queries.tsv)  
DBpedia 2015-10 en: 
[data](https://hobbitdata.informatik.uni-leipzig.de/ISWC2020_Tentris/dbpedia_2015-10_en_wo-comments_c.nt.zst), concat. of [those files](https://raw.githubusercontent.com/dice-group/iswc2020_tentris/master/datasets/DBpedia-2015-10-en_links.txt) | 
[queries](https://raw.githubusercontent.com/dice-group/iswc2020_tentris/master/queries/DBpedia-Queries.txt) | 
[queries' stats](https://raw.githubusercontent.com/dice-group/iswc2020_tentris/master/queries/DBpedia-Queries.tsv)  
WatDiv: 
[run generator with scale factor 10000](https://dsg.uwaterloo.ca/watdiv/watdiv_v06.tar) | 
[queries](https://raw.githubusercontent.com/dice-group/iswc2020_tentris/master/queries/WatDiv-Queries.txt) | 
[queries' stats](https://raw.githubusercontent.com/dice-group/iswc2020_tentris/master/queries/WatDiv-Queries.tsv)  
Measurements: [data loading stats](https://raw.githubusercontent.com/dice-group/iswc2020_tentris/master/measurements/dataset_loading_stats.tsv) | 
[http bechmarks]() #todo | [cli benchmarks](https://raw.githubusercontent.com/dice-group/iswc2020_tentris/master/measurements/CLI_benchmark_results.csv)  
Setup: [ansible playbook](https://github.com/dice-group/tentris-paper-benchmarks/releases/tag/v1.0)  
Tentris Binaries: [1.0.4](https://raw.githubusercontent.com/dice-group/iswc2020_tentris/master/binaries/tentris_1.0.4.zip) | 
[1.0.4 2-way join](https://raw.githubusercontent.com/dice-group/iswc2020_tentris/master/binaries/tentris_1.0.4_2way_join.zip) | 
[1.0.4 rand. label order](https://raw.githubusercontent.com/dice-group/iswc2020_tentris/master/binaries/tentris_1.0.4_random_label_order.zip)  

**Proof of Hypertrie Space Complexity:** [pdf](https://raw.githubusercontent.com/dice-group/iswc2020_tentris/master/pdfs/proof_of_hypertrie_space_complexity.pdf)

**Impact of Small and Large Queries:** [pdf]() #todo