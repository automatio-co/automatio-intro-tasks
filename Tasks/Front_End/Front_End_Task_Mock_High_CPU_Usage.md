# Front End Task: Mock High CPU and Memory Usage

**First make sure the code is well commented, tested and have a nice documentation** and then you can submit the solution in any of the following ways:

- A private repo (add `taher@vanila.io` as collaborator)
- A deployed version
- A public blog describing the process
- A small video of browser

---

Sometimes we need to do some mock stress tests. 

Create a page and a script which upon opening will make CPU and memory usage very high to the specified limits. Some bundler like webpack/browserify/parcel is recommended. You can use any library, method or implementation like class, prototypes, buffer, loops, arrays etc.

---
# Mock Memory Leak
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

# Mock CPU Leak

## Sample function calls with CPU
```js
// by default it'll use one cpu core/thread
function mockCPULeak(){}
mockCPULeak.prototype.init = ({ cpu = 1 }) => {} // your code
mockCPULeak.prototype.start = () => {} // your code
mockCPULeak.prototype.stop = () => {} // your code
window.mockCPULeak = mockCPULeak;

const mocker = new mockCPULeak()
mocker.init({ cpu: 6 })
mocker.start() // starts the mock
mocker.stop() // stop the mock
```

## Sample output in Chrome Task Manager
![](http://i.imgur.com/beDqpb6.png)
