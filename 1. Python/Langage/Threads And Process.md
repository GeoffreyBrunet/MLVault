**MOC**:: [[1. Python MOC]]
**Tags**:: #python #language
## Thread vs Process
**Thread**:
- use native threads
- belong to a process
- lightweight, fast to start
- shared memory
- subject to the GIL
- suited to IO-bound tasks
- create 10s to 1000s workers
**Process**:
- use native processes
- has threads and child processes
- heavyweight, slow to start
- inter-processes communication
- not subject to the GIL
- suited to CPU-bound tasks
- create 10s of workers

## Thread
```python
from threading import Thread


def do_threading():
	thread_1 = Thread(target=func_1, args=(arg1, arg2))
	thread_2 = Thread(target=func_2, args=(arg1, arg2))
	thread_3 = Thread(target=func_3, args=(arg1, arg2))
	
	thread_1.start()
	thread_2.start()
	thread_3.start()
	
	thread_1.join()
	thread_2.join()
	thread_3.join()
```
The **start()** method start execution of the thread.
The **join()** method provides a way for one thread to block until another thread has finished.

## Process
```python
from multiprocessing import Process


def do_threading():
	process_1 = Thread(target=func_1, args=(arg1, arg2))
	process_2 = Thread(target=func_2, args=(arg1, arg2))
	process_3 = Thread(target=func_3, args=(arg1, arg2))
	
	process_1.start()
	process_2.start()
	process_3.start()
	
	process_1.join()
	process_2.join()
	process_3.join()
```
The `start()` method start execution of the process.
The `join()` method provides a way for one process to block until another thread has finished.

## Pool of workers
`Pool` provides a pool of reusable processes for executing ad hoc tasks.
The built-in `map()` function allows you to apply a function to each item in an iterable.
`Pool`provides an asynchronous parallel version of the `map_async()` function.
```python
from multiprocessing import Pool

pool = Pool(processes = 4)

input_list = range(0, 50000000)

result = pool.map_async(some_function, input_list)
```
