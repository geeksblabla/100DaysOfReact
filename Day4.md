What's the result of this code ? 01 or 421 ? 

```jsx
function App(){
  return (
    Object.assign([0,1] ,{0:42},{0:0})
    .map((element,i)=> (<b key={i}>{element}</b>))
  );

}
render(<App />, document.getElementById('root'));

```
