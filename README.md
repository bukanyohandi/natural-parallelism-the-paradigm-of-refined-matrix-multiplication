In contemporary artificial intelligence, matrix multiplication is omnipresent, making it a foundational component of intricate computations. With the advent of architectures, optimizing matrix multiplication is more relevant than ever. The scope of this project will be solely focus on the most generalized form: dense matrix multiplication.

The objective of this project is to improve a dense matrix multiplication function by implementing various optimization techniques. The function’s computational performance will be enhanced through systematic optimization by addressing aspects of memory locality, data-level parallelism, thread-level parallelism, and process-level parallelism.

Within the submitted zip file, a folder project can be found, this will be the main project folder.
1. Navigate to the folder
2. Run `run.sh` or simply paste the below sequence of commands:
```
scancel -u {username} # to cancel submitted batch jobs
mkdir build
cd build
cmake ..
make -j4
cd ..
sbatch src/sbatch.sh
sbatch src/sbatch-perf.sh # to display profiling results
squeue # to check batch jobs queue
```

By default, the above commands will execute the a multiplication between matrices in `matrix5.txt` and `matrix6.txt`. If one wish to test other matrices, one can simply modify the appropriate scripts located in `src/sbatch.sh`. Additional scripts for different matrices might also be found in the parent directory, `..`. Make sure relevant matrices can be found in `matrices` directory. Upon completion, one can find the experiment results in the directory: `matrices/`.
