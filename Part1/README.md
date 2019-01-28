# Mutex and Channel basics

### What is an atomic operation?
> In concurrent programming: Program operations that run completely independent of any other processes. If for example a process is going to check if a lock is enabled (multiple/group of reads/writes), this needs to happen atomically

### What is a semaphore?
> A semaphore is something that is used to controll access to a common resource, preventing two processes accessing a recource that only can handle one access at a time. This can for example be counting semaphores and binary semaphores (locks)

### What is a mutex?
> A mutex controlls the resource usage for threads. When a thread wants a resource, it "ask the mutex", and the mutex will "give the lock" if/when the "lock is free". A mutex is a type of semaphore ("SEMAPHORE is SIGNALS, MUTEX is OWNERSHIP")

### What is the difference between a mutex and a binary semaphore?
> Mutex is used to give exclusive access to a resource, while a binary semaphore should be used for synchronization

### What is a critical section?
> A critical section is where a program is accessing shared recources. This is the only times a program can destroy for other processes. To avoid race conditions we can make sure that two programs does not enter critical section at the same time

### What is the difference between race conditions and data races?
 > A race condition is when a program is non-derministic because of timing related problems, while a data race is when a program acces the same memory space at the same time without ordering. An example of both of these are two threads accessing a shared variable at the same time

### List some advantages of using message passing over lock-based synchronization primitives.
> You are not as vulnerable to race conditions and deadlocks when you do not use the shared memory-concept. It is also easier to achieve higher performance with message passing.

### List some advantages of using lock-based synchronization primitives over message passing.
> It is easier to achieve correctness with a lock-based synchronization system.
