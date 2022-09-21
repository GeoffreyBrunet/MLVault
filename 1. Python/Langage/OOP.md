**MOC**:: [[1. Python MOC]]
**Tags**:: #python #language
## Iterator
Class is keyword for Python constructor.
All classes have a function called `__init__()`, which allows you to do some initializing when the object is being created.
To create an object/class as an iterator you have to implement the methods `__iter__()` and `__next__()` to your object.
The `__iter__()` method acts similar, you can do operations (initializing etc.), but must always return the iterator object.
The `__next__()` method also allows you to do operations, and must return the next item in the sequence.
```python
class myclass:
	def __init__(self):
		self.max = max
	# returns the iterator object itself:
	def __iter__(self):
		self.n = 0 return self
	# return the next item in the sequence:
	def __next__(self):
		if self.n <= self.max:
			# Do anything
			return result
		else:
			raise StopIteration
```

## Generator
For declaring a generator, create a method, but with multiple `return` statements, declared with `yield` keyword.
The difference is that while a `return` statement terminates a function entirely, `yield` statement pauses the function saving all its states and later continues from there on successive calls.
```python
def my_gen():
	x = 5
	y = 6
	yield x, y
	
	x += y
	yield x,y
	
	x+=1
	y+=10
	yield x,y
```
