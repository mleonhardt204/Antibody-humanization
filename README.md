### <ins>OKT3 Fv humanization</ins>
#### This project focuses on the humanization of murine monoclonal “OKT3” antibody.  The crystal structure of OKT3 MAb complexed with CD3 receptor is contained within the cif (Crystallographic Information File): 1SY6.cif (https://www.rcsb.org/structure/1SY6).  The atomic coordinates of OKT3 Fv complexed with CD3 receptor is contained within the pdb (Protein Data Bank) file: Murine_Fv_V_Domain_Clean.pdb. 

### <ins>Step 1</ins>: Sequences underwent initial “humanness” assessment required to select the ideal human light and human heavy chain acceptors.

### <ins>Step 2</ins>:  Human framework regions were grafted on to the CDR regions of Murine_Fv_V_Domain_Clean.pdb.  Atomic coordinates of chimeric Fv are contained within: chimeric_Fv.pdb

### <ins>Step 3</ins>: to get a visualization of chimeric_Fv: 
#### • Option 1: examine chimeric_Fv.pdb file directly
#### • Option 2: run Python script (igfold.py) within IgFold Colab notebook (IgFold.ipynb) in the following order:
#### [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mleonhardt204/Antibody-humanization/blob/main/IgFold.ipynb)
#### o Run script in cell 1 (definitions and sequences)
#### o Run script in cell 2 (install dependencies)
#### o Manual restart  click on RESTART
#### o Run script in cell 1 (reload variables into fresh memory session)
#### o Run script in cell 3
#### o Run script in cell 4

### <ins>Step 4</ins>: potential framework back-mutations were noted and prioritized (based on the physical support provided to CDRs within the murine Fv).  However, if the equivalent human framework residues (within the chimeric_Fv) also provided physical support to the CDRs, then back-mutation was de-prioritized. Internal structure analyzed:
#### Intra-Chain, Intra-Domain: FRHeavy  CDRsHeavy
#### Intra-Chain, Intra-Domain: FRLight  CDRsLight
#### Inter-Chain, Inter-Domain: FRHeavy  CDRsLight
#### Inter-Chain, Inter-Domain: FRLight  CDRsHeavy
  
### <ins>Step 5</ins>: assessment of mutated chimeric_Fv molecules:
#### •	structural stability (using Mutation Explorer): The free energy (ΔΔG) for each molecule was assessed to determine if thermodynamic stability was improved upon when comparing to the parent molecule (i.e. unmutated chimeric_Fv).  Note: mutations which caused the molecule to have a more positive ΔΔG were scrapped (i.e. LESS stable and more prone to unfolding)
#### •	core stability check between H and L chains (using ChimeraX):  The physical stability/ geometric reality was assessed between non-bonded atoms and also by measuring the packing efficiency.  Note: molecules which were deemed unstable or which did not exhibit a tight interface between the light and heavy chain were ultimately scrapped.
#### •	quality of interface between H and L chains (using ChimeraX): the surface area lost when the Light Chain (L) and Heavy Chain (H) come together was assessed or “Buried Surface Area” (BSA).  
#### •	critical stabilizing contacts (i.e. “Framework anchors”) scored for quality (using ChimeraX): the contact distance for critical anchors was assessed to ensure highly conserved interactions with CDRs required for correct positioning.  The larger the BSA, the more extensive (and stable) the non-covalent interactions. Desired optimal range: 1500Å2 to 2000 Å2. 

### <ins>Step 6</ins>: visualization of final construct:  Chimeric_Fv_complete_set.pdb
