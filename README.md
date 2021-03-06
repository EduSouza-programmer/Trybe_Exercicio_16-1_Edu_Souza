<h1 align="center">
    <img alt="Image Trybe" src="https://i.ibb.co/d4W2x4g/trybe.png" width="400px" />
</h1>

<h3 align="center">
  Exercício 16-1: Intro ao Redux - O estado global da aplicação - Concluído o/ o/ o/ :star:
</h3>

<blockquote align="center">“Quanto mais você estuda, mais aprende e se aproxima de realizar seu sonhos!”</blockquote>

<h1></h1>

<p align="center">

  <a href="https://www.linkedin.com/in/eduardosouzaprogrammer/">
    <img alt="Made by Eduardo Souza" src="https://img.shields.io/badge/made%20by-Edu%20Souza-%23F8952D">
  </a>&nbsp;

 <a href="https://edusouza-programmer.github.io/">
<img alt="Github page Edu Souza " src="https://img.shields.io/badge/Github%20page-Edu_Souza-orange">
</a>&nbsp;

  <a href="LICENSE" >
    <img alt="License" src="https://img.shields.io/badge/license-MIT-%23F8952D">
  </a>

</p>

<p align="center">
  <a href="#rocket-Sobre-o-Exercício">Sobre o Exercício</a>&nbsp;&nbsp;|&nbsp;&nbsp;
  <a href="#postbox-Entrega">Entrega</a>&nbsp;&nbsp;|&nbsp;&nbsp;
  <a href="#unlock-Licença">Licença</a>
</p>

# :rocket: Sobre o Exercício

Hoje vamos aprender sobre uma biblioteca que possui ampla adoção entre as pessoas que desenvolvem em React . Essa biblioteca é o Redux . Ela é utilizada para ajudar no gerenciamento de estado. Vamos entender um pouco mais sobre o que é, como nasceu e como funciona o Redux.

# :postbox: Entrega

Você irá fazer 14 exercícios propostos pelo site freecodecamp , com objetivo de consolidar seus conhecimentos acerca dos conceitos presentes no Redux.

### :clipboard: Sumário

- <p><a href="#1"> :pushpin: 1.</a> Redux: Define an Action Creator;</p>

- <p><a href="#2"> :pushpin: 2.</a> Redux: Dispatch an Action Event;</p>

- <p><a href="#3"> :pushpin: 3.</a> Redux: Handle an Action in the Store;</p>

- <p><a href="#4"> :pushpin: 4.</a> Redux: Use a Switch Statement to Handle Multiple Actions;</p>

- <p><a href="#5"> :pushpin: 5.</a> Redux: Use const for Action Types;</p>

- <p><a href="#6"> :pushpin: 6.</a> Redux: Register a Store Listener;</p>

- <p><a href="#7"> :pushpin: 7.</a> Redux: Combine Multiple Reducers;</p>

- <p><a href="#8"> :pushpin: 8.</a> Redux: Send Action Data to the Store;</p>

- <p><a href="#9"> :pushpin: 9.</a> Redux: Write a Counter with Redux;</p>

- <p><a href="#10"> :pushpin: 10.</a> Redux: Never Mutate State;</p>

- <p><a href="#11"> :pushpin: 11.</a> Redux: Use the Spread Operator on Arrays;</p>

- <p><a href="#12"> :pushpin: 12.</a> Redux: Remove an Item from an Array;</p>

- <p><a href="#13"> :pushpin: 13.</a> Redux: Copy an Object with Object.assign;</p>

## :books: Exercícios

### 1°

