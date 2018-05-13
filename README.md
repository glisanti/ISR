# ISR
This MATLAB code provides the implementation of sparse re-weighted person re-identification from our paper:

**G. Lisanti, I. Masi, A. D. Bagdanov, A. Del Bimbo, "Person Re-identification by Re-weighted Sparse Ranking." in IEEE Transactions on Pattern Analysis and Machine Intelligence, 2015."**

![ISR](/media/ISR.png)

This code implements ONLY the re-identification algorithm from this paper and not descriptor extraction. In the *data/* directory we provide pre-computed features for some re-identification datasets. 
For more details about the descriptor please visit the https://github.com/glisanti/WHOS.

You will need a recent version of MATLAB and the Sparse Modeling and Optimization (SPAMS) package to use this code:
http://spams-devel.gforge.inria.fr/ . 

In the *spams-matlab/* directory we provide a copy of version 2.3 of the SPAMS Sparse Modeling toolkit.

We already provide a compiled version of SPAMS; in particular we provide the following MEX binary of SPAMS for:
- Linux 64 bit arch (tested on Ubuntu 12.04)
- Mac OS X 64 bit arch (tested on Lion and Mountain Lion)
- WinXP 64 bit arch (tested on Windows 7 and Windows XP64)

If there are any problems, please follow the directions in the *spams-matlab/* directory for compiling and installing SPAMS. All experiments from the paper above were run on an 8 core machine, and it is suggested that you start MATLAB according to the directions in the SPAMS directory so as to take full advantage of all available cores.

With this code you can reproduce the results from the above paper on:
- The VIPeR dataset (SvsS modality)
- The CAVIAR4REID dataset (SvsS, MvsM (N=5) modalities)

**Please cite our paper if you use this descriptor:**
> @ARTICLE{LisantiPAMI14,\
>  author={Lisanti, G. and Masi, I. and Bagdanov, A. and Del Bimbo, A.},\
>  journal={Pattern Analysis and Machine Intelligence, IEEE Transactions on},\
>  title={Person Re-identification by Iterative Re-weighted Sparse Ranking},\
>  year={2015},\
>  volume={37},\
>  number={8},\
>  pages={1629-1642},\
>  doi={10.1109/TPAMI.2014.2369055},\
>  ISSN={0162-8828}\
>}

## Organization of the demo distribution:

The structure of the code is the following:
- In the root are all files implementing our re-identification algorithm.
- In the *figure/* folder are the reference figures used in our paper.
- In the *data/* folder are .mat files used for precomputed features.
- In the *spams-matlab/* folder is SPAMS version 2.3 source and binary code.

## Running the demo:

To run the code on one of the pre-computed datasets, start MATLAB and ensure that a working version of SPAMS is in your MATLAB path. Then go to the root of our distribution and run:
```
L1_PeopleReid_Demo
```
You can change the dataset and tested modality at the top of the *L1_PeopleReid_Demo.m* file.

## Troubleshooting:

- If you get an *invalid MEX* error and you are on a NIX platform like Linux or Mac OS X, please consider starting MATLAB with the 'run_matlab.sh' script found in the SPAMS directory.

If you have any problem mail both Giuseppe Lisanti (giuseppe[dot]lisanti[at]unipv[dot]it) and Iacopo Masi (iacopoma[at]usc[dot]edu).



