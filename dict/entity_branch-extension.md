# Category Group branch_group


              Categories that describe branched chain carbohydrates.

---

## Category pdbx_branch_scheme


               The PDBX_BRANCH_SCHEME category provides residue level nomenclature
  	       mapping for branch chain entities.

---


```
     
         Example 1 -
     
          loop_
          _pdbx_branch_scheme.asym_id 
          _pdbx_branch_scheme.entity_id 
          _pdbx_branch_scheme.mon_id 
          _pdbx_branch_scheme.num
          _pdbx_branch_scheme.pdb_asym_id 
          _pdbx_branch_scheme.pdb_mon_id 
          _pdbx_branch_scheme.pdb_seq_num 
          _pdbx_branch_scheme.auth_asym_id 
          _pdbx_branch_scheme.auth_mon_id 
          _pdbx_branch_scheme.auth_seq_num 
          _pdbx_branch_scheme.hetero 
          B  2 NAG 1 B NAG 1  NAG A 1592 n
          B  2 GAL 2 B GAL 2  GAL A 1591 n
          B  2 FUC 3 B FUC 3  FUC A 1590 n
          B  2 FUC 4 B FUC 4  FUC A 1593 n
```


---

| Attribute | Key | Required | Type | Units | Enumerated | Bounded |
| --------- | --- | -------- | ---- | ----- | ---------- | ------- |
| asym_id | yes | yes | code | None | no | no |
| auth_asym_id | no | no | code | None | no | no |
| auth_mon_id | no | no | code | None | no | no |
| auth_seq_num | no | no | code | None | no | no |
| entity_id | yes | yes | code | None | no | no |
| hetero | no | no | ucode | None | yes | no |
| mon_id | yes | yes | ucode | None | no | no |
| num | yes | yes | int | None | no | yes |
| pdb_asym_id | no | yes | code | None | no | no |
| pdb_mon_id | no | yes | code | None | no | no |
| pdb_seq_num | no | yes | code | None | no | no |

---

#### _pdbx_branch_scheme.asym_id (key)


     Pointer to _atom_site.label_asym_id.



#### _pdbx_branch_scheme.auth_asym_id


               This data item is a pointer to _atom_site.pdbx_auth_asym_id in the
               ATOM_SITE category.



#### _pdbx_branch_scheme.auth_mon_id


               This data item is a pointer to _atom_site.pdbx_auth_comp_id in the
               ATOM_SITE category.



#### _pdbx_branch_scheme.auth_seq_num


               This data item is a pointer to _atom_site.pdbx_auth_seq_id in the
               ATOM_SITE category.



#### _pdbx_branch_scheme.entity_id (key)


               This data item is a pointer to _entity.id in the ENTITY category.



#### _pdbx_branch_scheme.hetero


               A flag to indicate whether this monomer in the entity is
               heterogeneous in sequence.



---

| Allowed Values | Detail |
| -------------- | ------ |
| n | abbreviation for "no" |
| no | sequence is not heterogeneous at this monomer |
| y | abbreviation for "yes" |
| yes | sequence is heterogeneous at this monomer |


#### _pdbx_branch_scheme.mon_id (key)


               This data item is a pointer to _atom_site.label_comp_id in the
               PDBX_ENTITY_BRANCH_LIST category.



#### _pdbx_branch_scheme.num (key)


               This data item is a pointer to _pdbx_entity_branch_list.num in the
               PDBX_ENTITY_BRANCH_LIST category.





---

| Minimum&nbsp;Value | Maximum&nbsp;Value |
| ------------- | ------ |
| 1 | <h3>+&infin;</h3> |


#### _pdbx_branch_scheme.pdb_asym_id (required)


               This data item is a pointer to _atom_site.auth_asym_id in the
               ATOM_SITE category.



#### _pdbx_branch_scheme.pdb_mon_id (required)


               This data item is a pointer to _atom_site.auth_comp_id in the
               ATOM_SITE category.



#### _pdbx_branch_scheme.pdb_seq_num (required)


               This data item is a pointer to _atom_site.auth_seq_id in the
               ATOM_SITE category.



## Category pdbx_entity_branch


               Data items in the PDBX_ENTITY_BRANCH category specify the list
               of branched entities and the type.

---


```
     
         Example 1 -
     
         loop_
         _pdbx_entity_branch.entity_id
         _pdbx_entity_branch.type
           2  oligosaccharide
```


---

