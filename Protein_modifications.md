# Protein Modifications Remediation

TODO:
- Add section about terminal acetylation/amidation and other caps

## Sections

- [Glossary of Terms](#glossary-of-terms)
- [Introduction](#introduction)
- [New CCD Data Categories](#new-ccd-data-categories)
- [New mmCIF Data Categories](#new-mmcif-data-categories)

## Glossary of Terms

PCM - Protein chemical modification
PTM - Post-translational modification

## Introduction

- Summary of the problem and what is missing
  - No data categories that comprehensively record the protein modifications that occur 
  within the PDB archive
  - A lack of clear rules as to how to annotate protein modifications
  - Lack of standardised handling of protein modifications within the PDB archive

- This makes it difficult to search and analyse protein modifications that occur in the PDB archive

- Summary of the aims of the remediation
  - Stan
- Summary of what the remediation achieves


## New CCD Data categories

- Here have a summary of pdbx_chem_comp_pcm


### Protein Modification Categories and Types 

Have a short intro to this and why two are used

#### Item to say if it can be a protein modification

- Describe how this works
- That this is used to maintain the standardisation by preventing
some CCDs from bein used to annotate protein modifications
- Give example here


#### Categories
- These are broad groups of modifications that group the modificatiion broadly by it's 
context or chemical characteristics. 
- Includes (table with definitions)
  - Named protein modification
  - Lipid/lipid-like 
  - Covalent chemical modification

- A full list of the categories created as part of this remediation can be found in the CCD dictionary controlled vocabulary
- https://mmcif.wwpdb.org/dictionaries/mmcif_pdbx_v50.dic/Items/_pdbx_chem_comp_pcm.category.html

#### Types

- These are specific and unambiguous definitions of protein modifications. 
- For example phosphorylation, or methylation refer to unambiguous chemical modification 
groups.

- When used in conjunction with pdbx_chem_comp_pcm.categories, the user is able to 
obtain both specific precise information about the modification, but also the more 

### Enriched Annotation

#### UniProt Crossreferencing

#### Position


#### Polypeptide Position



## New mmCIF Data Categories



## Acknowledgements
The protein chemical modifications (PCMs) and post translational modifications (PTMs) 
remediation project is a wwPDB collaborative project carried out principally by 
[PDBe](https://www.ebi.ac.uk/pdbe/) at [EMBL-EBI](https://www.ebi.ac.uk/), and is funded 
by BBSRC grant number BB/V018779/1.
