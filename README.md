[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.7899721.svg)](https://doi.org/10.5281/zenodo.7899721)

# Influenza Sequences Toolbox
A set of scripts and bioinformatic tools to process, handle and analyse Influenza viruses sequences.

## Installation

```
conda create -n influenza_toolbox -c bioconda -c conda-forge pysamstats samtools seqkit blast
conda activate influenza_toolbox
bin_path=$(which seqkit | sed 's/seqkit$//g')
git clone https://github.com/gtrichard/influenza_sequences_toolbox
cp influenza_sequences_toolbox/bin/* $bin_path
```

Galaxy versions of the tools will be developped later.


## Tools

The available tools are quickly presented below, refer to their command-line manual for more in-depth explanations about their usage.

| Tool name         | Description                                          |
| ----------------- | ---------------------------------------------------- |
| [concatenateSegments] | Takes a fasta file as input and concatenates all 8 segments for each strain/sample if the sequence is of good quality. |
| [fastaToGenotype] | Takes a fasta file and a makeblastdb database as input to assign genotypes to each segments of the fasta file. |
| [callConsensus] | Takes a BAM file and its reference fasta file as input to output a high-quality consensus sequence (adapted for short reads alignments). |

[seqkit]: https://bioinf.shenwei.me/seqkit/
[blast]: https://www.biostars.org/p/266983/
[concatenateSegments]: https://github.com/gtrichard/influenza_sequences_toolbox/blob/main/bin/concatenateSegments
[fastaToGenotype]: https://github.com/gtrichard/influenza_sequences_toolbox/blob/main/bin/fastaToGenotype
[callConsensus]: https://github.com/gtrichard/influenza_sequences_toolbox/blob/main/bin/callConsensus


## Citation

If you use some of these scripts in your work, please cite this repository using the following DOI:

Gautier RICHARD. (2023, May 5). gtrichard/influenza_sequences_toolbox: Influenza Sequences Toolbox. Zenodo. https://doi.org/10.5281/zenodo.7899721
