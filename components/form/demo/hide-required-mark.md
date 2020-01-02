---
order: 3
title:
  zh-CN: 隐藏必选标记
  en-US: Hide Required Mark
---

## zh-CN

隐藏必选标记，展示（可选）

## en-US

There is hideRequiredMark for form: `true`, `false`, `{ optionalMark: true }`.

```tsx
import React, { useState } from 'react';
import { Form, Input, Button } from 'antd';

const HideRequiredMarkDemo = () => {
  const [hideRequiredMark, setHideRequiredMark] = useState({ optionalMark: true });
  return (
    <Form layout="vertical" hideRequiredMark={hideRequiredMark}>
      <Form.Item label="Field A" rules={[{ required: true }]}>
        <Input placeholder="input placeholder" />
      </Form.Item>
      <Form.Item label="Field B">
        <Input placeholder="input placeholder" />
      </Form.Item>
      <Form.Item>
        <Button
          type="primary"
          onClick={() => {
            setHideRequiredMark(true);
          }}
        >
          Hide *
        </Button>
        <Button
          type="primary"
          onClick={() => {
            setHideRequiredMark(false);
          }}
        >
          Show *
        </Button>
        <Button
          type="primary"
          onClick={() => {
            setHideRequiredMark({ optionalMark: true });
          }}
        >
          Hide * and show optional text
        </Button>
      </Form.Item>
    </Form>
  );
};

ReactDOM.render(<HideRequiredMarkDemo />, mountNode);
```

```css
#components-form-demo-hide-required-mark .ant-btn {
  margin-right: 8px;
}
```