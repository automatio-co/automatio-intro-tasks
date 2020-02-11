# JS Challenge: `Delayed Promises`

**First make sure the code is well commented, tested and have a nice documentation** and then you can submit the solution in any of the following ways:

- A private repo (add `taher@vanila.io` as collaborator)
- A secret GitHub gist
- A public blog describing the process.

---

**Create a set of functions** that will allow to run multiple promises with delays, both sequencially and parallelly.

# Rules:
## Code:
- The code must be commented well.
- You must write some tests using mocha or jest.
## Submission:

You will write the functions and the possible test input/output as well, but we will evaluate it with our input and output later.

You can do either of following, the code must remain private (until next two weeks), so other developers cannot copy and paste the solution from google.


- Create a **secret github gist** which includes a complete code and example and provide link to it.
- In case you are using other npm modules, create a **private github repo** and invite **entrptaher**
# Steps:

Read the comments carefully to understand the requirements and join the pieces together. 

Create some dummy functions with random output, use your imagination and do whatever you want to do here.

```js
    async function somePromiseFunction(args) {
      // do something with the provided arguments
      // return some data after some async calculations
      return args[0] + args[1].foo
    }
    
    async function anotherPromiseFunction() {
      // Divide two Big Integer here on this function
      // without using any npm package
      // bigInt1 and bigInt2 are not 0, and both have more than 17 digits
      // ie: 100000000000000000 (has 18 digits)
      // bigInt1 is smaller than bigInt2
      // it must not return 0 
      // it should return the decimal points if available
      return bigInt1/bigInt2
    
      // or throw some errors
      throw new Error('this promise should fail');
    }
```

Then there will be an actions array with two different structures for input

```js
    const actions = [
      // somePromiseFunction will run after 1s of executing delayedActions
      { fn: somePromiseFunction, delay: 1000, args: ["bar", { foo: "baz" }] },
      // anotherPromiseFunction will run after 5s  of executing delayedActions
      { fn: anotherPromiseFunction, delay: 5000 },
      // we should be able to add more actions here
      // we should be able to provide this format as well
      [somePromiseFunction, 1000, ["bar", { foo: "baz" }]],
      [anotherPromiseFunction, 5000]
    ];
```

Write the **delayedActions** function which will accept some actions array and options,

```js
    // if recursive is truthy, then the actions will run one after another
    // otherwise all of them will run at once
    // by default it'll be true
    
    // if errorExit is truty, then exit on any given error from any action promise
    // otherwise handle the error and push the error to the results array
    // by default it'll be false
    function delayedActions(actions, { recursive = true, errorExit = false }) {
      // handle -0, NaN, null and any negative number as delay without crashing
      // run current function after the provided delay
      // push result to an array
      // if another action is present, run it
      // return the array with all results from all actions
      // results will include information about all actions
    }
```

## Output:

Run the function with random functions,
```js
    delayedActions(actions).then(console.log);
```
Here is a sample output,

```
    [
      { 
        success: true, 
        startedAt: <Date Object>, 
        endedAt: <Date Object>, 
        result: <some result from promise>
      },
      { 
        success: false, 
        startedAt: <Date Object>, 
        endedAt: <Date Object>, 
        error: <Error Object> 
      }
    ]
```

Sample for some promise that throws error and errorExit is true by default, it will not return result, instead it’ll throw the error at once and halt execution.

```js
    delayedActions(actions, { recursive: true, errorExit: true }).then(console.log);
```

Similar output:

![](https://paper-attachments.dropbox.com/s_133D7E5615DB8B9F3306FC8A68F5BC10EF3C1A23063AEA3DADA1DA4A3D6C5F16_1575125751349_image.png)
