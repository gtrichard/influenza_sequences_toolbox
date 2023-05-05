# Influenza Sequences Toolbox
A set of scripts and bioinformatic tools to process, handle and analyse Influenza viruses sequences.

## Installation

```
conda create -n influenza_toolbox -c bioconda seqkit
conda activate influenza_toolbox
bin_path=$(which seqkit)
git clone https://github.com/gtrichard/influenza_sequences_toolbox
cp influenza_sequences_toolbox/bin/* $bin_path/.
```

Galaxy versions of the tool will be developped later.


## Tools

The available tools are quickly presented below, refer to their command-line manual for more in-depth explanations about their usage.

| Tool name         | Description                                          |
| ----------------- | ---------------------------------------------------- |
| concatenateSegments | Takes a fasta file as input and concatenates all 8 segments for each strain/sample if the sequence is of good quality. Requires [seqkit] to be available in your environment. |

[seqkit]: https://bioinf.shenwei.me/seqkit/


## Citation

If you use some of these scripts in your work, please cite this repository using the following citation:

