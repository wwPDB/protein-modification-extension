# New item types

#### uniprot_ptm_id

```
UniProt PTM List Accession ID Pattern - PTM-XXXX
```

| Code           | Primitive code | Construct    | Detail                                           |
|----------------|----------------|--------------|--------------------------------------------------|
| uniprot_ptm_id | char           | PTM-[0-9]{4} | UniProt PTM List Accession ID Pattern - PTM-XXXX |

# Category Group chem_comp_group

```
Categories that define the chemical structure and nomenclature of the momoners and ligands in the experiment.
```

## Category chem_comp

#### _chem_comp.pdbx_pcm

```
A flag to indicate if the CCD  can be used to represent a protein modification.
```

| Attribute | Key | Required | Type | Units | Enumerated | Bounded |
|-----------|-----|----------|------|-------|------------|---------|
| pdbx_pcm  | no  | no       | code | None  | yes        | no      |

| Allowed Values | Detail                                                        |
|----------------|---------------------------------------------------------------|
| Y              | Yes - Can be used to represent a protein modification         |
| N              | No - Should never be used to represent a protein modification |

## Category chem_comp_atom

#### _chem_comp.pdbx_backbone_atom_flag

```
A flag indicating the backbone atoms in polypeptide units.
```

| Attribute               | Key | Required | Type | Units | Enumerated | Bounded |
|-------------------------|-----|----------|------|-------|------------|---------|
| pdbx_backbone_atom_flag | no  | no       | code | None  | yes        | no      |

| Allowed Values | Detail                                     |
|----------------|--------------------------------------------|
| Y              | Yes - a part of the polypeptide backbone   |
| N              | No  - not part of the polypeptide backbone |

#### _chem_comp.pdbx_n_terminal_atom_flag

```
A flag indicating the N-terminal group atoms in polypeptide units.
```

| Attribute                 | Key | Required | Type | Units | Enumerated | Bounded |
|---------------------------|-----|----------|------|-------|------------|---------|
| pdbx_n_terminal_atom_flag | no  | no       | code | None  | yes        | no      |


| Allowed Values | Detail                                 |
|----------------|----------------------------------------|
| Y              | Yes - a part of the N-terminal group   |
| N              | No  - not part of the N-terminal group |


#### _chem_comp.pdbx_c_terminal_atom_flag

```
A flag indicating the C-terminal group atoms in polypeptide units.
```

| Attribute                 | Key | Required | Type | Units | Enumerated | Bounded |
|---------------------------|-----|----------|------|-------|------------|---------|
| pdbx_c_terminal_atom_flag | no  | no       | code | None  | yes        | no      |


| Allowed Values | Detail                                 |
|----------------|----------------------------------------|
| Y              | Yes - a part of the C-terminal group   |
| N              | No  - not part of the C-terminal group |


## Category pdbx_chem_comp_pcm

```
Data items in the PDBX_CHEM_COMP_PCM category provide information about the 
protein modifications that are described by the chemical component.
```

Example 1:
```
loop_
_pdbx_chem_comp_pcm.pcm_id                                        
_pdbx_chem_comp_pcm.comp_id 			
_pdbx_chem_comp_pcm.modified_residue_id
_pdbx_chem_comp_pcm.type                                             
_pdbx_chem_comp_pcm.category                                      
_pdbx_chem_comp_pcm.position                             
_pdbx_chem_comp_pcm.polypeptide_position 
_pdbx_chem_comp_pcm.comp_id_linking_atom
_pdbx_chem_comp_pcm.modified_residue_id_linking_atom
_pdbx_chem_comp_pcm.uniprot_specific_ptm_accession
_pdbx_chem_comp_pcm.uniprot_generic_ptm_accession
1 SEP SER Phosphorylation "Named protein modification" "Amino-acid side chain" "Any position" . . PTM-0253 ?
```

