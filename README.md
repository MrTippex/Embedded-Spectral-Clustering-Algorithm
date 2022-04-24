# Embedded Spectral Clustering Algorithm
#### Python interface to preform Spectral Clustering Algorithm, using C modules in order to obtain accelerated performance <br />
**This is a little project using Cython I wanted to get an experiance with** <br />
**(More about [the 'Spectral Clustering Algorithm'](https://en.wikipedia.org/wiki/Spectral_clustering))** <br />
**(More about [finding eigenvalues using Jacobi's Algorithm](https://en.wikipedia.org/wiki/Jacobi_eigenvalue_algorithm))** <br />

## Code Files:

- #### spkmeans.py
The use interface, includes the main function
- #### spkmeans.h
- #### spkmeans.c
Spkmeans Algorithm
- #### spkmeansmodule.c
- #### kmeans.h
- #### kmeans.c
Kmeans Algorithm
- #### kmeansmodule.c
- #### setup.py
Setup build for the C modules
- #### comp.sh
Compilation script
- #### Data_to_classify.txt
An example for required data to classify

## Running The Program:
1. Build the C modules using: $ pyhton3 setup.build --inplace
2. Compile the programm using: $ bash comp.sh
3. Run spkmeans.py with the desire input: $ python3 spkmeans.py 0 spk path_to_input.txt

## The Output:
**First row** - represents the initial clusters that has been selected <br />
**Next paragrapth** - represents the final clusters, using convergence = 1.0*10^-5 <br />
<br />
**$ python3 spkmeans.py 0 spk ./Data_to_classify.txt <br />**
44,65,87,84,90,58 <br />
0.0000,0.0000,0.0822,0.0000,0.0000,0.0000 <br />
1.0000,0.0000,0.0000,0.0000,0.0000,0.0000 <br />
0.0532,0.0000,0.0000,0.9832,0.0000,0.0000 <br />
0.0000,0.0000,0.0000,0.0000,0.0000,1.0000 <br />
0.0000,1.0000,0.0000,0.0000,0.0000,0.0000 <br />
0.0000,0.0000,0.0000,0.0000,1.0000,0.0000 <br />
