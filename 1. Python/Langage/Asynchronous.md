**MOC**:: [[1. Python MOC]]
**Tags**:: #python #language
## Definition
Multiple tasks can execute at time. For example, if two tasks are executed in this mode, one task has to waiting for I/O from user, the other task can start executing in the mean time to utilize the idle CPU time.
The idea is that the tasks are basically independent on another. For example, say task 2 need to compute mean of the array on disk, while task 1 to input array from user and do some computation the task 2 can start executing while task 1 is waiting on user input.
## Drawbacks
- Does not cause any blocking call.
- Since tasks are independent of each other, they can be executed in any order.
## AsyncIO
[AsyncIO](https://docs.python.org/fr/3/library/asyncio.html) is a library for asynchronous programming using the async/await syntax.
Install with:
```shell
pip install asyncio
```
Instead of `def`, `async def` is used for creatin asynchronous function. After, create tasks in `event_loop`. For running this `event_loop`, need `get_event_loop`, `run_until_complete` for executing code, and `close` it.
```python
import asyncio

 
async def f1(x):
	print("Starting function f1")
	for i in range(0, x):
	print("X right now is {}".format(i))
	await asyncio.sleep(0.01)
	print("Function f1 ended")

  
async def f2(my_str, times):
	print("Starting function f2")
	for i in range(0, times):
	print(my_str)
	await asyncio.sleep(0.01)
	print("Function f2 ended")


async def f3(my_str1, my_str2):
	print("Starting function f3")
	print(my_str1 + my_str2)
	print("Function f3 ended")


async def async_call_new():
	f1_obj = event_loop.create_task(f1(10))
	f2_obj = event_loop.create_task(f2("Hello Yolo", 10))
	f3_obj = event_loop.create_task(f3("Hello World", "Goodbye!"))
	await asyncio.wait([f1_obj, f2_obj, f3_obj])


event_loop = asyncio.get_event_loop()
event_loop.run_until_complete(async_call_new())
event_loop.close()
```
