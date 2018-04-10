If the code below is correct what is the result in HTML?

```jsx
const a  = true & 0;
function then({children}){
    return ( <b> {children} </b>)
}
function otherwise({children}){
    return (<tt>{children}</tt>)
}

function App(){
  const Element =  a ? then : otherwise
  return ( <Element> Hello</Element>)
}

render(<App />, document.getElementById('root'));
```
