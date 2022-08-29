---
title: AMBER ff99SBnmr2
permalink: /portfolio/nmr2/
---

### [<< Back to Home](https://rye4ray.github.io)

AMBER ff99SBnmr2 "nmr2" is a protein force field developed by me and co-workers in the Brüschweiler group at The Ohio State University for realistic simulations of both folded and disordered proteins. "nmr2" is a residue-specfic protein force field that is derived from ff99SBnmr1 by balancing the backbone dihedral angle potentials in a residue-specific manner to quantitatively reproduce dihedral angle distributions from an experimental coil library.

For GROMACS, a "nmr2" force field package is readily available for implementation.

### Instructions
1. [Download](amber99sbnmr2.ff.zip) and extract the force field into your working directory.
2. Run ```pdb2gmx``` and select ```amber99sbnmr2``` as your protein force field. Run ```grompp``` to obtain a ```tpr``` file.  
3. Equilibrate and submit your production run.

### Notes
1. "nmr2" uses AMBER nomenclature and may not recognize residue names in other naming conventions. This issue can usually be resolved by changing the 3-letter abbreviation of the residue, e.g., by changing HSE to HIE.
2. If your protein contains a residue type that is not common, please check aminoacids.rtp to see if the residue-specific modifications in "nmr2" apply. For example, the atom type of carbon atoms under [CYX] is CT13 with number 13 indicating cysteine residue type, whereas the atom type of carbon atoms under [CYM] is simply CT without specifying its residue type. Therefore, the modification of dihedral angle potentials is applied to cysteines forming disulfide bonds (CYX) but not S-methylcysteine (CYM).
3. If you use "nmr2" in your work, please cite the reference below.

### Reference
Yu, L; Li, D.-W.; Brüschweiler, R., Balanced Amino-Acid-Specific Molecular Dynamics Force Field for the Realistic Simulation of Both Folded and Disordered Proteins, *J. Chem. Theory Comput.*, **2020**, *16*, 1311–1318, doi:10.1021/acs.jctc.9b01062

### Contact
If you have any questions, please feel free to contact Lei Yu via yu.1935@osu.edu
