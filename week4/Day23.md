Consider the  component below, How we can implement the Card Component.

Go Go https://codesandbox.io/s/m57xjr46vy

```jsx
import React from "react";
import { render } from "react-dom";
import Card from "./Card";

const App = () => (
  <Card>
    <Card.Header title="Card Header" />
    <Card.Content> your card content here </Card.Content>
    <div>
      <Card.Footer> Card Header </Card.Footer>
    </div>
  </Card>
);

render(<App />, document.getElementById("root"));
```
