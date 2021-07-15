# Algorithmic Challenges

Hi there! 👋

These bite-sized challenges will help us reason about your ability to write concise, elegant, type-safe code.

Requirements:

- written in TypeScript in `strict` mode
- avoid `any` if you can
- make it as readable as possible

Optionally, you can choose to:

- write unit tests
- write a README or a method/function documentation for the consumer of your code
- make a GIF showing how it works in your console
- avoid supporting edge cases, as long as you document this behaviour in code
- do anything else you feel important to do

## Promise.all

Implement a [Promise.all](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise/all) function which takes an array of promises and returns a single promise that resolves to an array of the results, and rejects as soon as any of the promises rejects.

Example:

```
await Promise.all([
    Promise.resolve('foo'),
    new Promise(r => setTimeout(() => r('bar'), 1000)),
    'baz'
]);
// Resolves ['foo', 'bar', 'baz'] in about 1 second
```

No need to follow the ECMAScript spec to letter, just implement what the summary says.

## Wait for Event

Implement a `waitForEvent` function that:

- takes `EventEmitter`, event name and optionally a timeout as its arguments
- returns a Promise which:
    - resolves once an event with specified name is fired
    - resolved result should be the event data (i.e. the second argument of `emitter.emit`)
    - rejects if timeout is specified and event was not emitted in specified time frame
- does not leak events

Example:

```
const emitter = new EventEmitter();

waitForEvent(emitter, 'foo').then(console.log);

setTimeout(() => emitter.emit('foo', { hello: 'World' }), 1000);

// Types `{ hello: 'World' }` in about 1 second
```
