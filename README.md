# Study of ColE1 expression using public data

## Finding relevant data in short read archive

We searched {NCBI_SRA] (https://www.ncbi.nlm.nih.gov/sra) with the following query:

https://www.ncbi.nlm.nih.gov/sra?term=(((((%22escherichia%20coli%22%5BOrganism%5D)%20AND%20illumina%5BPlatform%5D))%20AND%20%22transcriptomic%22%5BSource%5D)%20AND%20%22rna%20seq%22%5BStrategy%5D)%20AND%20(%222018%22%5BPublication%20Date%5D%20%3A%20%222019%22%5BPublication%20Date%5D)

```
((((("escherichia coli"[Organism]) 
AND illumina[Platform])) 
AND "transcriptomic"[Source]) 
AND "rna seq"[Strategy]) 
AND ("2018"[Publication Date] : "2019"[Publication Date]) 
```

## possible good hit: https://www.ncbi.nlm.nih.gov/bioproject/PRJNA459526

This contaions 16 datasets, we downloaded RunInfo table from NCBI and removed columns to produce this:

Run	download_path	LibraryName
SRR7119574	https://sra-download.ncbi.nlm.nih.gov/traces/sra62/SRR/006952/SRR7119574	lacZ_ind_RPF_r2
SRR7119575	https://sra-download.ncbi.nlm.nih.gov/traces/sra62/SRR/006952/SRR7119575	lacZ_ind_mRNA_r2
SRR7119576	https://sra-download.ncbi.nlm.nih.gov/traces/sra62/SRR/006952/SRR7119576	lacZ_unind_RPF_r2
SRR7119577	https://sra-download.ncbi.nlm.nih.gov/traces/sra62/SRR/006952/SRR7119577	lacZ_unind_mRNA_r2
SRR7119562	https://sra-download.ncbi.nlm.nih.gov/traces/sra62/SRR/006952/SRR7119562	lacZ_ind_RPF_r1
SRR7119563	https://sra-download.ncbi.nlm.nih.gov/traces/sra62/SRR/006952/SRR7119563	lacZ_ind_mRNA_r1
SRR7119572	https://sra-download.ncbi.nlm.nih.gov/traces/sra62/SRR/006952/SRR7119572	lacZ_unind_RPF_r1
SRR7119573	https://sra-download.ncbi.nlm.nih.gov/traces/sra62/SRR/006952/SRR7119573	lacZ_unind_mRNA_r1


## Read processing

The reads contain the following adapters:

```
-a 
-b 
-g 
```
