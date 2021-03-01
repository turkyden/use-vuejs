## Methods

You can use the state with `data`

```tsx
/**
 * defaultShowCode: true
 */
import React from 'react';
import useVuejs from 'use-vuejs';

export default () => {
  const { data, methods } = useVuejs({
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
      <p>{data.message}</p>
      <button onClick={methods.reverseMessage.bind(data)}>反转消息</button>
    </div>
  );
};
```

More skills for writing demo: https://d.umijs.org/guide/demo-principle
