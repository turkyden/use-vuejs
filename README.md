<p align="center">
  <img align="center" alt="use-vuejs" width="256px" src="https://camo.githubusercontent.com/5ebc638bb3e5113c5a87a5462197c35f40f7185ea9940e7723846b6e403f8a6b/68747470733a2f2f6372656174652d72656163742d6170702e6465762f696d672f6c6f676f2e737667" />
</p>
<h1 align="center">useVuejs</h1>

<p align="center">🥑 A React Hook similar to the <a href="https://github.com/darkreader/darkreader" target="_blank">Vuejs</a> API. 
</p>

<p align="center">
  <a href="https://www.npmjs.com/package/use-vuejs" target="_blank"><img alt="npm" src="https://img.shields.io/npm/v/use-vuejs?color=orange" /></a> <img alt="npm" src="https://img.shields.io/npm/dt/use-vuejs" /> <a href="https://github.com/umijs/dumi" target="_blank"><img alt="dumi" src="https://img.shields.io/badge/docs%20by-dumi-blue" /></a> <img alt="license" src="https://img.shields.io/github/license/Turkyden/use-vuejs" /> <a href="https://www.jsdelivr.com/package/npm/use-vuejs" target="_blank"><img alt="jsdelivr" src="https://data.jsdelivr.com/v1/package/npm/use-vuejs/badge" /></a>
</p>

<p align="center">Live Demo ✨ <a href="https://use-vuejs.vercel.app" target="_blank">https://use-vuejs.vercel.app</a></p>

## Hello Vue

```jsx | pure
function App() {
  const { message } = useVuejs({
    data: {
      message: 'Hello Vue!',
    },
  });

  return <div id="app">{message}</div>;
}

ReactDOM.render(<App />, document.querySelector('#app'));
```

## `v-bind`

```jsx | pure
function App2() {
  const { message } = useVuejs({
    data: {
      message: '页面加载于 ' + new Date().toLocaleString(),
    },
  });

  return (
    <div id="app-2">
      <span title={message}>鼠标悬停几秒钟查看此处动态绑定的提示信息！</span>
    </div>
  );
}

ReactDOM.render(<App2 />, document.querySelector('#app-2'));
```

## `v-if`

```jsx | pure
function App3() {
  const { seen } = useVuejs({
    data: {
      seen: true,
    },
  });

  return <div id="app-3">{seen && <p>现在你看到我了</p>}</div>;
}

ReactDOM.render(<App3 />, document.querySelector('#app-3'));
```

## `v-for`

```jsx | pure
function App4() {
  const { todos } = useVuejs({
    data: {
      todos: [
        { text: '学习 JavaScript' },
        { text: '学习 Vue' },
        { text: '整个牛项目' },
      ],
    },
  });

  return (
    <div id="app-4">
      <ol>
        {todos.map(todo => (
          <li>{todo.text}</li>
        ))}
      </ol>
    </div>
  );
}

ReactDOM.render(<App4 />, document.querySelector('#app-4'));
```

## Methods

```jsx | pure
function App5() {
  const { message, reverseMessage } = useVuejs({
    data: {
      message: 'Hello Vue.js!',
    },
    methods: {
      reverseMessage: function() {
        this.message = this.message
          .split('')
          .reverse()
          .join('');
      },
    },
  });

  return (
    <div id="app-5">
      <p>{message}</p>
      <button onClick={reverseMessage}>反转消息</button>
    </div>
  );
}

ReactDOM.render(<App5 />, document.querySelector('#app-5'));
```

## `v-model`

```jsx | pure
function App6() {
  const { message, vModel } = useVuejs({
    data: {
      message: 'Hello Vue!',
    },
  });

  return (
    <div id="app-6">
      <p>{{ message }}</p>
      <input onChange={vModel(message)} />
    </div>
  );
}

ReactDOM.render(<App6 />, document.querySelector('#app-6'));
```

## Contribute

Install dependencies,

```bash
$ npm i
```

Start the dev server,

```bash
$ npm start
```

Build documentation,

```bash
$ npm run docs:build
```

Build library via `father-build`,

```bash
$ npm run build
```
