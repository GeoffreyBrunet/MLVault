**MOC**:: [[1. Python MOC]]
**Tags**:: #python #language
## Definition
In Synchronous, only one task can execute at a time. For example, if two tasks are executed in this mode, one task has to wait for the other one to finish before it can be started.
The idea is that the tasks are basically dependent on another. For example, say task 2 needs input from task 1 to start the computation, hence it must wait for task 1 to finish completely.
## Drawbacks
- It can lead to idle CPU time.
- Tasks are blocked if the previous task does not finish it's computation.
- Basically only one task can execute at time.