| Attribute | Key | Required | Type | Units | Enumerated | Bounded |
| --------- | --- | -------- | ---- | ----- | ---------- | ------- |
| entity_id | yes | yes | code | None | no | no |
| type | no | yes | code | None | yes | no |

---

#### _pdbx_entity_branch.entity_id (key)


               The entity id for this branched entity. 

               This data item is a pointer to _entity.id



#### _pdbx_entity_branch.type (required)


               The type of this branched oligosaccharide.



---

| Allowed Values | Detail |
| -------------- | ------ |
| oligosaccharide | . |


## Category pdbx_entity_branch_link


               Data items in the PDBX_ENTITY_BRANCH_LINK category give details about
               the linkages between components within a branched entity.

---


```
     
         Example 1 - based on PDB entry 2WMG
     
         loop_
         _pdbx_entity_branch_link.link_id 
         _pdbx_entity_branch_link.entity_id
         _pdbx_entity_branch_link.entity_branch_list_num_1
         _pdbx_entity_branch_link.comp_id_1
         _pdbx_entity_branch_link.atom_id_1
         _pdbx_entity_branch_link.leaving_atom_id_1
         _pdbx_entity_branch_link.atom_stereo_config_1
         _pdbx_entity_branch_link.entity_branch_list_num_2
         _pdbx_entity_branch_link.comp_id_2
         _pdbx_entity_branch_link.atom_id_2
         _pdbx_entity_branch_link.leaving_atom_id_2
         _pdbx_entity_branch_link.atom_stereo_config_2
         _pdbx_entity_branch_link.value_order
         _pdbx_entity_branch_link.details
         1 2 1 NAG O4 HO4 ? 2 GAL C1 O1 R sing ?
         2 2 2 GAL O2 HO2 ? 3 FUC C1 O1 R sing ?
         3 2 1 NAG O3 HO3 ? 4 FUC C1 O1 R sing ?
```


---

| Attribute | Key | Required | Type | Units | Enumerated | Bounded |
| --------- | --- | -------- | ---- | ----- | ---------- | ------- |
| atom_id_1 | no | yes | atcode | None | no | no |
| atom_id_2 | no | yes | atcode | None | no | no |
| atom_stereo_config_1 | no | no | ucode | None | yes | no |
| atom_stereo_config_2 | no | no | ucode | None | yes | no |
| comp_id_1 | no | yes | code | None | no | no |
| comp_id_2 | no | yes | code | None | no | no |
| details | no | no | text | None | no | no |
| entity_branch_list_num_1 | no | yes | int | None | no | no |
| entity_branch_list_num_2 | no | yes | int | None | no | no |
| entity_id | no | yes | code | None | no | no |
| leaving_atom_id_1 | no | yes | atcode | None | no | no |
| leaving_atom_id_2 | no | yes | atcode | None | no | no |
| link_id | yes | yes | int | None | no | no |
| value_order | no | no | ucode | None | yes | no |

---

#### _pdbx_entity_branch_link.atom_id_1 (required)


               The atom identifier/name for the first atom making the linkage. 




#### _pdbx_entity_branch_link.atom_id_2 (required)


               The atom identifier/name for the second atom making the linkage. 




#### _pdbx_entity_branch_link.atom_stereo_config_1


               The chiral configuration of the first atom making the linkage.



---

| Allowed Values | Detail |
| -------------- | ------ |
| N | none |
| R | rectus - right handed configuration |
| S | sinister - left handed configuration |


#### _pdbx_entity_branch_link.atom_stereo_config_2


               The chiral configuration of the second atom making the linkage.



---

| Allowed Values | Detail |
| -------------- | ------ |
| N | none |
| R | rectus - right handed configuration |
| S | sinister - left handed configuration |


#### _pdbx_entity_branch_link.comp_id_1 (required)


               The component identifier for the first component making the linkage. 

               This data item is a pointer to _pdbx_entity_branch_list.comp_id 
               in the PDBX_ENTITY_BRANCH_LIST category.



#### _pdbx_entity_branch_link.comp_id_2 (required)


               The component identifier for the second component making the linkage. 

               This data item is a pointer to _pdbx_entity_branch_list.comp_id 
               in the PDBX_ENTITY_BRANCH_LIST category.



#### _pdbx_entity_branch_link.details


               A description of special aspects of this linkage.



#### _pdbx_entity_branch_link.entity_branch_list_num_1 (required)


               The component number for the first component making the linkage. 

               This data item is a pointer to _pdbx_entity_branch_list.num 
               in the PDBX_ENTITY_BRANCH_LIST category.




