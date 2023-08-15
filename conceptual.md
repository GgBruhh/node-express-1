### Conceptual Exercise

Answer the following questions below:

- What are some ways of managing asynchronous code in JavaScript?
  awaiting feedback and ordering it to ensure that it will have a flow to it

- What is a Promise?
  a promise is a promise to return something, this can be fufilled and return the data or it can be a bad promise and not return data

- What are the differences between an async function and a regular function?
  async functions await for the result to move on as regular functions will just continue to fire off until complete

- What is the difference between Node.js and Express.js?
  express is built off of node and just adds more functionality, such as routing, middleware and many others

- What is the error-first callback pattern?
  a function that returns an error object whenever any successful data is returned by the function

- What is middleware?
  middleware is stuff that can help developers and maybe even users understand what is happeneing behind the scenes in the terminal. It normally is logging what is happeneing at all times or something of that nature

- What does the `next` function do?
  the `next` function is to ensure that the code continues to run after the data is returned. it will allow the rest of the functions to fire off once that required data is given

- What are some issues with the following code? (consider all aspects: performance, structure, naming, etc)
  the performance would be lacking because you would be awaiting all three links one after the other

```js
async function getUsers() {
  const elie = await $.getJSON('https://api.github.com/users/elie');
  const joel = await $.getJSON('https://api.github.com/users/joelburton');
  const matt = await $.getJSON('https://api.github.com/users/mmmaaatttttt');

  return [elie, matt, joel];
}
```
