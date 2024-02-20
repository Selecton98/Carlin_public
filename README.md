# Carlin_heart
These jupyter notebooks are refered to the CARLIN pipeline modified by the authors of the DARLIN paper.

Then very first step of the CARLIN pipeline is cleaning-up of the amplicon data to match the single-cell transcriptomic data.

Amplicon sequences include the barcode (corresponding to the 10x single-cell barcodes) and the UMI (corresponding to the CARLIN allele sequence). 

(1) We extract these information from the fastq file of amlicon [Step #6-7]. The quality is the NGS sequencing quality.

(2) We filter the reads including the barcodes that also found in the 10x single-cell CellRanger pre-processing output [Step #9-10].

# These reads could be further filtered according to sequencing quality, sequence features, etc.

(3) We filter the cells with a linear slope between read number per cell and clone number per cell. (similar to the doublet cells in 10x). [Step #11]

# Then there are some plots that can help with determining the clonal identity of cells.

(4) How many cells/clones should be there? The excessive read counts are likely noise. [Step #14]  

(5) How the sequences of certain distance could assemble clones if the low-count reads are removed. [Step #17]

(6) What is the dominant cell barcode with each clone which can be the representative clonal id. [Step #18]

#To be continued.