#### _pdbx_entity_branch_link.entity_branch_list_num_2 (required)


               The component number for the second component making the linkage. 

               This data item is a pointer to _pdbx_entity_branch_list.num 
               in the PDBX_ENTITY_BRANCH_LIST category.




#### _pdbx_entity_branch_link.entity_id (required)


               The entity id for this branched entity. 

               This data item is a pointer to _pdbx_entity_branch_list.entity_id  
               in the PDBX_ENTITY_BRANCH_LIST category.



#### _pdbx_entity_branch_link.leaving_atom_id_1 (required)


               The leaving atom identifier/name bonded to the first atom making the linkage. 




#### _pdbx_entity_branch_link.leaving_atom_id_2 (required)


               The leaving atom identifier/name bonded to the second atom making the linkage. 




#### _pdbx_entity_branch_link.link_id (key)


               The value of _pdbx_entity_branch_link.link_id uniquely identifies
               linkages within the branched entity.




#### _pdbx_entity_branch_link.value_order


               The bond order target for the chemical linkage.



---

| Allowed Values | Detail |
| -------------- | ------ |
| arom | aromatic bond |
| delo | delocalised double bond |
| doub | double bond |
| pi | pi bond |
| poly | polymeric bond |
| quad | quadruple bond |
| sing | single bond |
| trip | triple bond |


## Category pdbx_entity_branch_list


               Data items in the PDBX_ENTITY_BRANCH_LIST category specify the list
               of monomers in a branched entity.  Allowance is made for the possibility
               of microheterogeneity in a sample by allowing a given sequence
               number to be correlated with more than one monomer ID. The
               corresponding ATOM_SITE entries should reflect this
               heterogeneity.

---


```
     
         Example 1 -
     
          loop_
         _pdbx_entity_branch_list.entity_id
         _pdbx_entity_branch_list.num
         _pdbx_entity_branch_list.comp_id
         _pdbx_entity_branch_list.hetero
         2 1  NAG   n
         2 2  GAL   n
         2 3  FUC   n 
         2 4  FUC   n
```


---

| Attribute | Key | Required | Type | Units | Enumerated | Bounded |
| --------- | --- | -------- | ---- | ----- | ---------- | ------- |
| comp_id | yes | yes | ucode | None | no | no |
| entity_id | yes | yes | code | None | no | no |
| hetero | no | no | ucode | None | yes | no |
| num | yes | yes | int | None | no | yes |

---

#### _pdbx_entity_branch_list.comp_id (key)


               This data item is a pointer to _chem_comp.id in the CHEM_COMP
               category.



#### _pdbx_entity_branch_list.entity_id (key)


               This data item is a pointer to _entity.id in the ENTITY category.



#### _pdbx_entity_branch_list.hetero


               A flag to indicate whether this monomer in the entity is
               heterogeneous in sequence.



---

| Allowed Values | Detail |
| -------------- | ------ |
| n | abbreviation for "no" |
| no | sequence is not heterogeneous at this monomer |
| y | abbreviation for "yes" |
| yes | sequence is heterogeneous at this monomer |


#### _pdbx_entity_branch_list.num (key)


               The value pair  _pdbx_entity_branch_list.num and _pdbx_entity_branch_list.comp_id
               must uniquely identify a record in the PDBX_ENTITY_BRANCH_LIST list.




---

| Minimum&nbsp;Value | Maximum&nbsp;Value |
| ------------- | ------ |
| 1 | <h3>+&infin;</h3> |


## Category pdbx_entity_descriptor


               Data items in the PDBX_ENTITY_DESCRIPTOR category provide
               string descriptors of entity chemical structure.

---


```
     
         Example 1 -
     
         loop_
         _pdbx_entity_descriptor.ordinal
         _pdbx_entity_descriptor.entity_id
         _pdbx_entity_descriptor.descriptor
         _pdbx_entity_descriptor.type
         _pdbx_entity_descriptor.program
         _pdbx_entity_descriptor.program_version
     	1     1       
          '[][Asn]{[(4+1)][b-D-GlcpNAc]{[(4+1)][b-D-GlcpNAc]{[(4+1)][b-D-Manp]{[(3+1)][a-D-Manp]{[(2+1)][a-D-Manp]{[(2+1)][a-D-Manp]{}}}[(6+1)][a-D-Manp]{[(3+1)][a-D-Manp]{[(2+1)][a-D-Manp]{}}[(6+1)][a-D-Manp]{[(2+1)][a-D-Manp]{}}}}}}}'
                LINUCS           PDB-CARE Beta
```


---

