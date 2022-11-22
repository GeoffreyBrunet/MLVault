**MOC**:: [[1. Python MOC]]
**Tags**:: #python #library 

# Init Python project
- Setup new project:
```shell
hatch new new_project
```
- Setup new project in existing folder:
```shell
hatch new --init
```
- Create virtual environment:
```shell
hatch env create
```
- Entering environments:
```shell
hatch shell
```
- Print where your environment's Python is located:
```shell
python -c "import sys;print(sys.executable)"
```
- Run script without beeing in virtual environement:
``` shell
hatch run python -c "import sys;print(sys.executable)"
```
- Delete virtual environement:
```shell
env remove
```
or 
```shell
env prune
```
