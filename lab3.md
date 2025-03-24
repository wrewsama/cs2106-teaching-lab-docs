# Lab 3

#### Comments from previous lab
* Generally really well done
* Please submit on time

#### Demo Instructions
**Demo 1**
* Compile and run `lab3p1-sem.c` (remember to compile with the `lpthread` flag!)
* Ensure each child runs in order from `child 0` to `child 4`

**Demo 2**
* Compile and run `test_barrier.c` (remember to compile with the `lpthread` flag!)
* The output for each test should look something like:
```
**Parent waiting for children**

    Child x slept for y seconds and has now reached the barrier
    ...
    Child a slept for b seconds and has now reached the barrier

**All the children have returned**
```
* note that the sleep times and the order of the child processes doesn't matter, all we need is for all children to reach the barrier first, then return together, for each test case