Example 2:
```
loop_
_pdbx_chem_comp_pcm.pcm_id                                        
_pdbx_chem_comp_pcm.comp_id 			
_pdbx_chem_comp_pcm.modified_residue_id
_pdbx_chem_comp_pcm.type                                             
_pdbx_chem_comp_pcm.category                                      
_pdbx_chem_comp_pcm.position                             
_pdbx_chem_comp_pcm.polypeptide_position 
_pdbx_chem_comp_pcm.comp_id_linking_atom
_pdbx_chem_comp_pcm.modified_residue_id_linking_atom
_pdbx_chem_comp_pcm.uniprot_specific_ptm_accession
_pdbx_chem_comp_pcm.uniprot_generic_ptm_accession
1 FUC SER . Carbohydrate "Amino-acid side chain" "Any position" C1 OG  ? ? 
2 FUC THR . Carbohydrate "Amino-acid side chain" "Any position" C1 OG1 ? ?
```

| Attribute                        | Key | Required | Type           | Units | Enumerated | Bounded |
|----------------------------------|-----|----------|----------------|-------|------------|---------|
| pcm_id                           | yes | yes      | int            | None  | no         | no      |
| comp_id                          | no  | yes      | ucode          | None  | no         | no      |
| modified_residue_id              | no  | no       | uline          | None  | no         | no      |
| type                             | no  | no       | line           | None  | yes        | no      |
| category                         | no  | yes      | line           | None  | yes        | no      |
| position                         | no  | yes      | line           | None  | yes        | no      |
| polypeptide_position             | no  | yes      | line           | None  | yes        | no      |
| comp_id_linking_atom             | no  | no       | atcode         | None  | no         | no      |
| modified_residue_id_linking_atom | no  | no       | atcode         | None  | no         | no      |
| uniprot_specific_ptm_accession   | no  | no       | uniprot_ptm_id | None  | no         | no      |
| uniprot_generic_ptm_accession    | no  | no       | uniprot_ptm_id | None  | no         | no      |

#### _pdbx_chem_comp_pcm.pcm_id

```
An ordinal index for this category.
```

#### _pdbx_chem_comp_pcm.comp_id

```
Chemical component identifier for the CCD that contains the modification group.
```

#### _pdbx_chem_comp_pcm.modified_residue_id

```
Chemical component identifier for the amino acid residue that is being modified.
```

#### _pdbx_chem_comp_pcm.type

```
The type of protein modification.
```

| Allowed Values   | Details |
|------------------|---------|
| ADP-ribosylation | .       |
| AMPylation       | .       |
| Acetamidation    | .       |
| Acetylation      | .       |
| Allysine         | .       |
 | ...              | .       |
| Sulfonation      | .       |
| Tert-butylation  | .       |
| Thyroxine        | .       |
| Triiodothyronine | .       |
| UMPylation       | .       |

#### _pdbx_chem_comp_pcm.category

```
The category of protein modification.
```

| Allowed Values                 | Details                                                                                                                                                                                                                                                                                                        |
|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ADP-Ribose                     | ADP-ribose protein modifications                                                                                                                                                                                                                                                                               |
| Biotin                         | Biotin protein modifications                                                                                                                                                                                                                                                                                   |
| Carbohydrate                   | Carbohydrate protein modifications                                                                                                                                                                                                                                                                             |
| Chromophore/chromophore-like   | Chromophore or chromophore-like protein modifications                                                                                                                                                                                                                                                          |
| Covalent chemical modification | A diverse range of chemical compounds that form covalent bonds with amino acids. Not covered by any of the other modification categories                                                                                                                                                                       |
| Crosslinker                    | Chemical modifications which covalently link two amino-acid residues. Excludes reaction intermediates and modifications covered by other modification categories                                                                                                                                               |
| Disulfide bridge               | Disulfide bridge protein modifications                                                                                                                                                                                                                                                                         |
| Flavin                         | Flavin protein modifications                                                                                                                                                                                                                                                                                   |
| Heme/heme-like                 | Heme or heme-like protein modifications                                                                                                                                                                                                                                                                        |
| Isopeptide bond                | Isopeptide bond protein modifications                                                                                                                                                                                                                                                                          |
| Lipid/lipid-like               | Lipid or lipid-like protein modifications                                                                                                                                                                                                                                                                      |
| Named protein modification     | All protein modifications that are well defined into known types, have limited diversity, and are not explicitly covered by any other category. It includes PTMs, PCMs, rare amino acids and unnatural amino acids                                                                                             |
| Non-standard linkage           | Non-standard covalent chemical linkages directly between two polypeptide residues                                                                                                                                                                                                                              |
| Non-standard residue           | A diverse range of non-standard polypeptide residues that are not considered to be 'Named protein modifications'. These cannot be practically split into two CCDs, which describe the standard polypeptide residue and the modification group, and are not covered by any of the other modification categories |
| Nucleotide monophosphate       | Nucleotide monophosphate protein modifications                                                                                                                                                                                                                                                                 |
| Terminal acetylation           | Terminal acetylation protein modification                                                                                                                                                                                                                                                                      |
| Terminal amidation             | Terminal amidation protein modification                                                                                                                                                                                                                                                                        |

