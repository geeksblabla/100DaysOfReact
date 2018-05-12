what is the best way to render children DOM node that exists outside the DOM hierarchy of the parent component?

```jsx
    $(domNode).append(
        ReactDOM.findDOMNode(this.ref)
    )
```

```jsx
    return ReactDOM.createPortal(
        this.ref,
        domNode
    )
```