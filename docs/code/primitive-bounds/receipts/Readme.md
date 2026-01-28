## Code related to the paper, "Uniform exponent bounds on the number of primitive extensions of number fields", by Robert J. Lemke Oliver
### Receipts for specific computations claimed in the paper.

This folder contains the receipts for most of the computations mentioned in the paper.  More concretely, it holds:
- The computation of the invariant degrees of the Mathieu groups claimed in Lemma 4.18.  The Magma code used to verify this computation is [`compute-mathieu-invariants.mag`](compute-mathieu-invariants.mag).  The file [`mathieu-invariants-output.txt`](mathieu-invariants-output.txt) contains the output of this file run on my personal office computer with an Intel i7-12700K and 128GB of RAM.
- The determination of the exponents for the small degree extensions claimed in Theorem 5.9, and a verification of the claimed properties.  The code for this is [`small-degree-exponents.mag`](small-degree-exponents.mag), and the output of running it is [`small-degree-output.txt`](small-degree-output.txt).
- The folder [`experiments/`](experiments/) contains the output of some experiments related to invariants of linear groups.  This will be periodically updated.
