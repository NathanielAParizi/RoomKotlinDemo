# RoomKotlinDemo

This is a demonstration of both SQLite Open Helper and Room.

************************

Application will allow users to store, update, delete, and read entries in the SQLite database.

1. Define the following thread synchronization approaches:
        - Locks 
		
	 locks are "advisory locks" which means that each thread will cooperate by acquiring the lock before accessing the same data. When a thread acquires a lock (has access to resources) then it is said to have "entered the moniter". Locks play an integral part of how threads interact with eachother in asynchronous systems.		
        - Mutex
		
	Mutex and locks are very similar. Here are some differences:
			
	-A mutex is a synchronization object. You acquire a lock on a mutex at the start  of a part in the code, and then afterwards release it once finished. This must be done to prevent any other thread accessing the same data contemporaneously. The mutex will have multiple threads attempting to access it.  A mutex's lifespan lasts for as long as the data that it's protecting. 

	-A lock object is an object that encapsulates a given lock on the mutex. When the object is constructed it will acquire the lock on the mutex. When it is destructed the lock is released. 
		
       
	 - Semaphores
		
	A semphaore can be thought of as a traffic light in an intersection, it is simply a variable or abstract data type which is used to control access of a resource by multiple processes (signals) in a concurrent system. 
		
      - Synchronized
		
		Process synchronization refers to the notion that many different processes must unite at a given point in order to execute a subsequent action.
	
		
     - Volatile
		
		the volatile keyword in Java and C++ indicates that a value may change between different accesses, even if it does not appear to be modified. A variable can be written or read to main memory or the CPU cache. Volatile allows for a variable to by read or written into main memory rather than the CPU cache. It is an important way in managing variables in multithreaded systems.		
		
		
     - Atomic
		
		Declaring an atomic variable guarantees that substeps of the operation are completed within the given thread which they are to be executed in and must not be interrupted by any other threads.
		
		
2. Define Deadlock conditions.

Deadlock occurs when a necessary condition is never met because two or more processes are waiting for a specific resource in order to be satisfied and have the system continue operation. 

3. Define Race conditions.


A race condition is an undesirable situation that occurs when a system attempts to peform two operations at the same time with a unintended outcome. An example of this a conflict when a given resource is shared by two separate processes in an asynchronous system with unwanted results. 

4. What is a memory leak?	

 When an app incorrectly manages memory allocations such that that memory which is no longer needed is not released. Another aspect of memory leaks is when an object is stored into memory but cannot be accessed.

5. What is an ANR and what are some common causes?

Application Not Responding, usually from the main thread of an Activity becoming unresponsive for longer than 5 seconds, or a Broadcast Reciever not receiving a signal for longer than 10 seconds. This is actually different from a crash, because a crash will occur when a bug is encountered such as a unhandled exception or run-time error. There will be a dialogue box asking for the option to 'wait' or 'ok' to close the app.
