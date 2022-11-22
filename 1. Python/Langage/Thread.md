**MOC**:: [[1. Python MOC]]
**Tags**:: #python #language

# Definition
- use native threads
- belong to a process
- lightweight, fast to start
- shared memory
- subject to the GIL
- suited to IO-bound tasks
- create 10s to 1000s workers

# Thread
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

