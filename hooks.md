# Hooks
Hooks are a new addition in React 16.8. They let you use state and other React features without writing a class

 Hooks allow you to reuse stateful logic without changing your component hierarchy.

 # Rules
 ✅ Call Hooks from React function components.

✅ Call Hooks from custom Hooks .

# useState hook

The useState Hook can be used to keep track of strings, numbers, booleans, arrays, objects, and any combination of these! We could create multiple state Hooks to track individual values.

# What does calling useState do?
Each call to useState creates a single piece of state, holding a single value of any type. The useState hook is perfect for local component state, and a small-ish amount of it.

# what do we pass to useState as an argument?
The only argument to the useState() Hook is the initial state. Unlike with classes, the state doesn't have to be an object. We can keep a number or a string if that's all we need. In our example, we just want a number for how many times the user clicked, so pass 0 as initial state for our variable.


# What does useState return?
useState accepts an initial state and returns two values: The current state. A function that updates the state.
 
 