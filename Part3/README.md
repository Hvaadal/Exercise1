# Reasons for concurrency and parallelism


To complete this exercise you will have to use git. Create one or several commits that adds answers to the following questions and push it to your groups repository to complete the task.

When answering the questions, remember to use all the resources at your disposal. Asking the internet isn't a form of "cheating", it's a way of learning.

 ### What is concurrency? What is parallelism? What's the difference?
 > *Concurrency is a core switching between two tasks with a high enough frequency, making it look like the tasks are running at the same time. Parallellism is two tasks actually running at the same time. For parallelism, two or more cores are needed, since it is impossible to achieve with only one piece of hardware.*
 
 ### Why have machines become increasingly multicore in the past decade?
 > *To increase speed, the operating frequency of the core must be increased. This requires more energy for higher frequencies. Therefore it is more efficient to distribute the load over multiple cores.*
 
 ### What kinds of problems motivates the need for concurrent execution?
 (Or phrased differently: What problems do concurrency help in solving?)
 > *Problems that require different tasks to run at the same time, using just one processor.*
 
 ### Does creating concurrent programs make the programmer's life easier? Harder? Maybe both?
 (Come back to this after you have worked on part 4 of this exercise)
 > *Easier in the way that one can focus on each problem seperately while solving several problems. Harder because a lot of problems arise when the problems og tasks share properties or are connected in some other way.*
 
 ### What are the differences between processes, threads, green threads, and coroutines?
 > *Processes and threads are mainly the same thing, but threads can have access to a shared memory. No memory is shared between different processes.
	Using coroutines is a way of providing concurrency, but the different coroutines are made to cooperate with each other, and multitasked thereafter. 
	Green threads are spawned by a runtime library or virtual machine (VM), and native threads by the underlying OS (Wikipedia).*
 
 ### Which one of these do `pthread_create()` (C/POSIX), `threading.Thread()` (Python), `go` (Go) create?
 > *Green threads*
 
 ### How does pythons Global Interpreter Lock (GIL) influence the way a python Thread behaves?
 > *Only one python thread at a time is allowed to access python objects.*
 
 ### With this in mind: What is the workaround for the GIL (Hint: it's another module)?
 > *IronPython is a Python compiler, that does not have a GIL.*
 
 ### What does `func GOMAXPROCS(n int) int` change? 
 > *The number of operating system threads that can run Go code.*
