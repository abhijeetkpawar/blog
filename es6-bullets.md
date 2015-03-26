ES6 Bullet points
=================

## Class ##  

1. Classes are just syntactic sugar.  
2. Instantiating an es6 class has same syntax as of prototypal way  
3. `constructor()` is automatically called on creating instance of the class.  
4. `extends` keyword is used to inherit from class  
5. `super()` call returns the execution of same function from parent
  
    class LogView extends View {
      render() {
    	var compiled = super();
    	console.log(compiled);
      }
    }

## Promise ## 

- A promise can only succeed or fail once. It cannot succeed or fail twice, neither can it switch from success to failure or vice-versa
- If a promise has succeeded or failed and you later add a success/failure callback, the correct callback will be called, even though the event took place earlier

### State of Promise:
The core idea behind promises is that a promise represents the result of an asynchronous operation. A promise is in one of three different states:

 - **Pending** - The initial state of a promise.
 - **Fulfilled** - The state of a promise representing a successful operation.
 - **Rejected** - The state of a promise representing a failed operation.

### Fate of Promise:
Promises have two possible mutually exclusive fates: resolved, and unresolved.

 - A promise is **resolved** if trying to resolve or reject it has no effect, i.e. the promise has been "locked in" to either follow another promise, or has been fulfilled or rejected.
 - A promise is **unresolved** if it is not resolved, i.e. if trying to resolve or reject it will have an impact on the promise.

A promise can be "resolved to" either a promise or thenable, in which case it will store the promise or thenable for later unwrapping; or it can be resolved to a non-promise value, in which case it is fulfilled with that value.

*A promise whose fate is unresolved is necessarily pending.*

###Promise API Reference###

**Static Methods**


**`Promise.resolve(promise);`**  
Returns promise (only if promise.constructor == Promise)

**`Promise.resolve(thenable);`**  
Make a new promise from the thenable. A thenable is promise-like in as far as it has a "then" method.

**`Promise.resolve(obj);`**
Make a promise that fulfills to obj. in this situation.

**`Promise.reject(obj);`**  
Make a promise that rejects to obj. For consistency and debugging (e.g. stack traces), obj should be an instanceof Error.

**`Promise.all(array);`**  
Make a promise that fulfills when every item in the array fulfills, and rejects if (and when) any item rejects. Each array item is passed to Promise.resolve, so the array can be a mixture of promise-like objects and other objects. The fulfillment value is an array (in order) of fulfillment values. The rejection value is the first rejection value.

**`Promise.race(array);`**  
Make a Promise that fulfills as soon as any item fulfills, or rejects as soon as any item rejects, whichever happens first.

**Constructor**:   
**`new Promise(function(resolve, reject) {});`**  
Note: Any errors thrown in the constructor callback will be implicitly passed to reject().

**Instance Methods**

**`promise.then(onFulfilled, onRejected)`**  
onFulfilled is called when/if "promise" resolves. onRejected is called when/if "promise" rejects. Both are optional, if either/both are omitted the next onFulfilled/onRejected in the chain is called. Both callbacks have a single parameter, the fulfillment value or rejection reason. "then" returns a new promise equivalent to the value you return from onFulfilled/onRejected after being passed through Promise.resolve. If an error is thrown in the callback, the returned promise rejects with that error.

**`promise.catch(onRejected)`**  
Sugar for promise.then(undefined, onRejected)

References:   
Specification: https://promisesaplus.com/
Polyfill: https://github.com/jakearchibald/ES6-Promises#readme
MDN: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise
