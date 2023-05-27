# 时间线 Timeline

常用于循序渐进的展示一些内容。

## 代码示例

:::demo timeline/basis

### 基础用法

追溯过往，展望未来。

:::

:::demo timeline/pending

### 进行中

加 `pending` 属性可以使最后一个节点显示为进行中。

:::

:::demo timeline/flip

### 内容翻转

添加 `flip` 属性可以快速将节点内容放置在另一侧。

:::

:::demo timeline/sides

### 双边模式

有一个需求用到这样子的设计，于是它就诞生了。

:::

:::demo timeline/horizontal

### 横向

添加 `horizontal` 属性可以使时间线变为横向的。

在双边模式下，如果你不希望组件自动计算高度，那么你可以自己给一个行内样式高度。

:::

## API

### Timeline 属性

| 名称       | 类型               | 说明                                                          | 默认值  | 始于     |
| ---------- | ------------------ | ------------------------------------------------------------- | ------- | -------- |
| pending    | `boolean`          | 设置时间线是否为未完成状态                                    | `false` | -        |
| both-sides | `boolean`          | 设置是否开启两侧模式                                          | `false` | -        |
| dashed     | `boolean`          | 设置时间线是否为虚线                                          | `false` | -        |
| lineColor  | `string`           | 设置时间线的颜色                                              | `null`  | -        |
| spacing    | `number \| string` | 设置时间节点间的间隔距离，可以传入一个数字或合法的 css 长度值 | `null`  | -        |
| flip       | `boolean`          | 设置是否翻转内容                                              | `false` | `2.0.18` |
| horizontal | `boolean`          | 设置时间线是否为横向                                          | `false` | `2.0.18` |

### Timeline 事件

| 名称         | 说明                                               | 参数                        | 始于 |
| ------------ | -------------------------------------------------- | --------------------------- | ---- |
| signal-click | 当时间线节点被点击时触发，返回被点击节点的 `label` | `(label: string \| number)` | -    |

### TimelineItem 属性

| 名称      | 类型                                                           | 说明                                                          | 默认值      | 始于 |
| --------- | -------------------------------------------------------------- | ------------------------------------------------------------- | ----------- | ---- |
| type      | `'default' \| 'success' \| 'error' \| 'warning' \| 'disabled'` | 时间节点的类型                                                | `'default'` | -    |
| color     | `string`                                                       | 可以指定节点的自定义颜色                                      | `''`        | -    |
| label     | `number \| string`                                             | 设置节点的 `label`，在监听节点点击事件时有用                  | `null`      | -    |
| dashed    | `boolean`                                                      | 设置时间节点的线是否为虚线                                    | `false`     | -    |
| lineColor | `string`                                                       | 设置时间节点的线的颜色                                        | `null`      | -    |
| spacing   | `number \| string`                                             | 设置时间节点间的间隔距离，可以传入一个数字或合法的 css 长度值 | `null`      | -    |

### TimelineItem 事件

| 名称         | 说明                                       | 参数                        | 始于 |
| ------------ | ------------------------------------------ | --------------------------- | ---- |
| signal-click | 当时间线节点被点击时触发，返回当前 `label` | `(label: string \| number)` | -    |