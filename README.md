# `Event Loop`

![](https://github.com/newmohib/event-loop/blob/master/public/EventLoop-1.PNG)


### Event Loop Summary

    1: The Event Loop is a C program that orchestrates or co-ordinates the exicution 
    of synchronous and asynchronous code in Node.js

    2: It co-ordinates the execution of callbacks in six different queues

    3: They are nextTick, Promise, Timer, I/O, Check and Close Queues

### Executions Priority

    1: We use process.nextTick() method to queue into the nextTick queue.
    2: We resolve or reject a Promise to queue into the Promise queue.
    3: we use setTimeout or setInterval to queue into the timer queue.
    4: Execute an async method to queue into the I/O queue.
    5: Use setImmediate functions to queue into the check queue.
    6: Attach close event Listeeners to queue into the close queue.

`The order of executions follows the same order listed here`

`nextTick and Promise queues are executed in between each queue and also in between each callback execution in the timer check queues`

