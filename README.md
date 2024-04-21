# multithreading
# methodology
In this experiment, we're exploring the performance of matrix multiplication across 100 matrices, each sized 1000 x 1000, while varying the number of threads used. The matrix multiplication is executed through a function called multiply(), which employs the np.dot() function to compute the product of two matrices and then stores the result in a specified index of the output array.

To manage the utilization of threads, we've designed the run_threads() function. This function enables the execution of matrix multiplication with a range of threads, from 1 to 10. Initially, it initializes a list called threads to hold thread objects. Then, it iterates over the list of matrices, creating a new thread for each multiplication operation using the threading.Thread() constructor. Each thread starts its execution using the start() method. After creating all threads, the function waits for all threads to finish their operations using the join() method and records the time taken for the multiplication operations.

Matrix Generation
Firstly, a constant matrix A of size 1000x1000 is generated using numpy.random.rand(). Then, a list containing 100 random matrices of the same size is created.

Execution
The run_threads() function is invoked for each number of threads ranging from 1 to 10, capturing the time taken for each operation. The results are stored in the results_table list along with the corresponding number of threads.
# results
![image](https://github.com/himanshu9988/multithreading/assets/100368433/e5216d34-c788-4f39-abe5-45587ca9cf83)

![image](https://github.com/himanshu9988/multithreading/assets/100368433/061c4520-b69a-47ce-b9c9-072c13e7c2bb)

![image](https://github.com/himanshu9988/multithreading/assets/100368433/95ad3e62-d718-4bf7-a51b-4430f138027d)
