## v-for

You can use the state with `data`

```tsx
/**
 * defaultShowCode: true
 */
import React from 'react';
import useVuejs from 'use-vuejs';

export default () => {
  const { data } = useVuejs({
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
        {data.todos.map(todo => (
          <li>{todo.text}</li>
        ))}
      </ol>
    </div>
  );
};
```

More skills for writing demo: https://d.umijs.org/guide/demo-principle
