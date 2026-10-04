# Cannabis sativa cultivar Abacus UCSC genome browser track hub
A UCSC genome browser track hub was generated based on the genome sequence of the Cannabis sativa cultivar 'Abacus'. Annotation was carried out using GALBA version 1.0.6 with default parameters using the protein sequences of cultivar cs10.

```
singularity exec galba.sif galba.pl --species=abacus \
                                     --genome=../fasta/abacus.fna \
                                     --prot_seq=../protein/cs10.faa \
                                     --threads 20 --gff3
```

A total of eight additional varieties (cannbio, cs10, dash, finola, jamlionF1, jlwild, pink, pkush) and the outgroups *Trema orientalis* and *Morus alba* were aligned to the Abacus genome using Cactus version 2.1.1 and the output HAL file converted to MAF using hal2maf with `--noDupes --onlyOrthologs --noAncestors`. Note that GALBA annotation gene names have not been converted to gene IDs or symbols.

## Data file location on Zenodo

Large files for this trackhub are stored on zenodo: [https://zenodo.org/records/23138193](https://zenodo.org/records/23138193). The track hub text files point to the zenodo files. 

## Connect track hub to UCSC

The track hub can be connected via [https://genome.ucsc.edu/cgi-bin/hgHubConnect](https://genome.ucsc.edu/cgi-bin/hgHubConnect).
