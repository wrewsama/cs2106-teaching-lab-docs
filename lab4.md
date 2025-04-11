# Lab 4

#### Comments from previous lab
* Q1.2: This question was only asking for mutual exclusion, not a total order
    * Need to provide some execution order that results in 2 or more processes inside the critical section
* Q1.4: Remember that `sem_wait` and `sem_post` don't just increment/decrement the value in the semaphore
    * if the sem value is 0, `sem_wait` will cause the process/thread to wait
    * if there are waiting processes/threads, `sem_post` will wake one up
* Q3.3: Many possible answers, including but not limited to:
    * Time taken to create shared memory (timer starts after)
    * Time taken to spawn new processes with `fork()` (same as above)
    * Overhead of context switching (`time.h`'s `clock()` function only measures the parent's **processor time** (i.e. amount of time the CPU spends executing this process))
    * Work done by child processes (same as above)
* Side note: Please adhere to the submission instructions in the lab sheet

#### Demo Instructions
* For each allocation algorithm (Bitmap, Linkedlist, Buddy):
    * Run the `harness`
    * All assertions should pass and the program should not crash

#### Other Comments
This is the last lab. Good luck & have fun for finals!
