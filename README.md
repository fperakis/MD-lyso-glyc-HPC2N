# MD-lyso-glyc-HPC2N
An example of runing MD simulations using gromacs at HPC2N, project number: SNIC2021-22-656.

The simulation includes 10 lysozyme molecules (~200mg/ml) in a 23%mol water/glycerol solution. 
Protein and glycerol molecules are simulated using CHARMM36 and water with TIP4P/2005.
http://mackerell.umaryland.edu/charmm_ff.shtml

For the more details see `pipeline.txt`. 

-----
## Run it on HPC

To connect on the HPC2N use
```bash 
$ ssh username@kebnekaise.hpc2n.umu.se
```

To activate GROMACS and it's prerequisites use: 
```bash 
$ ml GCC/10.2.0  CUDA/11.1.1  OpenMPI/4.0.5
$ ml GCC/10.2.0  OpenMPI/4.0.5
$ ml GROMACS/2021
```

Submit jobs by
```bash
$ sbatch slurm/cpu.sh
```

Check status by
```bash
$ squeue -u username
```
