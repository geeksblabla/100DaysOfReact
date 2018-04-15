Does this code work? if not, how to fix it

```jsx
class MyComponent extends React.PureComponent {
  constructor(props){
    super(props);
    this.state = {
      arr: [1,2,3,4]
    }
  }
  addElement() {
    this.setState(
      state => {
        state.arr.push(state.arr.length);
        return state;
      }
    )
  }
  render() {
    return (
      <React.Fragment>
        <div>length is {this.state.arr.length}</div>
        <button onClick={() => this.addElement()} >
          Another one
        </button>
      </React.Fragment>
    );
  }
}
```