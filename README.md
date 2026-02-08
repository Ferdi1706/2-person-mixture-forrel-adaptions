# Kinship in 2-person DNA mixtures (proof of concept)

This repository contains an R notebook with a proof-of-concept implementation for estimating IBD / kinship coefficients in a 2-person DNA mixture setting with
- one known contributor (Person 1) and
- one unknown contributor (Person 2),

> Status: Work in progress  
> The code is functional for the current use case, but the structure is not yet polished and will likely be refactored/cleaned up.

---

## What’s inside

- `*.Rmd` / notebook containing:
  - an adapted projected gradient descent routine (`my_PGD`) based on internal `forrel` functionality
  - genotype enumeration for the unknown contributor (`compute_person2_genotypes`, `get_person2_genotypes`)
  - adapted likelihood / weight computation for mixtures (`my_ibdEstimate`, `my_IBDlikelihood`, `my_checkPairwise`)
  - helper to compute posterior genotype probabilities of the unknown contributor (`get_gtProbs`)
  - an example run on a real-case dataset using provided allele frequency `.txt` files

- `*.txt` allele frequency tables used by the example (one file per marker)
