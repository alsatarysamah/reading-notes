# Use Effect
## What does useEffect do?

 By using this Hook, you tell React that your component needs to do something after render. 

## Why is useEffect called inside a component?

 Placing useEffect inside the component lets us access the  state variable (or any props) right from the effect. 

## Does useEffect run after every render?

 Yes! By default, it runs both after the first render and after every update. 

 example:

 ```js
 function Example() {
  const [count, setCount] = useState(0);

  useEffect(() => {
    document.title = `You clicked ${count} times`;
  });
}
```
