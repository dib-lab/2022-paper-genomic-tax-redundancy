---
title: 'Comprehensive evaluation of genomic redundancy and taxonomic coherence in large biological databases '
keywords:
- Shannon entropy
- unicity distance
lang: en-US
date-meta: '2022-11-19'
author-meta:
- John Doe
- Jane Roe
header-includes: |-
  <!--
  Manubot generated metadata rendered from header-includes-template.html.
  Suggest improvements at https://github.com/manubot/manubot/blob/main/manubot/process/header-includes-template.html
  -->
  <meta name="dc.format" content="text/html" />
  <meta property="og:type" content="article" />
  <meta name="dc.title" content="Comprehensive evaluation of genomic redundancy and taxonomic coherence in large biological databases " />
  <meta name="citation_title" content="Comprehensive evaluation of genomic redundancy and taxonomic coherence in large biological databases " />
  <meta property="og:title" content="Comprehensive evaluation of genomic redundancy and taxonomic coherence in large biological databases " />
  <meta property="twitter:title" content="Comprehensive evaluation of genomic redundancy and taxonomic coherence in large biological databases " />
  <meta name="dc.date" content="2022-11-19" />
  <meta name="citation_publication_date" content="2022-11-19" />
  <meta property="article:published_time" content="2022-11-19" />
  <meta name="dc.modified" content="2022-11-19T21:39:17+00:00" />
  <meta property="article:modified_time" content="2022-11-19T21:39:17+00:00" />
  <meta name="dc.language" content="en-US" />
  <meta name="citation_language" content="en-US" />
  <meta name="dc.relation.ispartof" content="Manubot" />
  <meta name="dc.publisher" content="Manubot" />
  <meta name="citation_journal_title" content="Manubot" />
  <meta name="citation_technical_report_institution" content="Manubot" />
  <meta name="citation_author" content="John Doe" />
  <meta name="citation_author_institution" content="Department of Something, University of Whatever" />
  <meta name="citation_author_orcid" content="XXXX-XXXX-XXXX-XXXX" />
  <meta name="twitter:creator" content="@johndoe" />
  <meta name="citation_author" content="Jane Roe" />
  <meta name="citation_author_institution" content="Department of Something, University of Whatever" />
  <meta name="citation_author_institution" content="Department of Whatever, University of Something" />
  <meta name="citation_author_orcid" content="XXXX-XXXX-XXXX-XXXX" />
  <link rel="canonical" href="https://dib-lab.github.io/2022-paper-genomic-tax-redundancy/" />
  <meta property="og:url" content="https://dib-lab.github.io/2022-paper-genomic-tax-redundancy/" />
  <meta property="twitter:url" content="https://dib-lab.github.io/2022-paper-genomic-tax-redundancy/" />
  <meta name="citation_fulltext_html_url" content="https://dib-lab.github.io/2022-paper-genomic-tax-redundancy/" />
  <meta name="citation_pdf_url" content="https://dib-lab.github.io/2022-paper-genomic-tax-redundancy/manuscript.pdf" />
  <link rel="alternate" type="application/pdf" href="https://dib-lab.github.io/2022-paper-genomic-tax-redundancy/manuscript.pdf" />
  <link rel="alternate" type="text/html" href="https://dib-lab.github.io/2022-paper-genomic-tax-redundancy/v/1f44b3ca936a98beef02ce3d72c283e49a513f6b/" />
  <meta name="manubot_html_url_versioned" content="https://dib-lab.github.io/2022-paper-genomic-tax-redundancy/v/1f44b3ca936a98beef02ce3d72c283e49a513f6b/" />
  <meta name="manubot_pdf_url_versioned" content="https://dib-lab.github.io/2022-paper-genomic-tax-redundancy/v/1f44b3ca936a98beef02ce3d72c283e49a513f6b/manuscript.pdf" />
  <meta property="og:type" content="article" />
  <meta property="twitter:card" content="summary_large_image" />
  <link rel="icon" type="image/png" sizes="192x192" href="https://manubot.org/favicon-192x192.png" />
  <link rel="mask-icon" href="https://manubot.org/safari-pinned-tab.svg" color="#ad1457" />
  <meta name="theme-color" content="#ad1457" />
  <!-- end Manubot generated metadata -->
bibliography:
- content/manual-references.json
manubot-output-bibliography: output/references.json
manubot-output-citekeys: output/citations.tsv
manubot-requests-cache-path: ci/cache/requests-cache
manubot-clear-requests-cache: false
...






