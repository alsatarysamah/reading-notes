# Context
### What can React Context provide your app?
 React context allows us to pass down and use (consume) data in whatever component we need in our React app without using props.

###  Why might we use Context?
 Context is primarily used when some data needs to be accessible by many components at different nesting levels

```js

const ThemeContext = React.createContext('light');

class App extends React.Component {
  render() {

    return (
      <ThemeContext.Provider value="dark">
        <Toolbar />
      </ThemeContext.Provider>
    );
  }
}

function Toolbar() {
  return (
    <div>
      <ThemedButton />
    </div>
  );
}

class ThemedButton extends React.Component {
 
  static contextType = ThemeContext;
  render() {
    return <Button theme={this.context} />;
  }
}
```
