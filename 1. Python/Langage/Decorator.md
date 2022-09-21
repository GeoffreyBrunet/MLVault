**MOC**:: [[1. Python MOC]]
**Tags**:: #python #language
## Creating decorator
**Decorator**: Take function as input (for enhance it's functionality) and return a new function.
```python
 def my_func():
	do_anything()


def my_decorator(my_fn):
	def modified_function():
		my_fn()


return modified_function my_new_function = my_decorator(my_func)
```

## Using annotation for calling decorator
Using decorator with `@name`:
```python
@decorator
my_func:
	# Do anything
```
Is equal to using while creating new function:
```python
new_func() = decorator(my_func)
```
