### Snippet 1

Which one is a valid JSX expression?

- One
```jsx
const Text = ({children}) => () => children

render(
    <Text>Hey</Text>
)
```

- Two
```jsx
const Text = ({children}) => () => children

render(
    <Text()>Hey</Text()>
)
```
