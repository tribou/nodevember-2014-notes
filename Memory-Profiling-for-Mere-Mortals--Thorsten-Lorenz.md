# Memory Profiling for Mere Mortals
*Thorsten Lorenz*

- Initialization of app is not usually an issue
- Requests coming into your app
- Memory leak occurs when references to objects are retained even though that are no longer needed by your program

## Memory leak causes

- registered event handlers
- function closures
- registered event handlers
- leaking connections

## Garbage Collector

- follows retaining path from your GC root
- if reference to object is no longer found, it becomes subject to collection
- ```devtools/javascript-memory-profiling```
- if you reference something you don't need, you can still get memory leaks

## Troubleshooting Leaks

### Reproduce 

(sometimes watching process with ```top``` suffices)

- Print the PID of your process
- Use ```htop``` instead of top
- ab allows you to fire requests at a server
- V8 will crash when 1.5GB of memory is reached

### Isolate and find the culprit with tools like *Instruments* and *DevTools*

- Process
  - Take bottom line snapshot
  - Perform operation that may cause leak
  - Take another snapshot
  - repeat...
- Run Node with --expose-gc to expose the gc() method
- *Instruments* is like a frontend for *dtrace*
- Run Node with Xcode and gc exposed to allow memory profiling

### Profiling heap dumps

- Ensure advanced heap profiling is enabled (setting)
- kill -USR2 PID - exports a heap dump of a process
- Load heap file into Chrome DevTools
- Comparison of one heap dump to the next
- Summary of objects allocated between different heap dumps
- Closures show which functions are holding on to objects

## Considerations

- Name your functions
  - e.g. ```var foo = function foo() {};```
  - e.g. ```fs.readFile(file, function functionName(err, src) {});```

## Resources

https://thlorenz.github.io/v8-perf/
