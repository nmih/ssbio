.. _software:

********
Software
********

+-------------------+-----------------+------------------------------+-----------------------------------------------------------+------------------------------+-------------------+-----------------+-----------------------------+
| Analysis level    | Function type   | Name                         | Function                                                  | Internal Python functions    | External software | Web server      | Alternate external software |
+===================+=================+==============================+===========================================================+==============================+===================+=================+=============================+
| Network model or  | Pipeline        | GEM-PRO                      | Pipeline to automatically map gene IDs, protein           | :doc:`gempro`                |                   |                 |                             |
| a set of proteins |                 |                              | sequences, or GEMs to available experimental structures.  |                              |                   |                 |                             |
|                   |                 |                              | Enables streamlined analysis for all functions described  |                              |                   |                 |                             |
|                   |                 |                              | below for individual proteins.                            |                              |                   |                 |                             |
+-------------------+-----------------+------------------------------+-----------------------------------------------------------+------------------------------+-------------------+-----------------+-----------------------------+
| Protein sequence  | Sequence-based  | Various sequence properties  | Basic properties of the sequence, such as percent of      | `Biopython ProteinAnalysis`_ | :doc:`emboss`     |                 |                             |
|                   | calculation     |                              | polar, non-polar, hydrophobic or hydrophilic residues.    |                              |                   |                 |                             |
+-------------------+-----------------+------------------------------+-----------------------------------------------------------+------------------------------+-------------------+-----------------+-----------------------------+
|                   |                 | Sequence alignment           | Basic functions to run pairwise or multiple sequence      | `Biopython pairwise2`_       | :doc:`emboss`     |                 |                             |
|                   |                 |                              | alignments                                                |                              |                   |                 |                             |
+-------------------+-----------------+------------------------------+-----------------------------------------------------------+------------------------------+-------------------+-----------------+-----------------------------+
|                   | Sequence-based  | Aggregation propensity       | Consensus method to predict the aggregation propensity of |                              |                   | :doc:`amylpred` |                             |
|                   | prediction      |                              | proteins, specifically the number of aggregation-prone    |                              |                   |                 |                             |
|                   |                 |                              | segments on an unfolded protein sequence                  |                              |                   |                 |                             |
+-------------------+-----------------+------------------------------+-----------------------------------------------------------+------------------------------+-------------------+-----------------+-----------------------------+
|                   |                 | Secondary structure and      | Predictions of secondary structure and relative solvent   |                              | :doc:`scratch`    |                 |                             |
|                   |                 | solvent accessibilities      | accessibilities per residue                               |                              |                   |                 |                             |
+-------------------+-----------------+------------------------------+-----------------------------------------------------------+------------------------------+-------------------+-----------------+-----------------------------+
|                   |                 | Thermostability              | Free energy of unfolding (ΔG), adapted from Oobatake      | ssbio custom functions       |                   |                 |                             |
|                   |                 |                              | (Oobatake & Ooi 1993) and Dill (Dill et al. 2011)         |                              |                   |                 |                             |
+-------------------+-----------------+------------------------------+-----------------------------------------------------------+------------------------------+-------------------+-----------------+-----------------------------+
|                   |                 | Transmembrane domains        | Prediction of transmembrane domains from sequence         |                              | :doc:`tmhmm`      |                 |                             |
+-------------------+-----------------+------------------------------+-----------------------------------------------------------+------------------------------+-------------------+-----------------+-----------------------------+
| Protein structure | Sequence-based  | Homology modeling            | Preparation scripts and parsers for executing homology    |                              | :doc:`itasser`    |                 |                             |
|                   | prediction      |                              | modeling algorithms                                       |                              |                   |                 |                             |
+-------------------+-----------------+------------------------------+-----------------------------------------------------------+------------------------------+-------------------+-----------------+-----------------------------+
|                   | Structure-based | Kinetic folding rate         | Prediction of protein folding rates from amino acid       |                              |                   | :doc:`foldrate` |                             |
|                   | prediction      |                              | sequence                                                  |                              |                   |                 |                             |
+-------------------+-----------------+------------------------------+-----------------------------------------------------------+------------------------------+-------------------+-----------------+-----------------------------+
|                   |                 | Transmembrane orientation    | Prediction of transmembrane domains and orientation in a  |                              |                   | :doc:`opm`      |                             |
|                   |                 |                              | membrane                                                  |                              |                   |                 |                             |
+-------------------+-----------------+------------------------------+-----------------------------------------------------------+------------------------------+-------------------+-----------------+-----------------------------+
|                   | Structure-based | Secondary structure          | Calculations of secondary structure                       | `Biopython Structure`_       | :doc:`dssp`       |                 | :doc:`stride`               |
|                   | calculation     |                              |                                                           |                              |                   |                 |                             |
+-------------------+-----------------+------------------------------+-----------------------------------------------------------+------------------------------+-------------------+-----------------+-----------------------------+
|                   |                 | Solvent accessibilities      | Calculations of per-residue absolute and relative solvent | `Biopython Structure`_       | :doc:`dssp`       |                 | :doc:`freesasa`             |
|                   |                 |                              | accessibilities                                           |                              |                   |                 |                             |
+-------------------+-----------------+------------------------------+-----------------------------------------------------------+------------------------------+-------------------+-----------------+-----------------------------+
|                   |                 | Residue depths               | Calculations of residue depths                            | `Biopython Structure`_       | :doc:`msms`       |                 |                             |
+-------------------+-----------------+------------------------------+-----------------------------------------------------------+------------------------------+-------------------+-----------------+-----------------------------+
|                   |                 | Structural similarity        | Pairwise calculations of 3D structural similarity         |                              | :doc:`fatcat`     |                 |                             |
+-------------------+-----------------+------------------------------+-----------------------------------------------------------+------------------------------+-------------------+-----------------+-----------------------------+
|                   |                 | Quality                      | Custom functions to allow ranking of structures by        | ssbio custom functions       |                   |                 |                             |
|                   |                 |                              | percent identity to a defined sequence, structure         |                              |                   |                 |                             |
|                   |                 |                              | resolution, and other structure quality metrics           |                              |                   |                 |                             |
+-------------------+-----------------+------------------------------+-----------------------------------------------------------+------------------------------+-------------------+-----------------+-----------------------------+
|                   |                 | Various structure properties | Basic properties of the structure, such as distance       | `Biopython Structure`_       |                   |                 |                             |
|                   |                 |                              | measurements between residues or number of disulfide      |                              |                   |                 |                             |
|                   |                 |                              | bridges                                                   |                              |                   |                 |                             |
+-------------------+-----------------+------------------------------+-----------------------------------------------------------+------------------------------+-------------------+-----------------+-----------------------------+
|                   | Structure-based | Structure cleaning, mutating | Custom functions to allow for the preparation of          | `Biopython Structure`_       |                   | AmberTools_     |                             |
|                   | function        |                              | structure files for molecular modeling, with options to   |                              |                   |                 |                             |
|                   |                 |                              | remove hydrogens/waters/heteroatoms, select specific      |                              |                   |                 |                             |
|                   |                 |                              | chains, or mutate specific residues.                      |                              |                   |                 |                             |
+-------------------+-----------------+------------------------------+-----------------------------------------------------------+------------------------------+-------------------+-----------------+-----------------------------+


|  .. _Biopython Structure: http://biopython.org/wiki/The_Biopython_Structural_Bioinformatics_FAQ |  |  |  |  |  |  |  |
|  .. _Biopython ProteinAnalysis: http://biopython.org/wiki/ProtParam |  |  |  |  |  |  |  |
|  .. _Biopython pairwise2: http://biopython.org/DIST/docs/api/Bio.pairwise2-module.html |  |  |  |  |  |  |  |
|  .. _AmberTools: http://ambermd.org/#AmberTools |  |  |  |  |  |  |  |