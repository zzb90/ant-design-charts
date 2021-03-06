---
title: 玫瑰图
order: 3
---

# 玫瑰图

## Rose

### 多色玫瑰图

<a href="https://antv-g2plot.gitee.io/zh/examples/rose/basic/API" target="_blank">配置</a>

```tsx
import React, { useState, useEffect } from 'react';
import { Rose } from '@ant-design/charts';

const DemoRose: React.FC = () => {
  const data = [
    {
      type: '分类一',
      value: 27,
    },
    {
      type: '分类二',
      value: 25,
    },
    {
      type: '分类三',
      value: 18,
    },
    {
      type: '分类四',
      value: 15,
    },
    {
      type: '分类五',
      value: 10,
    },
    {
      type: '其它',
      value: 5,
    },
  ];
  const config = {
    forceFit: true,
    title: {
      visible: true,
      text: '多色玫瑰图',
    },
    description: {
      visible: true,
      text:
        '指定颜色映射字段(colorField)\uFF0C饼图切片将根据该字段数据显示为不同的颜色\u3002指定颜色需要将color配置为一个数组\u3002\n当把饼图label的类型设置为inner时\uFF0C标签会显示在切片内部\u3002设置offset控制标签的偏移值\u3002',
    },
    radius: 0.8,
    data,
    radiusField: 'value',
    categoryField: 'type',
    colorField: 'type',
    label: {
      visible: true,
      type: 'outer',
      content: (text) => text.value,
    },
  };
  return <Rose {...config} />;
};

export default DemoRose;
```

### 分组玫瑰图

<a href="https://antv-g2plot.gitee.io/zh/examples/rose/basic/API" target="_blank">配置</a>

```tsx
import React, { useState, useEffect } from 'react';
import { Rose } from '@ant-design/charts';

const DemoRose: React.FC = () => {
  const data = [
    {
      type: '分类一',
      value: 27,
      user: '用户一',
    },
    {
      type: '分类二',
      value: 25,
      user: '用户一',
    },
    {
      type: '分类三',
      value: 18,
      user: '用户一',
    },
    {
      type: '分类四',
      value: 25,
      user: '用户一',
    },
    {
      type: '分类五',
      value: 10,
      user: '用户一',
    },
    {
      type: '其它',
      value: 12,
      user: '用户一',
    },
    {
      type: '分类一',
      value: 17,
      user: '用户二',
    },
    {
      type: '分类二',
      value: 35,
      user: '用户二',
    },
    {
      type: '分类三',
      value: 28,
      user: '用户二',
    },
    {
      type: '分类四',
      value: 35,
      user: '用户二',
    },
    {
      type: '分类五',
      value: 20,
      user: '用户二',
    },
    {
      type: '其它',
      value: 15,
      user: '用户二',
    },
  ];
  const config = {
    forceFit: true,
    title: {
      visible: true,
      text: '分组玫瑰图',
    },
    description: {
      visible: true,
      text:
        '指定颜色映射字段(colorField)\uFF0C饼图切片将根据该字段数据显示为不同的颜色\u3002指定颜色需要将color配置为一个数组\u3002\n当把饼图label的类型设置为inner时\uFF0C标签会显示在切片内部\u3002设置offset控制标签的偏移值\u3002',
    },
    radius: 0.7,
    data,
    radiusField: 'value',
    categoryField: 'type',
    groupField: 'user',
    label: {
      visible: true,
      type: 'inner',
    },
    theme: {
      legend: {
        margin: [0, 0, 80, 0],
      },
    },
  };
  return <Rose {...config} />;
};

export default DemoRose;
```

### 堆叠玫瑰图

<a href="https://antv-g2plot.gitee.io/zh/examples/rose/basic/API" target="_blank">配置</a>

```tsx
import React, { useState, useEffect } from 'react';
import { Rose } from '@ant-design/charts';

const DemoRose: React.FC = () => {
  const data = [
    {
      type: '分类一',
      value: 27,
      user: '用户一',
    },
    {
      type: '分类二',
      value: 25,
      user: '用户一',
    },
    {
      type: '分类三',
      value: 18,
      user: '用户一',
    },
    {
      type: '分类四',
      value: 15,
      user: '用户一',
    },
    {
      type: '分类五',
      value: 10,
      user: '用户一',
    },
    {
      type: '其它',
      value: 5,
      user: '用户一',
    },
    {
      type: '分类一',
      value: 7,
      user: '用户二',
    },
    {
      type: '分类二',
      value: 5,
      user: '用户二',
    },
    {
      type: '分类三',
      value: 38,
      user: '用户二',
    },
    {
      type: '分类四',
      value: 5,
      user: '用户二',
    },
    {
      type: '分类五',
      value: 20,
      user: '用户二',
    },
    {
      type: '其它',
      value: 15,
      user: '用户二',
    },
  ];
  const config = {
    forceFit: true,
    title: {
      visible: true,
      text: '堆叠玫瑰图',
    },
    description: {
      visible: true,
      text:
        '指定颜色映射字段(colorField)\uFF0C饼图切片将根据该字段数据显示为不同的颜色\u3002指定颜色需要将color配置为一个数组\u3002\n当把饼图label的类型设置为inner时\uFF0C标签会显示在切片内部\u3002设置offset控制标签的偏移值\u3002',
    },
    radius: 0.8,
    data,
    radiusField: 'value',
    categoryField: 'type',
    stackField: 'user',
    label: {
      visible: true,
      type: 'inner',
    },
  };
  return <Rose {...config} />;
};

export default DemoRose;
```
