## Code related to the paper "The least prime with a given cycle type", by Peter J. Cho, Robert J. Lemke Oliver, and Asif Zaman

This is the main hub for code related to the paper "The least prime with a given cycle type", available on the arxiv here: [arxiv link](https://arxiv.org/abs/2512.24963).

In particular, this repository contains the code necessary to verify Theorems 2.5, 2.6, 7.1, and 8.1 from that paper.  Here is a description of the files:

- The file `checkholomorphy.mag` is a Magma file with many useful functions related to computing monomial characters of groups, finding a basis for the monomial cone of a group, and the like.  It uses some of Magma's built-in linear programming functionality.  However, when I call some functions relying on linear programming in the most recent versions of Magma, it has been throwing a warning: "LP unknown code: 2".  In every instance I've checked, the output has still been correct, and I believe these to still be useful functions.  However, I have steered away from invoking them in the proof of any theorem.

- The file `general-G-all-classes.mag` is a Magma file that will compute, for a given finite group G, the degree optimal choices of the characters Psi_+ and Psi_- for each of the rational classes in G, along with the resulting Linnik exponent.  In particular, it is the file that is used in the proofs of Theorems 7.1 and 8.1.  Here are some important but annoying points related to its use:
	- The group G is hard-coded into the file on the first real line of code, line 14.
	- As described in the proof of Theorem 7.1, there is an ad hoc Magma -> Python -> Magma pipeline.  
	- For the Python piece of the pipeline, the code assumes you have Python 3 installed, along with scipy version 1.09+.
	- It assumes you can run a python file with the command `python3 file.py` in your terminal.  This may be changed on line 126.
	- The reason for this awkward pipeline is to use Magma for the pieces of the computation that are group-heavy, namely iterating over subgroups to compute monomial characters.  As described in the proof, Python is used for two linear programming steps.  One could easily be done in Magma (but throws warnings; see above), but the other is a mixed integer linear programming problem for which Magma does not have a built in solver.  Instead, this calls [scipy.optimize.milp](https://docs.scipy.org/doc/scipy/reference/generated/scipy.optimize.milp.html).
	- Finally, for my personal convenience in writing the paper, I also have the code generate a LaTeX file with a table containing representatives of each rational class and the Linnik exponent.  I've left it in just in case it's useful, but if this is annoying to you, simply comment out line 165.
	
- The files `receipts/receipt-sym5.txt` through `receipts/receipt-sym10.txt` contain the output of running the `general-G-all-classes.mag` for the symmetric groups of degree between 5 and 10.  From this, one may verify the specific tables given in Section 7 and Appendix A.  Note that these files also include the specific choices of characters Psi_+ and Psi_-.  The assignment between Magma's labels for these characters and those included in Section 7 was done by hand.

- The files `receipts/receipt-M11.txt` through `receipts/receipt-M24.txt` and `receipts/receipt-PSL2-7.txt` through `receipts/receipt-PSL2-23.txt` contain the output of running the above for the simple groups referenced in Theorems 2.6 and 8.1.
