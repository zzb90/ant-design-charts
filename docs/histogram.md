---
title: Histogram
---

# Histogram Component

## Normal

```tsx
import React from 'react';
import { Histogram } from '@alipay/techui-charts';

const data = [
  { value: 1.2 },
  { value: 3.4 },
  { value: 3.7 },
  { value: 4.3 },
  { value: 5.2 },
  { value: 5.8 },
  { value: 6.1 },
  { value: 6.5 },
  { value: 6.8 },
  { value: 7.1 },
  { value: 7.3 },
  { value: 7.7 },
  { value: 8.3 },
  { value: 8.6 },
  { value: 8.8 },
  { value: 9.1 },
  { value: 9.2 },
  { value: 9.4 },
  { value: 9.5 },
  { value: 9.7 },
  { value: 10.5 },
  { value: 10.7 },
  { value: 10.8 },
  { value: 11.0 },
  { value: 11.0 },
  { value: 11.1 },
  { value: 11.2 },
  { value: 11.3 },
  { value: 11.4 },
  { value: 11.4 },
  { value: 11.7 },
  { value: 12.0 },
  { value: 12.9 },
  { value: 12.9 },
  { value: 13.3 },
  { value: 13.7 },
  { value: 13.8 },
  { value: 13.9 },
  { value: 14.0 },
  { value: 14.2 },
  { value: 14.5 },
  { value: 15 },
  { value: 15.2 },
  { value: 15.6 },
  { value: 16.0 },
  { value: 16.3 },
  { value: 17.3 },
  { value: 17.5 },
  { value: 17.9 },
  { value: 18.0 },
  { value: 18.0 },
  { value: 20.6 },
  { value: 21 },
  { value: 23.4 },
];
const config = {
  title: {
    visible: true,
    text: '直方图',
  },
  description: {
    visible: true,
    text: '通过设置binNumber进行分箱，binNumber决定直方图分箱的区域。',
  },
  forceFit: true,
  data,
  padding: 'auto',
  data,
  binField: 'value',
  binNumber: 6,
  onInit: chart => {
    console.log('canvas instance', chart);
  },
};
export default () => <Histogram {...config} />;
```