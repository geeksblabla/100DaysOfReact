How would fix the bug in the code bellow?

```jsx
const Colorize = ({ children }) => {
  const colors = ['#9DC8C8', '#58C9B9', '#519D9E', '#D1B6E1'];

  return [...children].map(
    child => Object.assign(
        child,
        { props: { ...child.props, backgroundColor: Number.parseInt(Math.random() * colors.length) } }
    )
  )
}

render(
    <Colorize>
      <span>Hey</span>
      <span>Hello</span>
    </Colorize>
)
```