#### _pdbx_chem_comp_pcm.position

```
The position of the modification on the amino acid.
```

| Allowed Values                     | Detail                                                                     |
|------------------------------------|----------------------------------------------------------------------------|
| Amino-acid side chain              | Protein modification occurs on the amino acid side chain                   |
| Amino-acid backbone                | Protein modification occurs on the amino acid backbone                     |
| Amino-acid side chain and backbone | Protein modification occurs on both the amino acid side chain and backbone |

#### _pdbx_chem_comp_pcm.polypeptide_position

```
The position of the modification on the polypeptide.
```

| Allowed Values | Detail                                                                     |
|----------------|----------------------------------------------------------------------------|
| C-terminal     | Protein modification can only occur on C-terminus                          |
| N-terminal     | Protein modification can only occur on N-terminus                          |
| Any position   | Protein modification can occur in any position of the polypeptide sequence |

#### _pdbx_chem_comp_pcm.comp_id_linking_atom

```
The atom on the modification group that covalently links the 
modification to the residue that is being modified. This is 
only added when the protein modification is linked and so the 
amino acid group and the modification group are described by 
separate CCDs.
```

#### _pdbx_chem_comp_pcm.modified_residue_id_linking_atom

```
The atom on the polypeptide residue group that covalently links 
the modification to the residue that is being modified. This is 
only added when the protein modification is linked and so the 
amino acid group and the modification group are described by 
separate CCDs.
```

#### _pdbx_chem_comp_pcm.uniprot_specific_ptm_accession

```
The UniProt PTM accession code that is an exact match for the protein modification.
```

#### _pdbx_chem_comp_pcm.uniprot_generic_ptm_accession

```
The UniProt PTM accession code that describes the group of PTMs of which this protein modification is a member.
```

# Category Group entry_group

## Category pdbx_entry_details

#### _pdbx_entry_details.has_protein_modification

```
A flag to indicate if the model contains any protein modifications.
```

| Attribute                | Key | Required | Type | Units | Enumerated | Bounded |
|--------------------------|-----|----------|------|-------|------------|---------|
| has_protein_modification | no  | no       | code | None  | yes        | no      |

| Allowed Values | Detail                       |
|----------------|------------------------------|
| Y              | Protein modification present |

# Category Group struct_group

## Category pdbx_chem_comp_pcm

```
Data items in the PDBX_MODIFICATION_FEATURE category provides 
information about all the protein modifications that have been 
modeled in the entry.
```

Example 1 - An example of the category in an entry that contains a disulfide bridge and 
two phosphoserine modifications.

```
loop_
_pdbx_modification_feature.ordinal
_pdbx_modification_feature.label_comp_id
_pdbx_modification_feature.label_asym_id
_pdbx_modification_feature.label_seq_id
_pdbx_modification_feature.modified_residue_label_comp_id
_pdbx_modification_feature.modified_residue_label_asym_id
_pdbx_modification_feature.modified_residue_label_seq_id
_pdbx_modification_feature.auth_comp_id
_pdbx_modification_feature.auth_asym_id
_pdbx_modification_feature.auth_seq_id
_pdbx_modification_feature.PDB_ins_code
_pdbx_modification_feature.modified_residue_auth_comp_id
_pdbx_modification_feature.modified_residue_auth_asym_id
_pdbx_modification_feature.modified_residue_auth_seq_id
_pdbx_modification_feature.modified_residue_PDB_ins_code
_pdbx_modification_feature.comp_id_linking_atom
_pdbx_modification_feature.modified_residue_id_linking_atom
_pdbx_modification_feature.modified_residue_id
_pdbx_modification_feature.ref_pcm_id
_pdbx_modification_feature.ref_comp_id
_pdbx_modification_feature.type
_pdbx_modification_feature.category
_pdbx_modification_feature.biological_function
_pdbx_modification_feature.biological_function_details
1 CYS B 46 CYS A 46 CYS B 46 ? CYS A 46 ? SG SG .   . .   .               Disulfide bridge             ? ?
2 SEP A 65 .   . .  SEP A 65 ? .   . .  . .  .  SER 1 SEP Phosphorylation 'Named protein modification' ? ?
3 SEP B 65 .   . .  SEP B 65 ? .   . .  . .  .  SER 1 SEP Phosphorylation 'Named protein modification' ? ?
```

