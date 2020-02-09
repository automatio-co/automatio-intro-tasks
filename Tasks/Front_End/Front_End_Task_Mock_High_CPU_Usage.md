# Front End Task: Mock High CPU and Memory Usage

You can submit the solution in any of the following ways:

- A private or public repo
- A deployed version
- A public blog describing the process
- A small video of browser

---

Sometimes we need to do some mock stress tests. 

Create a page and a script which upon opening will make CPU and memory usage very high to the specified limits. Some bundler like webpack/browserify/parcel is recommended. You can use any library, method or implementation like class, prototypes, buffer, loops, arrays etc.

---
# MockMemory Leak
## Sample function call with only memory mock
```js
function mockMemoryLeak(){}
mockMemoryLeak.prototype.init = ({ memory = 100 }) => {} // your code
mockMemoryLeak.prototype.start = () => {} // your code
mockMemoryLeak.prototype.stop = () => {} // your code
window.mockMemoryLeak = mockMemoryLeak;

const mocker = new mockMemoryLeak()
mocker.init({ memory: 1000 })
mocker.start() // starts the mock
mocker.stop() // stop the mock
```

## Sample Output in Chrome Task Manager
![](http://i.imgur.com/lrcgyoD.png)

# Mock CPU and Memory Leak

## Sample function calls with CPU and Memory
```js
// by default it'll use one cpu core/thread and 100MB of memory
function mockCPUandMemoryLeak(){}
mockCPUandMemoryLeak.prototype.init = ({ cpu = 1, memory = 100 }) => {} // your code
mockCPUandMemoryLeak.prototype.start = () => {} // your code
mockCPUandMemoryLeak.prototype.stop = () => {} // your code
window.mockCPUandMemoryLeak = mockCPUandMemoryLeak;

const mocker = new mockCPUandMemoryLeak()
mocker.init({ cpu: 6, memory: 1600 })
mocker.start() // starts the mock
mocker.stop() // stop the mock
```

## Sample output in Chrome Task Manager
![](http://i.imgur.com/9grAuH3.png)
