# Category Group chem_comp_group


              Categories that define the chemical structure and nomenclature of the momoners and ligands in the experiment.

---

## Category pdbx_chem_comp_atom_related


 PDBX_CHEM_COMP_ATOM_RELATED provides atom level nomenclature mapping between two related chemical components.

---


```
     
         Example 1 -
     
         loop_      
         _pdbx_chem_comp_atom_related.ordinal
         _pdbx_chem_comp_atom_related.comp_id
         _pdbx_chem_comp_atom_related.atom_id
         _pdbx_chem_comp_atom_related.related_comp_id
         _pdbx_chem_comp_atom_related.related_atom_id
         _pdbx_chem_comp_atom_related.related_type
          1 SGN C1    GLC C1   'Carbohydrate core'
          2 SGN C2    GLC C2   'Carbohydrate core'
          3 SGN C3    GLC C3   'Carbohydrate core'
          4 SGN C4    GLC C4   'Carbohydrate core'
          5 SGN C5    GLC C5   'Carbohydrate core'
          6 SGN C6    GLC C6   'Carbohydrate core'
          7 SGN N     GLC ?    'Carbohydrate core'
          8 SGN O1    GLC O1   'Carbohydrate core'
          9 SGN O3    GLC O3   'Carbohydrate core'
         10 SGN O4    GLC O4   'Carbohydrate core'
         11 SGN O5    GLC O5   'Carbohydrate core'
         12 SGN O6    GLC O6   'Carbohydrate core'
         13 SGN S1    GLC ?    'Carbohydrate core'
         14 SGN O1S   GLC ?    'Carbohydrate core'
         15 SGN O2S   GLC ?    'Carbohydrate core'
         16 SGN O3S   GLC ?    'Carbohydrate core'
         17 SGN S2    GLC ?    'Carbohydrate core'
         18 SGN O4S   GLC ?    'Carbohydrate core'
         19 SGN O5S   GLC ?    'Carbohydrate core'
         20 SGN O6S   GLC ?    'Carbohydrate core'
         21 SGN H1    GLC H1   'Carbohydrate core'
         22 SGN H2    GLC H2   'Carbohydrate core'
         23 SGN H3    GLC H3   'Carbohydrate core'
         24 SGN H4    GLC H4   'Carbohydrate core'
         25 SGN H5    GLC H5   'Carbohydrate core'
         26 SGN H61   GLC H61  'Carbohydrate core'
         27 SGN H62   GLC H62  'Carbohydrate core'
         28 SGN HN    GLC ?    'Carbohydrate core'
         29 SGN HO1   GLC HO1  'Carbohydrate core'
         30 SGN HO3   GLC HO3  'Carbohydrate core'
         31 SGN HO4   GLC HO4  'Carbohydrate core'
         32 SGN HOS3  GLC ?    'Carbohydrate core'
         33 SGN HOS6  GLC ?    'Carbohydrate core'
         #
```


---

| Attribute | Key | Required | Type | Units | Enumerated | Bounded |
| --------- | --- | -------- | ---- | ----- | ---------- | ------- |
| atom_id | no | yes | atcode | None | no | no |
| comp_id | yes | yes | ucode | None | no | no |
| ordinal | yes | yes | int | None | no | no |
| related_atom_id | no | no | atcode | None | no | no |
| related_comp_id | yes | yes | ucode | None | no | no |
| related_type | no | yes | line | None | yes | no |

---

#### _pdbx_chem_comp_atom_related.atom_id (required)


               The atom identifier/name for the atom mapping




#### _pdbx_chem_comp_atom_related.comp_id (key)


 The chemical component for which this relationship applies.



#### _pdbx_chem_comp_atom_related.ordinal (key)


 
               An ordinal index for this category



#### _pdbx_chem_comp_atom_related.related_atom_id


               The atom identifier/name for the atom mapping in the related chemical component



#### _pdbx_chem_comp_atom_related.related_comp_id (key)


 The related chemical component for which this chemical component is based.



#### _pdbx_chem_comp_atom_related.related_type (required)


 Describes the type of relationship



---

| Allowed Values | Detail |
| -------------- | ------ |
| Carbohydrate core | References a core carbohydrate structure |
| Precursor | The related component is a precursor for this one |


## Category pdbx_chem_comp_related


 PDBX_CHEM_COMP_RELATED describes the relationship between two chemical components.

---


```
     
         Example 1 -
     
         _pdbx_chem_comp_related.comp_id             SGN
         _pdbx_chem_comp_related.related_comp_id     GLC
         _pdbx_chem_comp_related.relationship_type   "Carbohydrate core"
         _pdbx_chem_comp_related.details             ?
```


---

| Attribute | Key | Required | Type | Units | Enumerated | Bounded |
| --------- | --- | -------- | ---- | ----- | ---------- | ------- |
| comp_id | yes | yes | ucode | None | no | no |
| details | no | no | text | None | no | no |
| related_comp_id | yes | yes | ucode | None | no | no |
| relationship_type | yes | yes | line | None | yes | no |

---

#### _pdbx_chem_comp_related.comp_id (key)


 The chemical component for which this relationship applies.



#### _pdbx_chem_comp_related.details


 Describes the type of relationship



#### _pdbx_chem_comp_related.related_comp_id (key)


 The related chemical component for which this chemical component is based.



#### _pdbx_chem_comp_related.relationship_type (key)


 Describes the type of relationship



---

| Allowed Values | Detail |
| -------------- | ------ |
| Carbohydrate core | References a common core carbohydrate structure |
| Precursor | The related component is a precursor for this one |


## Category pdbx_chem_comp_synonyms


 PDBX_CHEM_COMP_SYNONYMS holds chemical name and synonym correspondences.

---


```
     
         Example 1 -
     
         loop_
         _pdbx_chem_comp_synonyms.comp_id
         _pdbx_chem_comp_synonyms.name 
         _pdbx_chem_comp_synonyms.provenance
         ROC  Fortovase       DRUGBANK
         ROC  SAQUINAVIR      DRUGBANK
         ROC  "RO 31-8959"    ?
```


---

| Attribute | Key | Required | Type | Units | Enumerated | Bounded |
| --------- | --- | -------- | ---- | ----- | ---------- | ------- |
| comp_id | yes | yes | ucode | None | no | no |
| name | yes | yes | text | None | no | no |
| provenance | no | no | line | None | yes | no |

---

#### _pdbx_chem_comp_synonyms.comp_id (key)


 The chemical component for which this synonym applies.



#### _pdbx_chem_comp_synonyms.name (key)


 The synonym of this particular chemical component.



#### _pdbx_chem_comp_synonyms.provenance


 The provenance of this synonym.



---

| Allowed Values | Detail |
| -------------- | ------ |
| AUTHOR | . |
| CHEBI | . |
| CHEMBL | . |
| DRUGBANK | . |
| PDB | . |
| PUBCHEM | . |


