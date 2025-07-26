# Spy-structure
80586 pdb files

# 1stVer_proteinSruct-NoFilted-
First version of Protein structure &amp; sequence &amp; score(RMSD, pLDDT, pTM, pAE) that generated from natural seq by using RFdiffusion+ProteinMPNN+Alphafold2.

# Repository Structure
Please ignored .trb files

```
📁
├── 📄 README.md
|
├── 📁 SifA_Agona.result\outputs        # ProteinName_BacteriaName.result
│    └── ...
│
├── 📁 SifA_Gallinarum.result\outputs
│   ├── 📁 SifA_Gallinarum
│   │   ├── 📁 all_pdb                  # all files by RFD+MPNN
│   │   ├── best_design0.pdb            # the best seq of one of the RFD structure
│   │   ├── best_design1.pdb
│   │   ├── ...
│   │   ├── best.pdb                    # the bestest structure+seq of this bacteria's protein
│   │   ├── design.fasta                # the sequence file(also contains score)
│   │   ├── input.pdb
│   │   └── mpnn_results.csv            # store score, sequence
│   │
│   │── 📁 traj                         # I am not sure what it means, but it contains.pdb files
│   │   └── ...
│   │
│   │── SifA_Agona_0.pdb                # the RFD structure, no side chains, only backbone.
│   │── SifA_Agona_0.trb                # ignored it
│   │── SifA_Agona_1.pdb
│   │── SifA_Agona_1.trb
│   │── ...
│   │
├── 📁 SseF_Agona_4kh3i.result
│
└── ...
```

# Fasta(.fa file) Structure
```
(design:RFD structure    n:ID of MPNN seq    plddt~rmsd:score)
>design:0 n:0|mpnn:1.000|plddt:0.879|ptm:0.615|pae:6.926|rmsd:0.991 (Custom header)
MEEEKKKKELEENP... (the protein sequence)
>design:0 n:1|mpnn:1.167|plddt:0.858|ptm:0.618|pae:7.529|rmsd:1.850
SSAAAKQAALEADPEAKIEALRKEIEKLEKEIEEKEKELKEMERKGIKDEEKKKKLEEEIKKLKKRKEELEKELKKLEEEVKRKEEELE
(so for example, "design:0 n:1" structure will store at all_pdb\design0_n1.pdb)
```

# CSV Structure
Same as Fasta.
