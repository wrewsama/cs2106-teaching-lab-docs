# Lab 1

### About Me
* Name: Andrew Lo Zhi Sheng
* Course / Year: Y4 CS
* Telegram: `@wrewsama` (Expect slow response after 10pm, I'm sleeping hehe)
* email: `andrewlo@u.nus.edu` (try to use tele instead)

### How My Lab Sessions Work
**Consultation Weeks**
* This is **OPTIONAL**
* But I will be in the lab to answer any questions (or you could just ask me on telegram)

**Demo Weeks**
* This is the important one
* If you need to miss this, please contact the Profs and me with a **valid reason** to arrange a makeup session. If you're absent without a valid reason, you will be given a 0 for the demo part of the lab (but you'll still get some credit for submitting the report)
* I will display a doc like this one on screen with some info like:
    * Common mistakes from the previous lab
    * Overview and demo instructions for the current lab
* You can immediately come up to the front and queue up to demo (with your lab partner, if you're both in the same lab group)
* Once done with the demo and I take your attendance, you are dismissed :)

### Demo Instructions
**Demo 1**
1. Compile and run your program
2. Show the results are correct:
    1. Reduce result: 45.00
    2. Flex Reduce with sum: 45.00
    3. Flex Reduce with prod: 362880.00

**Demo 2**
1. Compile your program using the command you gave in Question 3.3
2. Run valgrind - should have 0 errors / leaks 
3. Run the program - should match the output in the question paper

**Demo 3**
1. **Modify `testdir.c` to delete all the remaining files from the hashtable** (the given one doesn't delete them which results in a memory leak)

example:
```c
delete_file(NEW_FILE, hash, hashtable, TABLE_LEN);
for(i=0; i<NUM_FNAMES; i++) if (i != 1) delete_file(fnames[i].filename, hash, hashtable, TABLE_LEN);
```
2. Compile your program (_don't forget the `-g` flag!_)
3. Run valgrind - should have 0 errors / leaks
4. Run the program - should match the output in the question paper

### Lab 1 Overview
* C Programming
    * Function Prototypes (part 1)
    * Function Pointers (part 1)
    * Using `valgrind` to check your memory access (part 3 and 4)
* Explore different segments of a process' memory address space [Lecture 2]
    * Stack, Data (part 2)
    * Allocating and releasing memory from the Heap using `malloc` and `free` (part 3)

### FAQ From My Previous Class
**I can't get xlog to work!**
- For demoes, I personally don't care which environment you use. Feel free to use `stu` instead or download `gcc` and `valgrind` to compile / run / debug locally

**I'm getting a memory leak in part 4.**
- There is a bug in `testdir.c`, see step 1 in the Demo 3 instructions below

**`flex_reduce` in part 1 is already implemented!**
- yeah we leaked it by accident oops

