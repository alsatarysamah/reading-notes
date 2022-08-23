# Context.Provider
Every Context object comes with a Provider React component that allows consuming components to subscribe to context changes. The Provider component accepts a value prop to be passed to consuming components that are descendants of this Provider. One Provider can be connected to many consumers.
```js
<MyContext.Provider value={/* some value */}>
```

# Context.Consumer
A React component that subscribes to context changes. Using this component lets you subscribe to a context within a function component.
```js
<MyContext.Consumer>
  {value => /* render something based on the context value */}
</MyContext.Consumer>
```