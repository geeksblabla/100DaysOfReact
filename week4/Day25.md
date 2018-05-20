How we can implement the addCounting Function.
some Help Here https://www.youtube.com/watch?v=SQtrgiLy3Fo

Sandbox Example to start with : https://codesandbox.io/s/lpvnl97337

```jsx
import React from "react";
import { render } from "react-dom";
import {} from "recompose";

const addCounting = {};

const Counter = ({ counter, increment, decrement }) => (
  <div>
    <h1> {counter} </h1>
    <div>
      <button onClick={() => increment()}> Increment </button>
      <button onClick={() => decrement()}> Decrement </button>
    </div>
  </div>
);

const App = addCounting(Counter);

render(<App />, document.getElementById("root"));
```
