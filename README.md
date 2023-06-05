
# The Comprehensive Parallel Subscripted Subscript (COMPASS) Benchmark Suite 
This COMPASS suite is a collection of benchmarks exhibiting special patterns
referred to as subscripted subscript patterns such as a[b[i]]. The benchmarks
have been taken from several well-known benchmark suites listed below.

# Obtaining the Codes

This repository contains the benchmark codes listed below:

| Code  | Source | Original Source link | 
| ------------- | ------------- | ------------- |
| Amgmk-v1.0  | CORAL Benchmark Codes | (https://asc.llnl.gov/coral-benchmarks)
| UA-NPB-1.0.3 | NAS Parallel Benchmarks | (https://github.com/akshay9594/SNU_NPB-1.0.3)  
| CHOLMOD | SuiteSparse | (https://github.com/DrTimothyAldenDavis/SuiteSparse)
| IncompleteCholesky (C version) | Sparselib++ | (https://github.com/king-mahdi/IEGenLib)
| IS-NPB-1.0.3 | NAS Parallel Benchmarks | (https://github.com/akshay9594/SNU_NPB-1.0.3)
| SDDMM (C version) | Published Paper | (https://github.com/isratnisa/SDDMM_GPU)

The benchmarks can be obtained by cloning the git repository using the commands-
```
cd $HOME or cd ~
git clone (https://github.com/akshay9594/COMPASS.git)
cd COMPASS
```

# Input Files

- The benchmarks : Amgmk, UA-NPB and IS-NPB use internally generated inputs
- The benchmarks : CHOLMOD, SDDMM and IncompleteCholesky require
   input sparse matrices which can be obtained from the SuiteSparse
   matrix collection - (http://sparse.tamu.edu/)
