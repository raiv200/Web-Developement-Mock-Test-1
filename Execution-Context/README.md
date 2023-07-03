## Web development Mock Test-1

### Execution Context

Execution context refers to the environment in which JavaScript code is executed. It consists of the variables, functions, objects, and scopes that are accessible during the execution of code. It plays a crucial role in managing the execution of JavaScript programs.

It holds all the relevant information such as variables, function call etc. to execute a piece of JavaScript code. It keeps track of the state of the code and ensures that everything runs smoothly.

There are three types of execution contexts in JavaScript:

1. Global Execution Context:
  It is the default and outermost execution context.

2. Function Execution Context:
   Created when a function is called or invoked.

When JavaScript code is executed, the execution contexts are created and managed using a data structure called the "Execution Context Stack" or "Call Stack." The execution context stack follows a "Last-In, First-Out" (LIFO) order.

```js

function func1(){
  var first = 1;
  console.log("First Function started");
 function func2(){
   var second = 2;
console.log("SecondFunction started");

  }
console.log("Second Function ended ");

}
func1();
```

In the above code, we have two function calls (`func1` and `func2`) nested within the global execution context. When `func1` is called, its execution context is created and added to the top of the execution context stack. Similarly, when `func2` is called from within `func1`, its execution context is added on top of the stack.

The JavaScript engine always executes the code within the topmost execution context in the stack. Once the execution of that context is complete, it is removed from the stack, and the control moves to the next context below.

This process continues until all execution contexts have been processed, and the stack becomes empty, indicating the completion of the script execution.