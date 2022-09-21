**MOC**:: [[1. Python MOC]]
**Tags**:: #python #library
## Definition
[RxPy](https://rxpy.readthedocs.io/en/latest/) (Reactive Extension for Python) is a set of libraries for implementing [[Reactive Programming]] paradigm in Python. It have implementations for [[Observers]], [[Observables]], [[Data Operators]], and so on. It also have schedulers for [[Asynchronous]] programming that can be combined with other Python librairies like AsyncIO, PyGames and others.
## Installation
```shell
pip install rx
```
## Code examples
### Introduction example
#### Observer
There are the three events for observers:
1. on_next() - the next element in stream is recieved (if it exists)
2. on_completed()- the subscribed stream has finished transmitting
3. on_error() - for dealing with errors while transmitting
```python
from rx import Observer, Observable


class my_observer(Observer):
	def on_next(self, input_data):
		print("I have recieved {}".format(input_data))
		
	def on_completed(self):
		print("I have finished recieving data !")
		
	def on_error(self):
		# Define error according to your use case
		pass
```
#### Observable
Create observable:
```python
my_subscriber = Observable.from_(range(0, 20, 2))
```
Now subscribe the Observer(subscriber) to the Observable:
```python
my_var = my_subscriber.subscribe(my_observer())
```
[[Lambda]] function can be used instead of creating observer class and defining the functions:
```python
my_subscriber.subscribe(on_next = lambda x: print("I have recieved {}".format(x)), on_completed = lambda: print("completed"))
```
### Using Data Operators with RxPy
```python
my_observable = Observable.from_(range(0, 20, 2))
my_var = my_observable.subscribe(my_observer())
```
Filter Operator:
```python
my_observable = Observable.from_(range(0, 20, 2))
my_var = my_observable.filter(lambda x: x%4==0).subscribe(my_observer())
```
Distinct Operator:
```python
my_observable = Observable.from_([1, 2, 1, 3, 4, 2, 1, 4, 6])
my_var = my_observable.distinct().subscribe(my_observer())
```
Map Operator:
```python
my_observable = Observable.from_(range(0, 10))
my_var = my_observable.map(lambda x: x**2).subscribe(my_observer())
```
Chaining data operators:
```python
my_observable = Observable.from_(range(0, 10))
my_var = my_observable.map(lambda x: x**2).filter(lambda x: x%3==0).subscribe(my_observer())
```
