**MOC**:: [[1. Python MOC]]
**Tags**:: #python #language
## Definition
Reactive programming is based [[Asynchronous]] model of execution. Everything is considered as streams in reactive programmin: Database calls, user clicks, failures, API calls, and so on. Data from different streams can be combined, manipulated, transformed and so on. Reactive programming basically applies the asynchronous data processing over these streams of data. It use [[Observables]] and [[Observers]] for communications.
## Reactive manifesto
- **Responsive**: to focus on providing fast and consistent response time, in the event of change in the the system.
- **Elastic**: the system can handle varying amount of loads, without failure.
- **Resilient**: the system must stay responsive, even in the event of failure.
- **Message driven**: asynchronous message passage between different components to ensure loose coupling.
Documentation: [Reactive Manifesto](https://www.reactivemanifesto.org).
## Advantages
- Aims to allow the programmer to focus on the data streams and not the asynchronous part of programming.
- Complex use of threads can be easily done, without going into the details.
- Improved use of resources in asynchronous context.
- Since, programmer does not code the asynchronous part of the program, the final code is more readable and compact.
