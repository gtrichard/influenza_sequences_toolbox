[![DOI](https://zenodo.org/badge/DOI/10.1093/ve/veae112.svg)](https://academic.oup.com/ve/article/11/1/veae112/7924081) [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.15132490.svg)](https://doi.org/10.5281/zenodo.15132490)



# Influenza Sequences Toolbox
A set of scripts and bioinformatic tools to process, handle and analyse Influenza viruses sequences.

## Installation

```
conda create -n influenza_toolbox -c bioconda -c conda-forge pysamstats samtools seqkit blast bamtools
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
| [callConsensus] | Takes a BAM file and its reference fasta file as input to output a high-quality consensus sequence (adapted for short reads alignments). |
| [genotypeFasta] | Takes a fasta file and a makeblastdb database as input to assign genotypes to each segments of the fasta file. |
| [annotateFasta] | Takes a genotypeFasta log file and fasta file as input, as well as two tab-delimited database files, to annotate the full genome genotype as well as formating the strain names and adding important metadata to the fasta headers. |

[seqkit]: https://bioinf.shenwei.me/seqkit/
[blast]: https://www.biostars.org/p/266983/
[concatenateSegments]: https://github.com/gtrichard/influenza_sequences_toolbox/blob/main/bin/concatenateSegments
[callConsensus]: https://github.com/gtrichard/influenza_sequences_toolbox/blob/main/bin/callConsensus
[genotypeFasta]: https://github.com/gtrichard/influenza_sequences_toolbox/blob/main/bin/genotypeFasta
[annotateFasta]: https://github.com/gtrichard/influenza_sequences_toolbox/blob/main/bin/annotateFasta

## Database

This repository contains a modified version of the OctoFlu database to have proper M gene assignment to pdm or EA clades using a format compatible with the genotypeFasta tool.


## Citation

If you use some of these scripts in your work, please cite this article and this repository DOI:

- Gautier Richard, Séverine Hervé, Amélie Chastagner, Stéphane Quéguiner, Véronique Beven, Edouard Hirchaud, Nicolas Barbier, Stéphane Gorin, Yannick Blanchard, Gaëlle Simon. (2025). Major change in swine influenza virus diversity in France owing to emergence and widespread dissemination of a newly introduced H1N2 1C genotype in 2020. Virus Evolution. Volume 11. Issue 1. 2025. veae112. https://doi.org/10.1093/ve/veae112

- Gautier Richard. (2025). gtrichard/influenza_sequences_toolbox: Influenza Sequences Toolbox 0.6 (0.6). Zenodo. https://doi.org/10.5281/zenodo.15132490

If you use the modified OctoFlu database to genotype swIAV segments, please cite OctoFlu:

- Anderson, T., Chang, J., Arendsee, Z., mazeller, 2022. flu-crew/octoFLU: MRA Publication Release. https://doi.org/10.5281/zenodo.7458929
