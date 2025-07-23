Project: Parallel Quick Sort with Work Stealing in C++
This project implements a parallel version of Quick Sort using a thread pool that supports work stealing.
This approach allows for efficient distribution of tasks between threads, minimizing downtime and improving performance when processing large amounts of data.
Main components of the project
1. ThreadPool class
Implements a thread pool with a work stealing mechanism.
Allows adding tasks to a queue and automatically redistributes them between threads to balance the load.
Includes internal queues for each thread, which facilitates efficient task distribution.
2. parallel_quick_sort function
Performs quick sort in parallel mode.
Uses recursion and std::promise/std::future mechanism to synchronize completion of subtasks.
For small arrays, uses sequential sorting (std::sort) for increased efficiency.
3. Main function main
Generates a large array of random numbers.
Creates a thread pool.
Starts parallel sorting.
Displays execution time and checks the correctness of the sorting.
