<p align="center">
  <img align="center" alt="react-darkreader" src="https://darkreader.org/images/darkreader-icon-256x256.png" />
</p>
<h1 align="center">useVuejs</h1>

<p align="center">🌓 A React Hook for adding a dark / night mode to your site inspired by <a href="https://github.com/darkreader/darkreader" target="_blank">darkreader</a>
</p>

<p align="center">
  <a href="https://www.npmjs.com/package/react-darkreader" target="_blank"><img alt="npm" src="https://img.shields.io/npm/v/react-darkreader?color=orange" /></a> <img alt="npm" src="https://img.shields.io/npm/dt/react-darkreader" /> <a href="https://github.com/umijs/dumi" target="_blank"><img alt="dumi" src="https://img.shields.io/badge/docs%20by-dumi-blue" /></a> <img alt="license" src="https://img.shields.io/github/license/Turkyden/react-darkreader" /> <a href="https://www.jsdelivr.com/package/npm/react-darkreader" target="_blank"><img alt="jsdelivr" src="https://data.jsdelivr.com/v1/package/npm/react-darkreader/badge" /></a>
</p>

<p align="center">Live Demo ✨ <a href="https://react-darkreader.vercel.app" target="_blank">https://react-darkreader.vercel.app</a></p>

A react hook similar to the vuejs API.

## Hello Vue

```jsx
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

```jsx
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

```jsx
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

```jsx
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

```jsx
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

```jsx
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