Example 2 - An example of the category in an entry that contains a two cysteine 
hydroxylation modification sites and two palmitoylation modification sites.

```
loop_
_pdbx_modification_feature.ordinal
_pdbx_modification_feature.label_comp_id
_pdbx_modification_feature.label_asym_id
_pdbx_modification_feature.label_seq_id
_pdbx_modification_feature.modified_residue_label_comp_id
_pdbx_modification_feature.modified_residue_label_asym_id
_pdbx_modification_feature.modified_residue_label_seq_id
_pdbx_modification_feature.auth_comp_id
_pdbx_modification_feature.auth_asym_id
_pdbx_modification_feature.auth_seq_id
_pdbx_modification_feature.PDB_ins_code
_pdbx_modification_feature.modified_residue_auth_comp_id
_pdbx_modification_feature.modified_residue_auth_asym_id
_pdbx_modification_feature.modified_residue_auth_seq_id
_pdbx_modification_feature.modified_residue_PDB_ins_code
_pdbx_modification_feature.comp_id_linking_atom
_pdbx_modification_feature.modified_residue_id_linking_atom
_pdbx_modification_feature.modified_residue_id
_pdbx_modification_feature.ref_pcm_id
_pdbx_modification_feature.ref_comp_id
_pdbx_modification_feature.type
_pdbx_modification_feature.category
_pdbx_modification_feature.biological_function
_pdbx_modification_feature.biological_function_details
1 CSO C 32 .   . .  CSO C 32   ? .   . .  . .  .  CYS 1 CSO Hydroxylation  'Named protein modification' ? ?
2 CSO D 32 .   . .  CSO D 32   ? .   . .  . .  .  CYS 1 CSO Hydroxylation  'Named protein modification' ? ?
3 PLM E .  CYS A 82 PLM A 1068 ? CYS A 68 ? C1 SG CYS 6 PLM Palmitoylation 'Lipid/lipid-like'           ? ?
4 PLM F .  CYS B 82 PLM B 1068 ? CYS B 68 ? C1 SG CYS 6 PLM Palmitoylation 'Lipid/lipid-like'           ? ?
```

| Attribute                        | Key | Required | Type   | Units | Enumerated | Bounded |
|----------------------------------|-----|----------|--------|-------|------------|---------|
| ordinal                          | yes | yes      | int    | None  | no         | no      |
| label_comp_id                    | no  | yes      | ucode  | None  | no         | no      |
| label_asym_id                    | no  | yes      | code   | None  | no         | no      |
| label_seq_id                     | no  | no       | int    | None  | no         | no      |
| modified_residue_label_comp_id   | no  | no       | ucode  | None  | no         | no      |
| modified_residue_label_asym_id   | no  | no       | code   | None  | no         | no      |
| modified_residue_label_seq_id    | no  | no       | int    | None  | no         | no      |
| auth_comp_id                     | no  | no       | code   | None  | no         | no      |
| auth_asym_id                     | no  | no       | code   | None  | no         | no      |
| auth_seq_id                      | no  | no       | code   | None  | no         | no      |
| PDB_ins_code                     | no  | no       | code   | None  | no         | no      |
| symmetry                         | no  | no       | symop  | None  | no         | no      |
| modified_residue_auth_comp_id    | no  | no       | code   | None  | no         | no      |
| modified_residue_auth_asym_id    | no  | no       | code   | None  | no         | no      |
| modified_residue_auth_seq_id     | no  | no       | code   | None  | no         | no      |
| modified_residue_PDB_ins_code    | no  | no       | code   | None  | no         | no      |
| modified_residue_symmetry        | no  | no       | symop  | None  | no         | no      |
| comp_id_linking_atom             | no  | no       | atcode | None  | no         | no      |
| modified_residue_id_linking_atom | no  | no       | atcode | None  | no         | no      |
| modified_residue_id              | no  | no       | uline  | None  | no         | no      |
| ref_pcm_id                       | no  | no       | int    | None  | no         | no      |
| ref_comp_id                      | no  | no       | ucode  | None  | no         | no      |
| type                             | no  | no       | line   | None  | yes        | no      |
| category                         | no  | yes      | line   | None  | yes        | no      |
| biological_function              | no  | no       | code   | None  | yes        | no      |
| biological_function_details      | no  | no       | text   | None  | no         | no      |

