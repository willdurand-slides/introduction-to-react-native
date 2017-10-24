## What is React?

<img src="/assets/images/react.svg" style="height: 200px">


## Presentation

- JavaScript library for building User Interfaces (UIs)
- Facebook Open Source
- **Learn Once, Write Anywhere**

<br>
Documentation: https://facebook.github.io/react/


### React 101

- Abstract UI tree with components
- Virtual DOM with diff algorithm
- Data flow is **unidirectional**


### React in Action

``` javascript.player.web
import React from 'react';
import ReactDOM from 'react-dom';

const Counter = ({ value }) => (
  <p>State value is: {value}</p>
);

class App extends React.Component {
  constructor(props) {
    super(props);

    this.state = { value: 42 };
  }

  handleOnClick = () => {
    this.setState(prevState => ({ value: prevState.value + 1 }));
  }

  render() {
    return (
      <div style={{ margin: '1em' }}>
        <Counter value={this.state.value} />

        <button onClick={this.handleOnClick}>increment</button>
      </div>
    );
  }
}

ReactDOM.render(<App />, document.querySelector('#app'));
```


## What else?

- Data management with [Redux](http://redux.js.org/)
- Static type checker: [Flow](https://flow.org/) (also check out
  [TypeScript](https://www.typescriptlang.org/))
- [Hundreds of third-party
  components](https://github.com/brillout/awesome-react-components)
- Testing tools: [Jest](https://facebook.github.io/jest/),
  [Enzyme](http://airbnb.io/enzyme/)
- Live/Hot Reload, DevTools ❤️
- The rest of the JavaScript ecosystem
