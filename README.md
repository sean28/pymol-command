# Pymol command
<div style="text-align: justify"> PyMOL is a molecular 3D structure display software, which is suitable for creating high-quality 3D structure images of small molecules or biological macromolecules. The content of this issue is to share the quick reference manual of common commands in the use of PyMOL. If you need the original version, you can browse it on the official website <a href="https://pymolwiki.org/index.php/Main_Page">(pymolwiki)</a>.</div>


|Description           |        Command              |
|          :---        |           :---              |
|Start record operation|  log_open xx.pml|
|Close record operation|  log_close      | 
|remove solvent        | remove solvent  |
|Select Na+            | select selectionname, r. na\\+|
|Select Cl-            | select selectionname, r. cl\\-|
|Delete selection      |  delete ,selection|
|Merge selection       |  select ,new_selection, selection1 + selection2  | 
|Structural superposition | cealign, align, super, pairfit, fit  selection, target  <a href="https://github.com/sean28/home/blob/ba4be1a571124c8a258852e75c837058bdf112d8/Superpositions.pdf">(Detailed description)</a>|
|Label emerges         | set label_position, (0, 0, 40) |
|Print label           |  iterate  selection and name CA, print (label) |
|Print resi and resn   |  iterate  selection and name CA, print (resi, resn)  | 
|Rotating angle of view| turn x, 180 or turn y, 180|
|Select residues around 5 angstroms of ligand | select 5A_resi, byres selection_ligand_name around 5|
|Estimate the x, y and z of protein  |  get_extent <selection_name>|
|Move the screen 10A along the X axis ̊   |  move x, 10  | 
|View the number of residues  |  print len(cmd.get_model("poly").get_residues()) | 
|View the number of atoms     |  count_atoms <selection_name>| 
|Altering atom coordinates    |  alter_state 1, <selection_name>, y=y+10.0 |
|Cacluate RMSD                |  rms (selection), (target-selection)|
|select anything shown as a lines/dots/spheres |  select rep lines/dots/spheres|

 
There are also some simple scripts that can easily implement some functions, and  You can download them here for free.

(1) [Obtain protein residue sequence information. ](https://github.com/sean28/home/blob/bddec2088f8db6c096d0f62b22bc9d30f810eeff/get_fasta.pml)

(2) [Hydrogenation of protein.](https://github.com/sean28/home/blob/bddec2088f8db6c096d0f62b22bc9d30f810eeff/add_H.pml)

(3) [Remove solvent molecules.](https://github.com/sean28/home/blob/bddec2088f8db6c096d0f62b22bc9d30f810eeff/remove_water.pml)

to be continue...
