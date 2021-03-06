# IOR-Benchmarks-Cori
Daily IOR Benchmarking on Cori CSCRATCH and Project Filesystem

Check out this repo, and launch this notebook in your browser, this daily monitor includes:
  1. Project (DVS), 1 node POSIX IOR read/write
  2. CSCRATCH (Lustre), 1 node MPI/POSIX FPP/SSF IOR read/write
  3. CSCRATCH (Lustre), 32 nodes MPI/POSIX FPP/SSF IOR read/write
  
You can change the parameter from 'readwrite' to 'write' or 'read', if you want to plot them separately.

You could also specify the number of days to plot the last few days of log, which is generally good, otherwise, the plot is too dense.
```python
  IOR_HSW_DIR="/project/projectdirs/mpccc/fbench/IOR_CSCRATCH/IOR_HSW"
  NODES_POSIXMPI_DIR="1node_posix_ssf"
  BLOCK_SIZE="_1000000_" 
  title="CSCRATCH HSW 1node posix ssf"
  latest=20
  parser_ior(IOR_HSW_DIR,NODES_POSIXMPI_DIR,BLOCK_SIZE,"readwrite",title,latest=latest) 
```
![Alt text](https://cloud.githubusercontent.com/assets/1396867/25825720/e4e0ccbc-33f8-11e7-990f-fbe421420919.png)

Available to NERSC employees.   


# Temporary Use for All Users (who don't have permission to fbench account):

1. git clone https://github.com/NERSC/ior-bench-cori
2. launch ipython-dev 
3. replace log directory '/project/projectdirs/mpccc/fbench/IOR_CSCRATCH//IOR_HSW’ with ‘/global/cscratch1/sd/fbench/IOR_Temp17//IOR_HSW’
4. replace log directory ‘/project/projectdirs/mpccc/fbench/IOR_DVS/1node_posix_fpp/CORI_dvs_1’ with ‘/global/cscratch1/sd/fbench/IOR_Temp17/IOR_DVS/1node_posix_fpp/CORI_dvs_1’
5. Run all in your notebook

