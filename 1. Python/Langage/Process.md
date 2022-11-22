**MOC**:: [[1. Python MOC]]
**Tags**:: #python #language 

# Defition
- use native processes
- has mutliple [[Thread]] and child processes
- heavyweight, slow to start
- inter-processes communication
- not subject to the GIL
- suited to CPU-bound tasks
- create 10s of workers

# Process
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

# Pool of workers
`Pool` provides a pool of reusable processes for executing ad hoc tasks.
The built-in `map()` function allows you to apply a function to each item in an iterable.
`Pool`provides an asynchronous parallel version of the `map_async()` function.
```python
from multiprocessing import Pool

pool = Pool(processes = 4)

input_list = range(0, 50000000)

result = pool.map_async(some_function, input_list)
```