#### _pdbx_chem_comp_pcm.ordinal

```
An ordinal index for this category.
```

#### _pdbx_chem_comp_pcm.label_comp_id

```
A component of the identifier for the chemical component that 
describes the protein modification.

This data item is a pointer to _atom_site.label_comp_id in the 
ATOM_SITE category.
```

#### _pdbx_chem_comp_pcm.label_asym_id

```
A component of the identifier for the chemical component that 
describes the protein modification.

This data item is a pointer to _atom_site.label_asym_id in the 
ATOM_SITE category.
```

#### _pdbx_chem_comp_pcm.label_seq_id

```
A component of the identifier for the chemical component that 
describes the protein modification.

This data item is a pointer to _atom_site.label_seq_id in the 
ATOM_SITE category.
```

#### _pdbx_chem_comp_pcm.modified_residue_label_comp_id

```
A component of the identifier for the chemical component that 
is being modified.

This data item is a pointer to _atom_site.label_comp_id in the 
ATOM_SITE category.
```

#### _pdbx_chem_comp_pcm.modified_residue_label_asym_id

```
A component of the identifier for the chemical component that 
is being modified.

This data item is a pointer to _atom_site.label_asym_id in the 
ATOM_SITE category.
```

#### _pdbx_chem_comp_pcm.modified_residue_label_seq_id

```
A component of the identifier for the chemical component that 
is being modified.

This data item is a pointer to _atom_site.label_seq_id in the 
ATOM_SITE category.
```

#### _pdbx_chem_comp_pcm.auth_comp_id

```
A component of the identifier for the chemical component that 
describes the protein modification.

This data item is a pointer to _atom_site.auth_comp_id in the 
ATOM_SITE category.
```

#### _pdbx_chem_comp_pcm.auth_asym_id

```
A component of the identifier for the chemical component that 
describes the protein modification.

This data item is a pointer to _atom_site.auth_asym_id in the 
ATOM_SITE category.
```

#### _pdbx_chem_comp_pcm.auth_seq_id

```
A component of the identifier for the chemical component that 
describes the protein modification.

This data item is a pointer to _atom_site.auth_seq_id in the 
ATOM_SITE category.
```

#### _pdbx_chem_comp_pcm.PDB_ins_code

```
A component of the identifier for the chemical component that 
describes the protein modification.

This data item is a pointer to _atom_site.pdbx_PDB_ins_code in the 
ATOM_SITE category.
```

#### _pdbx_chem_comp_pcm.modified_residue_auth_comp_id

```
A component of the identifier for the chemical component that 
is being modified.

This data item is a pointer to _atom_site.auth_comp_id in the 
ATOM_SITE category.
```

#### _pdbx_chem_comp_pcm.modified_residue_auth_asym_id

```
A component of the identifier for the chemical component that 
is being modified.

This data item is a pointer to _atom_site.auth_asym_id in the 
ATOM_SITE category.
```

#### _pdbx_chem_comp_pcm.modified_residue_auth_seq_id

```
A component of the identifier for the chemical component that 
is being modified.

This data item is a pointer to _atom_site.auth_seq_id in the 
ATOM_SITE category.
```

#### _pdbx_chem_comp_pcm.modified_residue_PDB_ins_code

```
A component of the identifier for the chemical component that 
is being modified.

This data item is a pointer to _atom_site.pdbx_PDB_ins_code in the 
ATOM_SITE category.
```

#### _pdbx_chem_comp_pcm.comp_id_linking_atom

```
The atom on the modification group that covalently links the 
modification to the residue that is being modified. This is 
only added when the protein modification is linked and so the 
amino acid group and the modification group are described by 
separate CCDs.
```

