## v-if

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
      seen: true,
    },
  });

  return <div id="app-3">{data.seen && <p>现在你看到我了</p>}</div>;
};
```

More skills for writing demo: https://d.umijs.org/guide/demo-principle
