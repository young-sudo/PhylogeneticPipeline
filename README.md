# Phylogenetic Pipeline

## Usage

### Data preparation

To fetch proteomes for organism names in `species_list.txt` (one taxon per line) from NCBI Datasets:
>`./run_fetch_proteomes.sh species_list.txt`

`PhyloPipeline.py` - package with helper functions for other scripts

### Sequence clustering

To run clustering on sequences in `sequences.fasta`

>`./run_clust_mmseqs.sh sequences.fasta`

### MSA and NJ

>`run_gene_trees.py` - for gene trees

### Genome Trees

>`run_genome_tree.py` - for consensus tree

>`run_fasturec.sh` - for supertree

## Analysis Documents

Tree analysis outline can be found in: `analysis.pdf` and `phylo_prezi.pdf`

## Trees Name Guide

`ml_tree.txt` - species trees made with ML

`trees_[alias].txt` - gene trees (NJ) for specific tasks

Aliases:
- `np` - no paralogs for supertree, trees size 3 to 23 (2111)
- `cnp` - no paralogs for consensus tree, only size=23, i.e. 1-1 with taxa set (461)
- `bnp` - no paralogs, filtered with bootstrap, only with high split support (1743)
- `bcnp` - no paralogs, filtered with bootstrap, 1-1 with taxa set (206)
- `p` - with paralogs, size 3 to 23 (4187)