| Attribute | Key | Required | Type | Units | Enumerated | Bounded |
| --------- | --- | -------- | ---- | ----- | ---------- | ------- |
| descriptor | no | yes | text | None | no | no |
| entity_id | no | yes | code | None | no | no |
| ordinal | yes | yes | int | None | no | no |
| program | no | no | line | None | no | no |
| program_version | no | no | line | None | no | no |
| type | no | yes | uline | None | yes | no |

---

#### _pdbx_entity_descriptor.descriptor (required)


               This data item contains the descriptor value for this 
               entity.



#### _pdbx_entity_descriptor.entity_id (required)


               This data item is a pointer to _entity_poly.entity_id in the ENTITY
               category.



#### _pdbx_entity_descriptor.ordinal (key)


               Ordinal index for this category.



#### _pdbx_entity_descriptor.program


               This data item contains the name of the program
               or library used to compute the descriptor.



#### _pdbx_entity_descriptor.program_version


               This data item contains the version of the program
               or library used to compute the descriptor.



#### _pdbx_entity_descriptor.type (required)


               This data item contains the descriptor type.



---

| Allowed Values | Detail |
| -------------- | ------ |
| Glycam Condensed Core Sequence | Linear Notation for Unique description of oligosaccharide core structure |
| Glycam Condensed Sequence | Linear Notation for unique description of an oligosaccharide entity |
| LINUCS | Linear Notation for unique description of an oligosaccharide entity |


## Category pdbx_entity_poly_comp_link_list


               Data items in the PDBX_ENTITY_POLY_COMP_LINK_LIST category enumerate the 
               the linkages between components within the polymer entity.

---


```
     
         Example 1 -
     
     loop_
     _pdbx_entity_poly_comp_link_list.link_id 
     _pdbx_entity_poly_comp_link_list.entity_id
     _pdbx_entity_poly_comp_link_list.entity_comp_num_1
     _pdbx_entity_poly_comp_link_list.comp_id_1
     _pdbx_entity_poly_comp_link_list.atom_id_1
     _pdbx_entity_poly_comp_link_list.leaving_atom_id_1
     _pdbx_entity_poly_comp_link_list.atom_stereo_config_1
     _pdbx_entity_poly_comp_link_list.entity_comp_num_2
     _pdbx_entity_poly_comp_link_list.comp_id_2
     _pdbx_entity_poly_comp_link_list.atom_id_2
     _pdbx_entity_poly_comp_link_list.leaving_atom_id_2
     _pdbx_entity_poly_comp_link_list.atom_stereo_config_2
     _pdbx_entity_poly_comp_link_list.value_order
     1 1  1 .  .  . .  2 .  .  . . 'sing'
```


---

| Attribute | Key | Required | Type | Units | Enumerated | Bounded |
| --------- | --- | -------- | ---- | ----- | ---------- | ------- |
| atom_id_1 | no | yes | atcode | None | no | no |
| atom_id_2 | no | yes | atcode | None | no | no |
| atom_stereo_config_1 | no | no | ucode | None | yes | no |
| atom_stereo_config_2 | no | no | ucode | None | yes | no |
| comp_id_1 | no | yes | ucode | None | no | no |
| comp_id_2 | no | yes | ucode | None | no | no |
| details | no | no | text | None | no | no |
| entity_comp_num_1 | no | yes | int | None | no | no |
| entity_comp_num_2 | no | yes | int | None | no | no |
| entity_id | no | yes | code | None | no | no |
| leaving_atom_id_1 | no | yes | atcode | None | no | no |
| leaving_atom_id_2 | no | yes | atcode | None | no | no |
| link_id | yes | yes | int | None | no | no |
| value_order | no | no | ucode | None | yes | no |

---

#### _pdbx_entity_poly_comp_link_list.atom_id_1 (required)


               The atom identifier/name for the first atom making the linkage. 




#### _pdbx_entity_poly_comp_link_list.atom_id_2 (required)


               The atom identifier/name for the second atom making the linkage. 




#### _pdbx_entity_poly_comp_link_list.atom_stereo_config_1


               The chiral configuration of the first atom making the linkage.



---

| Allowed Values | Detail |
| -------------- | ------ |
| N | none |
| R | rectus - right handed configuration |
| S | sinister - left handed configuration |


#### _pdbx_entity_poly_comp_link_list.atom_stereo_config_2


               The chiral configuration of the second atom making the linkage.



---

| Allowed Values | Detail |
| -------------- | ------ |
| N | none |
| R | rectus - right handed configuration |
| S | sinister - left handed configuration |


