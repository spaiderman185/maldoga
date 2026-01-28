## Code related to the paper "Asymptotics for 6-torsion and D_6-extensions", by Koymans, Lemke Oliver, Sofos, and Thorne

This is the main hub for code related to the paper "Asymptotics for 6-torsion and D_6-extensions", available on the arxiv here: [arxiv link](https://arxiv.org/abs/2512.21920).

In particular, the Magma files above were used in the computations of local etale algebras over Q2 and Q3 during the course of the proof of Theorem 1.4.  The file `etale-algebras.mag` loads the two subfiles `etale-algebras-Q2.mag` and `etale-algebras-Q3.mag` in turn, and the file `etale-algebras-output.txt` records the output of running that Magma file.  The heart of the computation is in those two subfiles, each of pulls substantially from the tables of local fields provided by the [LMFDB](https://www.lmfdb.org/).
