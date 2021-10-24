# DNA-Cluster
DNA codon usage frequencies of a large sample of diverse biological organisms from different taxa.

Examination of codon usage frequencies in the genomic coding DNA of a large sample of diverse organisms from different taxa tabulated in the CUTG database, where we further manually curated and harmonized these existing entries by re-classifying CUTG's bacteria (bct) class into archaea (arc), plasmids (plm), and bacteria proper (keeping with the original label `bct'). The reclassification in the original `bct' domain was simplified by extracting from files `qbxxx.spsum.txt' (where xxx = bct (bacteria), inv (invertebrates), mam (mammals), pln (plants), pri (primates), rod (rodents), vrt (vertebrates)) the different genus names of the entries, and making the classification by genus. There were 514 different genus names. The different genus categories were checked and relabeled as `arc' where appropriate. In the eubacterial entries, the distinction was made of the bacterial genomes proper (keeping with the original label `bct'), and bacterial plasmids (now labeled `plm').

Following these preprocessing steps, the final dataset file comprises all entries of the CUTG databases qbxxx.spsum.txt in one text file. As detailed above, the qbbct.spsum.txt entries were separated as `bct' (that is, eubacteria), `plm' (plasmids), and `arc' (archaea), a distinction not originally made in the CUTG database.


Attribute Information:

Column 1: Kingdom
Column 2: DNAtype
Column 3: SpeciesID
Column 4: Ncodons
Column 5: SpeciesName
Columns 6-69: codon (header: nucleotide bases; entries: frequency of usage (5 digit floating point number))

The 'Kingdom' is a 3-letter code corresponding to `xxx' in the CUTG database name: 'arc'(archaea), 'bct'(bacteria), 'phg'(bacteriophage), 'plm' (plasmid), 'pln' (plant), 'inv' (invertebrate), 'vrt' (vertebrate), 'mam' (mammal), 'rod' (rodent), 'pri' (primate), and 'vrl'(virus) sequence entries. Note that the CUTG database does not contain 'arc' and 'plm' (these have been manually curated ourselves).

The 'DNAtype' is denoted as an integer for the genomic composition in the species: 0-genomic, 1-mitochondrial, 2-chloroplast, 3-cyanelle, 4-plastid, 5-nucleomorph, 6-secondary_endosymbiont, 7-chromoplast, 8-leucoplast, 9-NA, 10-proplastid, 11-apicoplast, and 12-kinetoplast.

The species identifier ('SpeciesID') is an integer, which uniquely indicates the entries of an organism. It is an accession identifier for each different species in the original CUTG database, followed by the first item listed in each genome.

The number of codons (`Ncodons') is the algebraic sum of the numbers listed for the different codons in an entry of CUTG. Codon frequencies are normalized to the total codon count, hence the number of occurrences divided by 'Ncodons' is the codon frequencies listed in the data file.

The species' name ('SpeciesName') is represented in strings purged of `comma' (which are now replaced by `space'). This is a descriptive label of the name of the species for data interpretations.

Lastly, the codon frequencies ('codon') including 'UUU', 'UUA', 'UUG', 'CUU', etc., are recorded as floats (with decimals in 5 digits).


