let's say that we'd like to display a message if an error occured in ErrorBoundary, what is missing?

```jsx
class ErrorBoundary extends React.Component {
  constructor(props) {
    super(props);
    this.state = { hasError: false };
  }

  render() {
    if (this.state.hasError) {
      return <h1>Something went wrong.</h1>;
    }
    return this.props.children;
  }
}

render(
    <ErrorBoundary>
    ....
    </ErrorBoundary>
)
```