## Code related to the paper, "Enumerating Galois extensions of number fields", by Robert J. Lemke Oliver

This folder contains the Magma code needed to verify many of the explicit computations in Section 4.1 of my paper *Enumerating Galois extensions of number fields* relating to almost simple groups.  Specifically, it includes:

- The receipts for Lemma 4.10 on classical groups.  The file [`receipt-classical.txt`](receipt-classical.txt) contains the output of running the file [`classical-bounds.mag`](classical-bounds.mag).  This Magma file relies on [`find-invariants.mag`](find-invariants.mag).  It mostly serves as a hub.  It loads several other files, roughly one per line in Table 1.  A tarball is available [`here`](classical-bounds-all.tar.gz).
- The receipts for Lemma 4.11 on exceptional groups.  The file [`receipt-exceptional.txt`](receipt-exceptional.txt) contains the output of running the file [`exceptional-bounds.mag`](exceptional-bounds.mag).  As less ad hoc work is needed in these cases, this is a single file to verify the entirety of the lemma.  (This relies on the file [`find-invariants.mag`](find-invariants.mag).)
- The receipts for Lemmas 4.12--4.16 on sporadic groups.  The file [`receipt-sporadic.txt`](receipt-sporadic.txt) contains the output of running the file [`sporadic-bounds.mag`](sporadic-bounds.mag).  This loads separate files for the Mathieu groups, the groups for which the base bounds are sufficient, the groups J_1 and J_3, and the Thompson group.  A tarball is [`here`](sporadic-bounds-all.tar.gz).
- The receipts for Lemma 4.17 and Lemma 4.18.
  - Lemma 4.17 is verified in the file [`find-alpha.mag`](find-alpha.mag), the output of which is in the text file [`receipt-find-alpha.txt`](receipt-find-alpha.txt).
  - Lemma 4.18 is verified in the file [`find-beta.mag`](find-beta.mag), the output of which is in the text file [`receipt-find-beta.txt`](receipt-find-beta.txt).
