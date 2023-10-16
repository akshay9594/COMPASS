
# The Combined Parallel Subscripted Subscript (COMPASS) Benchmark Suite 
This COMPASS suite is a collection of benchmarks exhibiting special patterns
referred to as subscripted subscript patterns such as a[b[i]]. This repository
serves as the artifact for our LCPC paper titled - 
*COMPASS: A Combined Parallel Subscripted Subscript Benchmark Suite*

The benchmarks have been taken from several well-known benchmark suites listed below.

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

# Compiling and Running the benchmarks

   1. There are 2 main directories - "serial" and "parallel
       which contain the serial and parallel versions of the codes. The
       process of compiling and running the codes is the same for both
       versions.
   2. Compiling amgmk, IncompleteCholesky and SDDMM
      - Navigate to the source of these benchmarks and find the Makefile
      - Use the "make" command to run the Makefile and generate the 
        executable.
      - "sddmm", "AMGMk" and "icm7" are the generated executables.
   2. Running amgmk:
      - Run this benchmark using command "./amgmk"
      - To change the input matrix, modify the values of variable
         nx, ny and nz within the routine "test_matvec()" in main.c.
   3. Running IncompleteCholesky and SDDMM
      - Place the input sparse matrix within the sud-directory "input" present 
        in the root directory of each of these benchmarks.
      - Use the following commands for execution"
         (a) ./sddmm /input/file_name.mtx
         (b) ./icm7 /input/file_name.mtx
      where file_name.mtx is the input sparse matrix in the matrix market format.

   4. IS and UA
      - Navigate to the directory with the source files and compile using the Makefile.
      - The command to compile is:
        " make CLASS=A" (for input Class A)
      - The supported classes are A through D
      - The executable is placed in the "bin" sub-directory.

   5. CHOLMOD Supernodal (SuiteSparse)
      - Navigate to the directories AMD, CAMD, SuiteSparse_config and COLAMD first.
      - Hit the command "make" to compile the source files in each of the above directories.
      - Then navigate to the directory CHOLMOD and hit "make" to compile.
      - If there are issues during compilation, check the make file - SuiteSparse_config.mk
        within SuiteSparse_config directory.
      - The executable for CHOLMOD Supernodal is placed within the "Demo" subdirectory within
        CHOLMOD main directory.
      - Execute using command: "./cholmod_demo /Matrix/file_name.mtx"
      - The list of input sparse matrices to be used are mentioned in the LCPC paper linked above.