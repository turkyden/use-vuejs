## Hello Vue!

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
      message: 'Hello Vue!',
    },
  });

  return <div id="app">{data.message}</div>;
};
```

More skills for writing demo: https://d.umijs.org/guide/demo-principle
