---
title: "What library insert sizes where used in the 1000 genomes project?"
faq_tags:
  - data-access
  - statistics
faq_related:
  - what-sequence-index-file
  - what-bas-file
  - are-there-any-statistics-about-how-much-sequence-data-has-been-generated-project
---
                    
The project has generally used short insert libraries between 100 and 600bp for Illumina sequence data. For SOLiD and 454 sequence data you will see a wider variety of insert sizes. The insert sizes are reported in both the [sequence.index](http://ftp.1000genomes.ebi.ac.uk/vol1/ftp/README.sequence_data) file and the [bas files](http://ftp.1000genomes.ebi.ac.uk/vol1/ftp/README.alignment_data). The sequence index file contains the insert size reported to the SRA when the data was submitted, the bas files contain the mean insert size based on the alignment and the standard deviation from that mean.