#### _pdbx_entity_poly_comp_link_list.comp_id_1 (required)


               The component identifier for the first component making the linkage. 

               This data item is a pointer to _entity_poly_seq.mon_id 
               in the ENTITY_POLY_SEQ category.



#### _pdbx_entity_poly_comp_link_list.comp_id_2 (required)


               The component identifier for the second component making the linkage. 

               This data item is a pointer to _entity_poly_seq.mon_id 
               in the ENTITY_POLY_SEQ category.



#### _pdbx_entity_poly_comp_link_list.details


               A description of special aspects of this linkage.



#### _pdbx_entity_poly_comp_link_list.entity_comp_num_1 (required)


               The component number for the first component making the linkage. 

               This data item is a pointer to _entity_poly_seq.num 
               in the ENTITY_POLY_SEQ category.




#### _pdbx_entity_poly_comp_link_list.entity_comp_num_2 (required)


               The component number for the second component making the linkage. 

               This data item is a pointer to _entity_poly_seq.num 
               in the ENTITY_POLY_SEQ category.




#### _pdbx_entity_poly_comp_link_list.entity_id (required)


               The entity id for this branched entity. 

               This data item is a pointer to _entity_poly_seq.entity_id  
               in the ENTITY_POLY_SEQ category.



#### _pdbx_entity_poly_comp_link_list.leaving_atom_id_1 (required)


               The leaving atom identifier/name bonded to the first atom making the linkage. 




#### _pdbx_entity_poly_comp_link_list.leaving_atom_id_2 (required)


               The leaving atom identifier/name bonded to the second atom making the linkage. 




#### _pdbx_entity_poly_comp_link_list.link_id (key)


               The value of _pdbx_entity_poly_comp_link_list.link_id uniquely identifies
               linkages within the branched entity.




#### _pdbx_entity_poly_comp_link_list.value_order


               The bond order target for the chemical linkage.



---

| Allowed Values | Detail |
| -------------- | ------ |
| arom | aromatic bond |
| delo | delocalised double bond |
| doub | double bond |
| pi | pi bond |
| poly | polymeric bond |
| quad | quadruple bond |
| sing | single bond |
| trip | triple bond |


## Category struct_conn


               Data items in the STRUCT_CONN category record details about
               the connections between portions of the structure. These can be
               hydrogen bonds, salt bridges, disulfide bridges and so on.

               The STRUCT_CONN_TYPE records define the criteria used to
               identify these connections.

---


```
     
         Example 1 - based on PDB entry 5HVP and laboratory records for the
                     structure corresponding to PDB entry 5HVP.
     
         loop_
         _struct_conn.id
         _struct_conn.conn_type_id
         _struct_conn.ptnr1_label_comp_id
         _struct_conn.ptnr1_label_asym_id
         _struct_conn.ptnr1_label_seq_id
         _struct_conn.ptnr1_label_atom_id
         _struct_conn.ptnr1_role
         _struct_conn.ptnr1_symmetry
         _struct_conn.ptnr2_label_comp_id
         _struct_conn.ptnr2_label_asym_id
         _struct_conn.ptnr2_label_seq_id
         _struct_conn.ptnr2_label_atom_id
         _struct_conn.ptnr2_role
         _struct_conn.ptnr2_symmetry
         _struct_conn.details
           C1  saltbr  ARG  A  87 NZ1 positive 1_555 GLU  A  92  OE1
               negative 1_555  .
           C2  hydrog  ARG  B 287 N   donor    1_555 GLY  B 292  O
               acceptor 1_555  .
         # - - - - data truncated for brevity - - - -
```


---

