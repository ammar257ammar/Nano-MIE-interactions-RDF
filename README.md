# Exploring Adverse Outcome Pathways for Nanomaterials with semantic web technologies

![GitHub release (latest SemVer)](https://img.shields.io/github/v/release/ammar257ammar/Nano-MIE-interactions-RDF) ![GitHub](https://img.shields.io/github/license/ammar257ammar/Nano-MIE-interactions-RDF)

This repository contains the RML mappings to a convert the dataset produced in this work into RDF, annotated using several ontologies including eNanoMapper and BioAssay ontologies, along with the generated RDF.

### Paper Authors:

* Jeaphianne P. M. van Rijn [0000-0001-5026-7705](https://orcid.org/0000-0001-5026-7705), 
* Marvin Martens [0000-0003-2230-0840](https://orcid.org/0000-0003-2230-0840), 
* Ammar Ammar [0000-0002-8399-8990](https://orcid.org/0000-0002-8399-8990), 
* Mihaela Roxana Cimpan, 
* Valerie Fessard [0000-0001-9046-9117](https://orcid.org/0000-0001-9046-9117), 
* Peter Hoet, Nina Jeliazkova [0000-0002-4322-6179](https://orcid.org/0000-0002-4322-6179), 
* Sivakumar Murugadoss4, 
* Ivana Vinković Vrček7 [0000-0003-1382-5581](https://orcid.org/0000-0003-1382-5581), 
* Egon L. Willighagen1 [0000-0001-7542-0286](https://orcid.org/0000-0001-7542-0286)

# Abstract 
Adverse Outcome Pathways (AOPs) have been proposed to facilitate mechanistic understanding of interactions of chemicals/materials with biological systems. Each AOP starts with a molecular initiating event (MIE) and possibly ends with adverse outcome(s) (AOs) via a series of key events (KEs). So far, the interaction of engineered nanomaterials (ENMs) with biomolecules, biomembranes, cells, and biological structures, in general, is not yet fully elucidated. There is also a huge lack of information on which AOPs are ENMs-relevant or -specific, despite numerous published data on toxicological endpoints they trigger, such as oxidative stress and inflammation. We propose to integrate related data and knowledge recently collected. Our approach combines the annotation of nanomaterials and their MIEs with ontology annotation to demonstrate how we can then query AOPs and biological pathway information for these materials. We conclude that a FAIR (Findable, Accessible, Interoperable, Reusable) representation of the ENM-MIE knowledge simplifies integration with other knowledge.

# RDF Model

![Nanomaterial MIE knowledge graph RDF model diagram](https://github.com/ammar257ammar/Nano-MIE-interactions-RDF/blob/master/model-diagram/nanomaterial-mie-rdf.png)


# Generating the RDF

### 1. Clone this repository to your computer, and "cd" into the cloned directory

```bash
git clone https://github.com/h2020-riskgone/Nanomaterials-MIE-interactions-RDF.git
```

### 1. Run the following Docker command to convert the CSV file "nano-aop-paper-sheet-comma-latest-rowid.csv" into RDF.

```bash
docker run -it --rm --name rmltools -v $(pwd):/data aammar/rmltools rmlmapper /data/mapping.yml /data/rdf/nano-mie-aop.nq
```

