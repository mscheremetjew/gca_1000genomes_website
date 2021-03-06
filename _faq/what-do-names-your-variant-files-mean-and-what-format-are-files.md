---
title: "What do the names of your variant files mean and what format are the files?"
faq_tags:
  - data-access
  - file-format
  - vcf
faq_related:
  - what-format-are-your-alignments-and-what-do-names-mean
  - where-are-your-sequence-files-located
  - how-do-i-get-sub-section-vcf-file
  - are-my-snps-found-1000-genomes-project
---
                    
Our variant files are distributed in [vcf format](http://vcftools.sourceforge.net/), a format initially designed for the 1000 Genomes Project which has seen wider community adoption.

The majority of our vcf files are named in the form:

**<span style"color:red">ALL</span>.<span style"color:blue">chrN</span>|<span style"color:green">wgs|wex</span>.<span style"color:orange">2of4intersection</span>.<span style"color:violet">20100804</span>.<span style"color:darkblue">snps|indels|sv</span>.genotypes.<span style"color:darkred">analysis_group</span>.vcf.gz**.

This name starts with the <span style"color:red">population</span> that the variants were discovered in, if ALL is specifed it means all the individuals available at that date were used. Then the <span style"color:blue">region</span> covered by the call set, this can be a chromosome, <span style"color:green">wgs</span> (which means the file contains at least all the autosomes) or <span style"color:green">wex</span> (this represents the whole exome) and a <span style"color:orange">description</span> of how the call set was produced or who produced it, the <span style"color:violet">date</span> matches the sequence and alignment freezes used to generate the variant call set. Next a field which describes what <span style"color:darkblue">type of variant</span> the file contains, then the <span style"color:darkred">analysis group</span> used to generate the variant calls, this should be low coverage, exome or integrated and finally we have either sites or genotypes. A sites file just contains the first 8 columns of the vcf format and the genotypes files contain individual genotype data as well.

Release directories should also contain panel files which also describe what individuals the variants have genotypes for and what populations those individuals are from
