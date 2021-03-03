## v-model

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

  const vModel = e => (data.message = e.target.value);

  return (
    <div id="app-6">
      <p>{data.message}</p>
      <input {...v_model(message)} />
      {/** <input v-model="message" /> **/}
    </div>
  );
};
```

More skills for writing demo: https://d.umijs.org/guide/demo-principle
