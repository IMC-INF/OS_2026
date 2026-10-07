# Operating Systems Examples and Exercises in C

1. **Swap Two Integers by Reference**

   Write a C program (int_swap.c) that swaps the two integer values passed as parameters.  
   **Hint:** Both parameters have to be passed by reference.

   **Note:**  
   “Pass by reference” means passing the **address** of a variable instead of directly changing its value.

---

2. **Modify `create_pthread.c` to Accept Thread Count**  
   Modify the program to accept the **number of threads to create** as a command line parameter.  
   You can refer to './posix/pthreads_example.c`.

   **Note:**  
   Creating threads may fail. This is usually due to:
   - System resource limits (too many threads or insufficient memory)  
   - Invalid parameters  

   Always check the return value to handle errors safely.

   **Example runs:**
   ```bash
   ./create_pthread 5
   ```
   
   Result: (sequence can be different)
   ```bash
      Hello from thread 0  
      Hello from thread 1  
      Hello from thread 2  
      Hello from thread 3  
      Hello from thread 4  
      All threads completed. 
   ```
   **Example runs:**
   ```bash
   ./create_pthread 
   ```

   Result:
   ```bash
   Error: Wrong number of parameters.
   ```

   **Example runs:**
   ```bash
   ./create_pthread 0
   ```
   Result:
   ```bash
   Too few threads. Please specify a number greater than zero.
   ```
   
