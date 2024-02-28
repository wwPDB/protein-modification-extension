# Standardizing Protein Modifications

## Sections

- [Glossary of Terms](#glossary-of-terms)
- [Introduction](#introduction)
- [New CCD Data Categories](#new-ccd-data-categories)
- [New mmCIF Data Categories](#new-mmcif-data-categories)

## Glossary of Terms

PCM - Protein chemical modification 

PTM - Post-translational modification

## Introduction

The standardization of protein modification handling ensures that there is a single 
correct approach to handling each protein modification that occurs within the PDB 
archive. However, there are many existing PDB entries that contain protein modifications
that do not follow these handling conventions. 

As part of the protein modification remediation project, all entries containing protein 
modifications are being re-released to add the new protein modification data category 
described [here](Protein_modifications.md). During this process, any protein modifications
that are incorrectly handled within a PDB entry are ammended to ensure that they are 
consistently handled. 

In this document, some examples are provided describing the processes that are being 
performed to standardize protein modification handling in PDB entries. 

The following datasets provide a list of all the standardization processes being 
performed:
- [Splitting CCDs into two CCDs](data/summaries/ccds_split.csv)
- [Merging two CCDs into one CCD](data/summaries/ccds_merge.csv)
- [Replacing one CCD with another CCD](data/summaries/ccds_replace.csv)
- [Adding or removing a residue from a polypeptide sequence](data/summaries/ccds_to_add_or_remove_from_peptide_seq.csv)
- [Renaming CCDs](data/summaries/ccds_rename.csv)
- [Changing the CCD parent residue](data/summaries/ccds_change_parent.csv)

### Splitting CCDs

- Example of split
  - 3U31 MYK to MYR + LYS
  - This is because this is 'Lipid/lipid-like' and so should be handled as a linked 
  protein modification.

### Merging CCDs

What to include:
- Example of merge
  - 1E1Y PO3 + SER to SEP
  - This is because this is a 'Named protein modification' and so should be handled as a 
  single CCD describing both the peptide residue and modification group.

### Replacing CCDs

- Example of replacing:
  - 19HC HEM to HEC

### Adding CCDs to Polypeptide Sequences
- Example of adding ACE/NH2 to N- or C-terminus
  - 1BHQ for ACE and 4TKY for NH2
  
### Renaming CCDs
- Example of renaming CCD
  - MLZ - The name will be changed from N-METHYL-LYSINE to N6-METHYL-LYSINE,
  - Its current name is misleading, implying that the methylation occurs on the backbone 
  nitrogen rather than the sidechain nitrogen atom.

### Changing CCD Parents
- Example of changing parent
  -SOQ is the CCD that describes N-METHYL-ASPARTIC ACID, however it is currently 
  annotated as not having a parent residue. It is a natural modification to Aspartic acid 
  and so the parent residue will be changed to ASP.

## Acknowledgements
The protein chemical modifications (PCMs) and post translational modifications (PTMs) 
remediation project is a wwPDB collaborative project carried out principally by 
[PDBe](https://www.ebi.ac.uk/pdbe/) at [EMBL-EBI](https://www.ebi.ac.uk/), and is funded 
by BBSRC grant number BB/V018779/1.