| Attribute | Key | Required | Type | Units | Enumerated | Bounded |
| --------- | --- | -------- | ---- | ----- | ---------- | ------- |
| conn_type_id | no | yes | ucode | None | no | no |
| details | no | no | text | None | no | no |
| id | yes | yes | code | None | no | no |
| pdbx_dist_value | no | no | float | angstroms | no | no |
| pdbx_leaving_atom_flag | no | no | code | None | yes | no |
| pdbx_PDB_id | no | no | code | None | no | no |
| pdbx_ptnr1_atom_stereo_config | no | no | ucode | None | yes | no |
| pdbx_ptnr1_auth_alt_id | no | no | code | None | no | no |
| pdbx_ptnr1_label_alt_id | no | no | code | None | no | no |
| pdbx_ptnr1_leaving_atom_id | no | no | atcode | None | no | no |
| pdbx_ptnr1_mod_name | no | no | line | None | no | no |
| pdbx_ptnr1_PDB_ins_code | no | no | code | None | no | no |
| pdbx_ptnr1_replaced_atom | no | no | code | None | no | no |
| pdbx_ptnr1_standard_comp_id | no | no | code | None | no | no |
| pdbx_ptnr1_sugar_name | no | no | line | None | no | no |
| pdbx_ptnr2_atom_stereo_config | no | no | ucode | None | yes | no |
| pdbx_ptnr2_auth_alt_id | no | no | code | None | no | no |
| pdbx_ptnr2_label_alt_id | no | no | code | None | no | no |
| pdbx_ptnr2_leaving_atom_id | no | no | atcode | None | no | no |
| pdbx_ptnr2_PDB_ins_code | no | no | code | None | no | no |
| pdbx_ptnr3_auth_alt_id | no | no | code | None | no | no |
| pdbx_ptnr3_auth_asym_id | no | no | code | None | no | no |
| pdbx_ptnr3_auth_atom_id | no | no | atcode | None | no | no |
| pdbx_ptnr3_auth_comp_id | no | no | code | None | no | no |
| pdbx_ptnr3_auth_ins_code | no | no | code | None | no | no |
| pdbx_ptnr3_auth_seq_id | no | no | code | None | no | no |
| pdbx_ptnr3_label_alt_id | no | no | code | None | no | no |
| pdbx_ptnr3_label_asym_id | no | no | code | None | no | no |
| pdbx_ptnr3_label_atom_id | no | no | atcode | None | no | no |
| pdbx_ptnr3_label_comp_id | no | no | ucode | None | no | no |
| pdbx_ptnr3_label_seq_id | no | no | int | None | no | no |
| pdbx_ptnr3_PDB_ins_code | no | no | code | None | no | no |
| pdbx_role | no | no | uline | None | yes | no |
| pdbx_value_order | no | no | ucode | None | yes | no |
| ptnr1_auth_asym_id | no | no | code | None | no | no |
| ptnr1_auth_atom_id | no | no | atcode | None | no | no |
| ptnr1_auth_comp_id | no | no | code | None | no | no |
| ptnr1_auth_seq_id | no | no | code | None | no | no |
| ptnr1_label_alt_id | no | no | code | None | no | no |
| ptnr1_label_asym_id | no | yes | code | None | no | no |
| ptnr1_label_atom_id | no | no | atcode | None | no | no |
| ptnr1_label_comp_id | no | yes | ucode | None | no | no |
| ptnr1_label_seq_id | no | yes | int | None | no | no |
| ptnr1_role | no | no | uline | None | yes | no |
| ptnr1_symmetry | no | no | symop | None | no | no |
| ptnr2_auth_asym_id | no | no | code | None | no | no |
| ptnr2_auth_atom_id | no | no | atcode | None | no | no |
| ptnr2_auth_comp_id | no | no | code | None | no | no |
| ptnr2_auth_seq_id | no | no | code | None | no | no |
| ptnr2_label_alt_id | no | no | code | None | no | no |
| ptnr2_label_asym_id | no | yes | code | None | no | no |
| ptnr2_label_atom_id | no | no | atcode | None | no | no |
| ptnr2_label_comp_id | no | yes | ucode | None | no | no |
| ptnr2_label_seq_id | no | yes | int | None | no | no |
| ptnr2_role | no | no | uline | None | yes | no |
| ptnr2_symmetry | no | no | symop | None | no | no |

---

#### _struct_conn.pdbx_ptnr1_atom_stereo_config


               The chiral configuration of the first atom making the linkage.



---

| Allowed Values | Detail |
| -------------- | ------ |
| N | none |
| R | rectus - right handed configuration |
| S | sinister - left handed configuration |


#### _struct_conn.pdbx_ptnr1_leaving_atom_id


               The leaving atom that is removed from first atom making the linkage.


#### _struct_conn.pdbx_ptnr2_atom_stereo_config


               The chiral configuration of the second atom making the linkage.



---

| Allowed Values | Detail |
| -------------- | ------ |
| N | none |
| R | rectus - right handed configuration |
| S | sinister - left handed configuration |




#### _struct_conn.pdbx_ptnr2_leaving_atom_id


               The leaving atom that is removed from second atom making the linkage. 






#### _struct_conn.pdbx_role


               The chemical or structural role of the interaction



---

| Allowed Values | Detail |
| -------------- | ------ |
| Glycosylation | . |
| Post-translational modification | . |



