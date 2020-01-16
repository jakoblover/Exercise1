# Reasons for concurrency and parallelism


To complete this exercise you will have to use git. Create one or several commits that adds answers to the following questions and push it to your groups repository to complete the task.

When answering the questions, remember to use all the resources at your disposal. Asking the internet isn't a form of "cheating", it's a way of learning.

 ### What is concurrency? What is parallelism? What's the difference?
 > Concurrency is when several tasks are run at the same time (though not necessarily simultaneous). This can be done through context switching on one core. Parallelism is when several tasks are run simultaneously in parallel on multiple cores. The difference is that concurrency switches between multiple tasks, while parallelism, a subset of concurrency, means those same tasks are actually run simultaneously.
 
 ### Why have machines become increasingly multicore in the past decade?
 > The increasing demand for lower power usage in portable devices have pushed the development of multicore processing. Parallelism allows a higher throughput of data processing using the same clock speed, this keeping power usage low.
 
 ### What kinds of problems motivates the need for concurrent execution?
 (Or phrased differently: What problems do concurrency help in solving?)
 > Concurrency allows multiple threads in a task to run at the same time. In a GUI application for example, you usually want to use multiple threads. If the data processing and GUI handling is in the same thread, the GUI will be less responsive. By moving the data processing to a separate thread, the GUI will be more responsive.

 ### Does creating concurrent programs make the programmer's life easier? Harder? Maybe both?
 (Come back to this after you have worked on part 4 of this exercise)
 > If done correctly, concurrent programs can be very powerful. It may make life a bit harder, but it increases the possibilities of what the program can do manyfold.
 
 ### What are the differences between processes, threads, green threads, and coroutines?
 > Processes are instances of computer programs that has its own resources, and may consist of several threads. A thread is the smallest unit of processing that can be run and scheduled. Green threads are threads that execute on a VM or in a runtime library instead of the kernel. A coroutine is a part of a program that can stop and yield to other parts of the program, and continue execution where it left off.
 
 ### Which one of these do `pthread_create()` (C/POSIX), `threading.Thread()` (Python), `go` (Go) create?
 > Threads
 
 ### How does pythons Global Interpreter Lock (GIL) influence the way a python Thread behaves?
 > It prevents python from running threads in parallel. Threads may only be run concurrently.
 
 ### With this in mind: What is the workaround for the GIL (Hint: it's another module)?
 > A module called multiprocessing mitigates this issue
 
 ### What does `func GOMAXPROCS(n int) int` change? 
 > This function changes the amount of cores the code is allowed to utilize
