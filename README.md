This repository provides a description of the data analysis tools used for a sucrose nanocluster experiment which was performed at the Linac Coherent Light Source (LCLS) and is described in 

> Phay J. Ho *et al.* The role of transient resonances for ultra-fast imaging of single sucrose nanoclusters *Nat. Comm.* **X**, Y (2019). [DOI](DOI).

The processed and sized data has been deposited in the Coherent X-ray Imaging Data Base (CXIDB) with ID **119** and can be downloaded from here: [http://cxidb.org/id-119.html](http://cxidb.org/id-119.html)

### Run numbers and photon energies ###
Photon energy [eV] | Run numbers 
-------------------| -----------
530                | 6,8,9,11
800                | 12,47
1000               | 13
1140               | 14
1483               | 15

### Data reduction and pre-processing ###
The data has been processed with [Hummingbird](https://github.com/fxihub/hummingbird) using the configuration and tools deposited here: [https://github.com/mhantke/electrospray_injection](https://github.com/mhantke/electrospray_injection). The output of this processing pipeline is deposited in [http://cxidb.org/data/119/preprocessed/](http://cxidb.org/data/119/preprocessed/).

### Size and intensity determination for each sucrose nanocluster ###
For size/intensity determination of each single sucrose particle, the [libspimage](https://github.com/FXIhub/libspimage) library has been used to fit the 
diffraction pattern of spheres to the data. An example tutorial for this sizing procedure is described in this repository: 
[sizing_example.ipynb](sizing_example.ipynb). This sizing pipeline has been applied to all sucrose events, the output is deposited in [http://cxidb.org/data/119/sizing/](http://cxidb.org/data/119/sizing/).

### Error analysis ###
It should be common practice to calculate the uncertainty for each size/intensity estimate, here is an example of how this can be done: [sizing_error_analysis.ipynb](sizing_error_analysis.ipynb). A more detailed description of this approach is given in the supplementary of the publication.