<small><em>
This manuscript
([permalink](https://dib-lab.github.io/2022-paper-genomic-tax-redundancy/v/1f44b3ca936a98beef02ce3d72c283e49a513f6b/))
was automatically generated
from [dib-lab/2022-paper-genomic-tax-redundancy@1f44b3c](https://github.com/dib-lab/2022-paper-genomic-tax-redundancy/tree/1f44b3ca936a98beef02ce3d72c283e49a513f6b)
on November 19, 2022.
</em></small>



## Authors



+ **John Doe**
  <br>
    ![ORCID icon](images/orcid.svg){.inline_icon width=16 height=16}
    [XXXX-XXXX-XXXX-XXXX](https://orcid.org/XXXX-XXXX-XXXX-XXXX)
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [johndoe](https://github.com/johndoe)
    · ![Twitter icon](images/twitter.svg){.inline_icon width=16 height=16}
    [johndoe](https://twitter.com/johndoe)
    <br>
  <small>
     Department of Something, University of Whatever
     · Funded by Grant XXXXXXXX
  </small>

+ **Jane Roe**
  ^[✉](#correspondence)^<br>
    ![ORCID icon](images/orcid.svg){.inline_icon width=16 height=16}
    [XXXX-XXXX-XXXX-XXXX](https://orcid.org/XXXX-XXXX-XXXX-XXXX)
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [janeroe](https://github.com/janeroe)
    <br>
  <small>
     Department of Something, University of Whatever; Department of Whatever, University of Something
  </small>


::: {#correspondence}
✉ — Correspondence possible via [GitHub Issues](https://github.com/dib-lab/2022-paper-genomic-tax-redundancy/issues)
or email to
Jane Roe \<jane.roe@whatever.edu\>.


:::


## Abstract {.page_break_before}

A central challenge in bacterial genomics and taxonomy is that genomic
databases are increasingly large and contain redundant content.  This
impacts the accuracy of taxonomic profilers and metagenome analysis
tools that rely on these databases.  Here, we probe the practical and
theoretical limits of genomic identification and taxonomic
classification by exploring _unicity distance_ and _Shannon
entropy_. Unicity distance provides an estimate of how many k-mers are
required to precisely identify a single reference genome from within a
database, while Shannon entropy of k-mers describes the
informativeness of a k-mer for taxonomic classification.  We show that
approximately 30% of genomes in GTDB rs207 have infinite unicity and
that 99% of k-mers can resolve taxonomy at the species, genus, or
family level.  We conclude that unicity distance and Shannon entropy
provide simple metrics for evaluating genomic redundancy and taxonomic
coherence of large genomic reference databases.


## Introduction {.page_break_before}

Introduction goes here.


## Results {.page_break_before}

### Many k-mers are genome specific

### Shannon entropy of k-mers can be used to measure taxonomic informativeness

We measured the species distribution in GTDB rs207 for 21.2 million hashes,
representing 21.2 billion 31-mers, and calculated the Shannon entropy of
species for each hash (equationXX). Per Table XX, 92.8% of hashes uniquely
identify a specific family.

| Taxonomic level | # perfectly informative hashes | cumulative % total | 
| -------- | -------- | -------- |
| species     | 21,150,287     | 92.8%     | 92.8%
| genus     | 1,262,281     | XXX%     |
| family     | 170,249     | YYY%     | 

(Make point that nucleotide k-mers are not necessarily specific beyond family ref protein paper.)

### Many k-mers with non-zero entropy come from a few specific genomes

Explore taxonomic incoherence and database contamination.

### Unicity distance can be used to estimate genomic redundancy

We next ask, how many genomes can be distinguished from each other
using a combinatorial collection of k-mers?  To do this, we estimate
the _unicity distance_ of each genome in the database, where the
unicity distance is defined as the smallest set of hashes capable of
uniquely identifying a genome. (k=31, scaled=1000)

Table YY shows that approximately 29.2% of the genomes in GTDB rs207
cannot be distinguished uniquely by any combination of k-mers with
these parameters.
 
| Unicity distance | Number of genomes | Percent of genomes |
| -------- | -------- | -------- |
| 1     | 48,630     | 15.3%     |
| infinite | 92,564 | 29.2% | 


## Discussion {.page_break_before}

Discussion goes here.


## Methods {.page_break_before}

Methods go here.


## References {.page_break_before}

<!-- Explicitly insert bibliography here -->
<div id="refs"></div>
