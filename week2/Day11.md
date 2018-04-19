without running this code, whar does it do?

```jsx
const store = {
  elements: [
    {
      name: 'My Awseome list',
      elements: [
        { name: 'Element 1' },
        { name: 'Element 2' },
        { name: 'Element 3' },
        {
          name: 'Element 4',
          elements: [
            {
              elements: [
                { name: 'Element 4.1' },
                { name: 'Element 4.2' },
                { name: 'Element 4.3' },
                { name: 'Element 4.4' },
              ]
            }
          ]
        },
      ]
    }
  ]
};

function SuperList({ name, elements }) {
  if(elements) {
    const subElements = elements.map(
      el => <SuperList {...el} />
    );
    return (
      <React.Fragment>
        <ul>
          <lh>{name}</lh>
          {subElements}
        </ul>
      </React.Fragment>
    )
  } else {
    return (
      <li>{name}</li>
    )
  }
}

render(
    <SuperList {...store} />
)
```
