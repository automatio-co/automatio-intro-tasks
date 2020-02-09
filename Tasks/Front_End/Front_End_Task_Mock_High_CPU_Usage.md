# Front End Task: Mock High CPU and Memory Usage

You can submit the solution in any of the following ways:

- A private or public repo
- A deployed version
- A public blog describing the process
- A small video of browser

---

Sometimes we need to do some mock stress tests. 

Create a page and a script which upon opening will make CPU and memory usage very high to the specified limits. You can use any library, method or implementation. Some bundler like webpack/browserify/parcel is recommended.

---

## Sample output in Chrome Task Manager
![](http://i.imgur.com/9grAuH3.png)

## Sample function calls
```js
// by default it'll use one cpu core/thread and 100MB of memory
function mockCPUandMemoryLeak({ cpu = 1, memory = 100 }){
  // your code here
}
window.mockCPUandMemoryLeak = mockCPUandMemoryLeak;

mockCPUandMemoryLeak.init({ cpu: 6, memory: 1600 })
mockCPUandMemoryLeak.start() // starts the mock
mockCPUandMemoryLeak.stop() // stop the mock
```
