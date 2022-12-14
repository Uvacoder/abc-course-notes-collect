# Return a Function to Cancel an Async Behavior

[ð¹ Video](https://egghead.io/lessons/egghead-return-a-function-to-cancel-an-async-behavior)

One required feature on almost every asynchronous situation is to be able to cancel the action that requested to be executed in the future.

For this example, using a timeout, the challenge is that we need an identificator of the called timeout to be able to cancel immediately. One solution is to return the id from the `createTimeout` function to be used to `clearTimeout` to cancel the timeout.

But since the only way to cancel a timeout is by calling `clearTimeout` every time we can wrap that into a function for reusability. So instead of return the `id` from `createTimeout` we can return a function that calls the clear timeout behavior

```javascript
let createTimeout = (time) => (callback) => {
  let id = setTimeout(callback, time)
  return () => {
    clearTimeout(id)
  }
}
```

ð This syntax wraps the concept of **capturing behavior**

To use this is just matter of assign the `createTimeout` call to a function with a descriptive name and then call it when is required

```javascript
let cancelOne = onSecond(() => {
  console.log('one')
})
cancelOne()
```

> ð¨You gain a lot of power and flexibility when you wrap things inside of functions. The complexity you need to grow accustomed to is the idea of returning functions from other functions, and also passing functions into other functions

## References

- [source code](https://github.com/johnlindquist/crafting-functions/blob/returning-functions/src/index.js)
