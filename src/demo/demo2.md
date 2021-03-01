## v-bind

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
      getMessage: function() {
        return '页面加载于 ' + new Date().toLocaleString();
      },
    },
  });

  return (
    <div id="app-2">
      <span title={data.getMessage()}>
        鼠标悬停几秒钟查看此处动态绑定的提示信息！
      </span>
    </div>
  );
};
```

More skills for writing demo: https://d.umijs.org/guide/demo-principle