#### _pdbx_chem_comp_pcm.modified_residue_id_linking_atom

```
The atom on the polypeptide residue group that covalently links 
the modification to the residue that is being modified. This is 
only added when the protein modification is linked and so the 
amino acid group and the modification group are described by 
separate CCDs.
```

#### _pdbx_chem_comp_pcm.modified_residue_id

```
Chemical component identifier for the amino acid residue that is being modified.
```

#### _pdbx_chem_comp_pcm.ref_pcm_id

```
A component of the identifier for the unique kind of protein 
modification.

This data item is a pointer to _pdbx_chem_comp_pcm.pcm_id in the 
CHEM_COMP_PCM category.
```

#### _pdbx_chem_comp_pcm.ref_comp_id

```
A component of the identifier for the unique kind of protein 
modification.

This data item is a pointer to _pdbx_chem_comp_pcm.comp_id in the 
CHEM_COMP_PCM category.
```

#### _pdbx_chem_comp_pcm.type

```
The type of protein modification.
```

| Allowed Values   | Details |
|------------------|---------|
| ADP-ribosylation | .       |
| AMPylation       | .       |
| Acetamidation    | .       |
| Acetylation      | .       |
| Allysine         | .       |
 | ...              | .       |
| Sulfonation      | .       |
| Tert-butylation  | .       |
| Thyroxine        | .       |
| Triiodothyronine | .       |
| UMPylation       | .       |

#### _pdbx_chem_comp_pcm.category

```
The category of protein modification.
```

| Allowed Values                 | Details                                                                                                                                                                                                                                                                                                        |
|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ADP-Ribose                     | ADP-ribose protein modifications                                                                                                                                                                                                                                                                               |
| Biotin                         | Biotin protein modifications                                                                                                                                                                                                                                                                                   |
| Carbohydrate                   | Carbohydrate protein modifications                                                                                                                                                                                                                                                                             |
| Chromophore/chromophore-like   | Chromophore or chromophore-like protein modifications                                                                                                                                                                                                                                                          |
| Covalent chemical modification | A diverse range of chemical compounds that form covalent bonds with amino acids. Not covered by any of the other modification categories                                                                                                                                                                       |
| Crosslinker                    | Crosslinker protein modifications                                                                                                                                                                                                                                                                              |
| Disulfide bridge               | Disulfide bridge protein modifications                                                                                                                                                                                                                                                                         |
| Flavin                         | Flavin protein modifications                                                                                                                                                                                                                                                                                   |
| Heme/heme-like                 | Heme or heme-like protein modifications                                                                                                                                                                                                                                                                        |
| Isopeptide bond                | Isopeptide bond protein modifications                                                                                                                                                                                                                                                                          |
| Lipid/lipid-like               | Lipid or lipid-like protein modifications                                                                                                                                                                                                                                                                      |
| Named protein modification     | All protein modifications that are well defined into known types, have limited diversity, and are not explicitly covered by any other category. It includes PTMs, PCMs, rare amino acids and unnatural amino acids                                                                                             |
| Non-standard linkage           | Non-standard covalent chemical linkages directly between two polypeptide residues                                                                                                                                                                                                                              |
| Non-standard residue           | A diverse range of non-standard polypeptide residues that are not considered to be 'Named protein modifications'. These cannot be practically split into two CCDs, which describe the standard polypeptide residue and the modification group, and are not covered by any of the other modification categories |
| Nucleotide monophosphate       | Nucleotide monophosphate protein modifications                                                                                                                                                                                                                                                                 |
| Terminal acetylation           | Terminal acetylation protein modification                                                                                                                                                                                                                                                                      |
| Terminal amidation             | Terminal amidation protein modification                                                                                                                                                                                                                                                                        |

#### _pdbx_chem_comp_pcm.biological_function

```
A flag to indicate if the protein modification at this site can 
occur naturally and that it is expected to have a biological 
function.
```

| Allowed Values | Detail                                                   |
|----------------|----------------------------------------------------------|
| Y              | Protein modification has a biological function           |
| N              | Protein modification does not have a biological function |

#### _pdbx_chem_comp_pcm.biological_function_details

```
Details of the biological function of the protein modification at this site.
```