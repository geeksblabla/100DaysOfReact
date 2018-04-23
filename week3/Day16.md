Considering the code below what's the output?

```jsx

function* countToTen() {
    for (var i = 0; i < 10; i++) {
        yield i;
    }
}

const App = () => {
    const counter = countToTen();
    const els = pull(counter).map(
        el => <Text>{el}</Text>
    );

    function pull(c) {
        const v = c.next().value;
        if(v !== undefined) {
            return [v].concat(pull(c));
        } else {
            return [];
        }
    }

    return els;
}

render(
    <App />
)
```