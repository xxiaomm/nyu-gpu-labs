## lab1

NYU GPU Lab 1: Write a program to process vectors in CUDA.


### Module load and Build

```bash
module load cuda-10.2  (from cuda-9.0 and higher(11.4) is OK)
nvcc -o vectorprog <cuda file name: xm2074.cu> -lm
```
An executable named `vectorprog` will be generated under the project root directory.

### Usage

```bash
./vectorprog <vector_size>
```

### Change Number of Blocks & Threads

Open `.cu` file and change the `BLOCK_NUM` and `THREADS_NUM` macros.


```c
#define BLOCK_NUM 4       // one grid contains 4 blocks.
#define THREADS_NUM 500   // one block contains 500 threads.   
```