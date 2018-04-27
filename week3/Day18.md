what's the output value ? and  let's assume it will be 4 if not what's the problem and how can we solve it ?
```jsx

class Toto extends Component {
  constructor(props) {
    super(props);
    this.state = { count: 1 };
    this.setState({ count: this.state.count + 1 });
    this.setState({ count: this.state.count + 1 });
    this.setState({ count: this.state.count + 1 });
    
  }
  render() {
    return (<h2>{this.state.count}</h2>);
  }
}
```