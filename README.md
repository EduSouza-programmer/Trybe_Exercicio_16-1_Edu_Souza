<h1 align="center">
    <img alt="Image Trybe" src="https://i.ibb.co/d4W2x4g/trybe.png" width="400px" />
</h1>

<h3 align="center">
  Exercício 16-1: JS_ES6 - Intro ao Redux : O estado global da aplicação - Concluído o/ o/ o/ :star:
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
Você irá fazer 14 exercícios propostos pelo site freecodecamp , com objetivo de consolidar seus conhecimentos acerca dos conceitos presentes no Redux.

# :postbox: Entrega

### :clipboard: Sumário

- <p><a href="#1"> :pushpin: 1.</a> Redux: Define an Action Creator;</p>

- <p><a href="#2"> :pushpin: 2.</a> Redux: Dispatch an Action Event;</p>

- <p><a href="#3"> :pushpin: 3.</a> Redux: Handle an Action in the Store;</p>

- <p><a href="#4"> :pushpin: 4.</a> Redux: Use a Switch Statement to Handle Multiple Actions;</p>

- <p><a href="#5"> :pushpin: 5.</a> Redux: Use const for Action Types;</p>

- <p><a href="#6"> :pushpin: 6.</a> Redux: Register a Store Listener;</p>

- <p><a href="#7"> :pushpin: 7.</a> ;</p>

- <p><a href="#8"> :pushpin: 8.</a> ;</p>

- <p><a href="#9"> :pushpin: 9.</a> ;</p>

- <p><a href="#10"> :pushpin: 10.</a> ;</p>

- <p><a href="#11"> :pushpin: 11.</a> ;</p>

- <p><a href="#12"> :pushpin: 12.</a> ;</p>

- <p><a href="#13"> :pushpin: 13.</a> ;</p>

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

[]()

#### Resposta:

<details>
 <summary> :pencil2: Código Javascript</summary>

```js

```

</details>

<p align="right">
    <a href="#clipboard-Sumário">
    <img alt="Back Sumário" src="https://img.shields.io/badge/Back-Sum%C3%A1rio-orange">
  </a>
</p>

#

### 8°

[]()

#### Resposta:

<details>
 <summary> :pencil2: Código Javascript</summary>

```js

```

</details>

<p align="right">
    <a href="#clipboard-Sumário">
    <img alt="Back Sumário" src="https://img.shields.io/badge/Back-Sum%C3%A1rio-orange">
  </a>
</p>

#

### 9°

[]()

#### Resposta:

<details>
 <summary> :pencil2: Código Javascript</summary>

```js

```

</details>

<p align="right">
    <a href="#clipboard-Sumário">
    <img alt="Back Sumário" src="https://img.shields.io/badge/Back-Sum%C3%A1rio-orange">
  </a>
</p>

#

### 10°

[]()

#### Resposta:

<details>
 <summary> :pencil2: Código Javascript</summary>

```js

```

</details>

<p align="right">
    <a href="#clipboard-Sumário">
    <img alt="Back Sumário" src="https://img.shields.io/badge/Back-Sum%C3%A1rio-orange">
  </a>
</p>

#

### 11°

[]()

#### Resposta:

<details>
 <summary> :pencil2: Código Javascript</summary>

```js

```

</details>

<p align="right">
    <a href="#clipboard-Sumário">
    <img alt="Back Sumário" src="https://img.shields.io/badge/Back-Sum%C3%A1rio-orange">
  </a>
</p>

#

### 12°

[]()

#### Resposta:

<details>
 <summary> :pencil2: Código Javascript</summary>

```js

```

</details>

<p align="right">
    <a href="#clipboard-Sumário">
    <img alt="Back Sumário" src="https://img.shields.io/badge/Back-Sum%C3%A1rio-orange">
  </a>
</p>

#

### 13°

[]()

#### Resposta:

<details>
 <summary> :pencil2: Código Javascript</summary>

```js

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