[Redux: Define an Action Creator](https://www.freecodecamp.org/learn/front-end-libraries/redux/define-an-action-creator)

#### Resposta:

<details>
 <summary> :pencil2: Código Javascript</summary>

```js
const action = {
  type: "LOGIN",
};
// Define an action creator here:

const actionCreator = () => action;
```

</details>

<p align="right">
    <a href="#clipboard-Sumário">
    <img alt="Back Sumário" src="https://img.shields.io/badge/Back-Sum%C3%A1rio-orange">
  </a>
</p>

#

### 2°

[ Redux: Dispatch an Action Event](https://www.freecodecamp.org/learn/front-end-libraries/redux/dispatch-an-action-event)

#### Resposta:

<details>
 <summary> :pencil2: Código Javascript</summary>

```js
const store = Redux.createStore((state = { login: false }) => state);

const loginAction = () => {
  return {
    type: "LOGIN",
  };
};

// Dispatch the action here:
store.dispatch(loginAction());
```

</details>

<p align="right">
    <a href="#clipboard-Sumário">
    <img alt="Back Sumário" src="https://img.shields.io/badge/Back-Sum%C3%A1rio-orange">
  </a>
</p>

#

### 3°

[Redux: Handle an Action in the Store](https://www.freecodecamp.org/learn/front-end-libraries/redux/handle-an-action-in-the-store)

#### Resposta:

<details>
 <summary> :pencil2: Código Javascript</summary>

```js
const defaultState = {
  login: false,
};

const reducer = (state = defaultState, action) => {
  // Change code below this line
  return action.type === "LOGIN" ? { login: true } : state;

  // Change code above this line
};

const store = Redux.createStore(reducer);

const loginAction = () => {
  return {
    type: "LOGIN",
  };
};
```

</details>

<p align="right">
    <a href="#clipboard-Sumário">
    <img alt="Back Sumário" src="https://img.shields.io/badge/Back-Sum%C3%A1rio-orange">
  </a>
</p>

#

### 4°

[Redux: Use a Switch Statement to Handle Multiple Actions](https://www.freecodecamp.org/learn/front-end-libraries/redux/use-a-switch-statement-to-handle-multiple-actions)

#### Resposta:

<details>
 <summary> :pencil2: Código Javascript</summary>

```js
const defaultState = {
  authenticated: false,
};

const authReducer = (state = defaultState, action) => {
  // Change code below this line
  switch (action.type) {
    case "LOGIN":
      return {
        authenticated: true,
      };

    case "LOGOUT":
      return {
        authenticated: false,
      };

    default:
      return state;
  }
  // Change code above this line
};

const store = Redux.createStore(authReducer);

const loginUser = () => {
  return {
    type: "LOGIN",
  };
};

const logoutUser = () => {
  return {
    type: "LOGOUT",
  };
};
```

</details>

<p align="right">
    <a href="#clipboard-Sumário">
    <img alt="Back Sumário" src="https://img.shields.io/badge/Back-Sum%C3%A1rio-orange">
  </a>
</p>

#

### 5°

[Redux: Use const for Action Types](https://www.freecodecamp.org/learn/front-end-libraries/redux/use-const-for-action-types)

#### Resposta:

<details>
 <summary> :pencil2: Código Javascript</summary>

```js
// Change code below this line
const LOGIN = "LOGIN";
const LOGOUT = "LOGOUT";
// Change code above this line

const defaultState = {
  authenticated: false,
};

const authReducer = (state = defaultState, action) => {
  switch (action.type) {
    case "LOGIN":
      return {
        authenticated: true,
      };

    case "LOGOUT":
      return {
        authenticated: false,
      };

    default:
      return state;
  }
};

const store = Redux.createStore(authReducer);

const loginUser = () => {
  return {
    type: LOGIN,
  };
};

const logoutUser = () => {
  return {
    type: LOGOUT,
  };
};
```

</details>

<p align="right">
    <a href="#clipboard-Sumário">
    <img alt="Back Sumário" src="https://img.shields.io/badge/Back-Sum%C3%A1rio-orange">
  </a>
</p>

#

### 6°

[Redux: Register a Store Listener](https://www.freecodecamp.org/learn/front-end-libraries/redux/register-a-store-listener)

#### Resposta:

<details>
 <summary> :pencil2: Código Javascript</summary>

```js
const ADD = "ADD";

const reducer = (state = 0, action) => {
  switch (action.type) {
    case ADD:
      return state + 1;
    default:
      return state;
  }
};

const store = Redux.createStore(reducer);

// Global count variable:
let count = 0;

// Change code below this line
const addCount = () => (count += 1);
store.subscribe(addCount);
// Change code above this line

store.dispatch({ type: ADD });
console.log(count);
store.dispatch({ type: ADD });
console.log(count);
store.dispatch({ type: ADD });
console.log(count);
```

</details>

<p align="right">
    <a href="#clipboard-Sumário">
    <img alt="Back Sumário" src="https://img.shields.io/badge/Back-Sum%C3%A1rio-orange">
  </a>
</p>

#

### 7°

[Redux: Combine Multiple Reducers](https://www.freecodecamp.org/learn/front-end-libraries/redux/combine-multiple-reducers)

#### Resposta:

<details>
 <summary> :pencil2: Código Javascript</summary>

```js
const INCREMENT = "INCREMENT";
const DECREMENT = "DECREMENT";

const counterReducer = (state = 0, action) => {
  switch (action.type) {
    case INCREMENT:
      return state + 1;
    case DECREMENT:
      return state - 1;
    default:
      return state;
  }
};

const LOGIN = "LOGIN";
const LOGOUT = "LOGOUT";

const authReducer = (state = { authenticated: false }, action) => {
  switch (action.type) {
    case LOGIN:
      return {
        authenticated: true,
      };
    case LOGOUT:
      return {
        authenticated: false,
      };
    default:
      return state;
  }
};

const rootReducer = Redux.combineReducers({
  count: counterReducer,
  auth: authReducer,
});

const store = Redux.createStore(rootReducer);
```

</details>

<p align="right">
    <a href="#clipboard-Sumário">
    <img alt="Back Sumário" src="https://img.shields.io/badge/Back-Sum%C3%A1rio-orange">
  </a>
</p>

#

### 8°

[Redux: Send Action Data to the Store](https://www.freecodecamp.org/learn/front-end-libraries/redux/send-action-data-to-the-store)

#### Resposta:

<details>
 <summary> :pencil2: Código Javascript</summary>

```js
const ADD_NOTE = "ADD_NOTE";

const notesReducer = (state = "Initial State", action) => {
  switch (action.type) {
    // Change code below this line
    case "ADD_NOTE":
      return action.text;
    // Change code above this line
    default:
      return state;
  }
};

const addNoteText = (note) => {
  // Change code below this line
  return {
    type: ADD_NOTE,
    text: note,
  };
  // Change code above this line
};

const store = Redux.createStore(notesReducer);

console.log(store.getState());
store.dispatch(addNoteText("Hello!"));
console.log(store.getState());
```

</details>

<p align="right">
    <a href="#clipboard-Sumário">
    <img alt="Back Sumário" src="https://img.shields.io/badge/Back-Sum%C3%A1rio-orange">
  </a>
</p>

#

### 9°

[Redux: Write a Counter with Redux](https://www.freecodecamp.org/learn/front-end-libraries/redux/write-a-counter-with-redux)

#### Resposta:

<details>
 <summary> :pencil2: Código Javascript</summary>

```js
const INCREMENT = "INCREMENT"; // Define a constant for increment action types
const DECREMENT = "DECREMENT"; // Define a constant for decrement action types

const counterReducer = (state = 0, action) => {
  switch (action.type) {
    case INCREMENT:
      return state + 1;
    case DECREMENT:
      return state - 1;
    default:
      return state;
  }
};

const incAction = () => {
  return {
    type: INCREMENT,
  };
};

const decAction = () => {
  return {
    type: DECREMENT,
  };
};

const store = Redux.createStore(counterReducer);

console.log(store.getState());
store.dispatch(incAction());
console.log(store.getState());
```

</details>

<p align="right">
    <a href="#clipboard-Sumário">
    <img alt="Back Sumário" src="https://img.shields.io/badge/Back-Sum%C3%A1rio-orange">
  </a>
</p>

#

### 10°

[Redux: Never Mutate State](https://www.freecodecamp.org/learn/front-end-libraries/redux/never-mutate-state)

#### Resposta:

<details>
 <summary> :pencil2: Código Javascript</summary>

```js
const ADD_TO_DO = "ADD_TO_DO";

// A list of strings representing tasks to do:
const todos = ["Go to the store", "Clean the house", "Cook dinner", "Learn to code"];

const immutableReducer = (state = todos, action) => {
  switch (action.type) {
    case ADD_TO_DO:
      return [...state, action.todo];
    default:
      return state;
  }
};

const addToDo = (todo) => {
  return {
    type: ADD_TO_DO,
    todo,
  };
};

const store = Redux.createStore(immutableReducer);

console.log(store.getState());
store.dispatch(addToDo("Amo minha família"));
console.log(store.getState());
```

</details>

<p align="right">
    <a href="#clipboard-Sumário">
    <img alt="Back Sumário" src="https://img.shields.io/badge/Back-Sum%C3%A1rio-orange">
  </a>
</p>

#

### 11°

[Redux: Use the Spread Operator on Arrays](https://www.freecodecamp.org/learn/front-end-libraries/redux/use-the-spread-operator-on-arrays)

#### Resposta:

<details>
 <summary> :pencil2: Código Javascript</summary>

```js
const immutableReducer = (state = ["Do not mutate state!"], action) => {
  switch (action.type) {
    case "ADD_TO_DO":
      return [...state, action.todo];
      return;
    default:
      return state;
  }
};

const addToDo = (todo) => {
  return {
    type: "ADD_TO_DO",
    todo,
  };
};

const store = Redux.createStore(immutableReducer);
```

</details>

<p align="right">
    <a href="#clipboard-Sumário">
    <img alt="Back Sumário" src="https://img.shields.io/badge/Back-Sum%C3%A1rio-orange">
  </a>
</p>

#

### 12°

[Redux: Remove an Item from an Array](https://www.freecodecamp.org/learn/front-end-libraries/redux/remove-an-item-from-an-array)

#### Resposta:

<details>
 <summary> :pencil2: Código Javascript</summary>

```js
const immutableReducer = (state = [0, 1, 2, 3, 4, 5], action) => {
  switch (action.type) {
    case "REMOVE_ITEM":
      return state.filter((_, i) => i !== action.index);
    default:
      return state;
  }
};

const removeItem = (index) => {
  return {
    type: "REMOVE_ITEM",
    index,
  };
};

const store = Redux.createStore(immutableReducer);
```

</details>

<p align="right">
    <a href="#clipboard-Sumário">
    <img alt="Back Sumário" src="https://img.shields.io/badge/Back-Sum%C3%A1rio-orange">
  </a>
</p>

#

### 13°

[Redux: Copy an Object with Object.assign](https://www.freecodecamp.org/learn/front-end-libraries/redux/copy-an-object-with-object-assign)

#### Resposta:

<details>
 <summary> :pencil2: Código Javascript</summary>

```js
const defaultState = {
  user: "CamperBot",
  status: "offline",
  friends: "732,982",
  community: "freeCodeCamp",
};

const immutableReducer = (state = defaultState, action) => {
  switch (action.type) {
    case "ONLINE":
      return Object.assign({}, state, { status: "online" });

    // podemos usar assim também
    // {...state, status:'online' }

    default:
      return state;
  }
};

const wakeUp = () => {
  return {
    type: "ONLINE",
  };
};

const store = Redux.createStore(immutableReducer);
```

</details>

<p align="right">
    <a href="#clipboard-Sumário">
    <img alt="Back Sumário" src="https://img.shields.io/badge/Back-Sum%C3%A1rio-orange">
  </a>
</p>

#

## :unlock: Licença

Este projeto está licenciado sob a Licença MIT - consulte [LICENSE](https://opensource.org/licenses/MIT) para maiores detalhes.
