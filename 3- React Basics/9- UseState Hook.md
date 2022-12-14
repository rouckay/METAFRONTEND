# useState() Hook

![image](https://user-images.githubusercontent.com/25232528/196673014-56c7ac50-cdba-40ff-9059-c1200c60312a.png)

React library provides the useState function for functional components, which will return an array with two elements, where the first is the constant that stores that state and the second is a function to replace the value of that state.

***

The most common hook used to control some state variable inside a functional component in React. To use it we define:

```js
const [count, setCount] = useState(0);
```

The first ```count``` value represents the state value that will be manipulated by the ```setCount``` function received through the destructuring performed in ```useState```. The value ```0``` passed to the hook is the initial state value.

So, to manipulate the value of count we can simply run:

```js
<button onClick={() => setCount(count + 1)}>+</button>
```

**Code Example**

```index.js```

```js
import React from "react";
import ReactDOM from "react-dom";
import App from "./components/App";

ReactDOM.render(<App />, document.getElementById("root"));
```

App Component ```App.jsx```

```js
import React, { useState } from "react";

function App() {
  const [count, setCount] = useState(0);

  function increase() {
    setCount(count + 1);
  }

  function decrease() {
    setCount(count - 1);
  }

  function setToZero() {
    setCount(0);
  }

  return (
    <div className="container">
      <h1>{count}</h1>
      <button onClick={decrease}>-</button>
      <button onClick={setToZero}>0</button>
      <button onClick={increase}>+</button>
    </div>
  );
}

export default App;
```

Check result: https://eufnr0.csb.app/

***
