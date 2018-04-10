Is the code below  correct ? if yes complete the render method to 
show profile view with title DevCasa

```jsx
const Views = {
    home({title}){
        return (<div>{title}</div>)
    },
    profile({title}){
      return (<h2>{title}</h2>)
    }
}
function App({page='home'}){
  const View = Views[page]
  return ( <View {...arguments[0]} />)
}

render(<App ....., document.getElementById('root'));

```
