### Slider Props

| Name         | Type    | Description                                             | Default | Since |
| ------------ | ------- | ------------------------------------------------ | ------ | --- |
| value        | `number`  | 滑动输入条的值，可以使用 v-model 双向绑定        | `0`      | - |
| min          | `number`  | 滑动输入条的最小值                               | `0`      | - |
| max          | `number`  | 滑动输入条的最大值                               | `100`    | - |
| step         | `number`  | 滑动输入条每次值变化的跨度                       | `1`      | - |
| vertical     | `boolean` | 设置滑动输入条是否为纵向，需要父元素具有有效高度 | `false`  | - |
| hide-tip     | `boolean` | 设置是否禁用 tooltip                             | `false`  | - |
| tip-transfer | `boolean` | 设置 Tooltip 的 `transfer` 属性                    | `false`  | - |
| disable-validate | `boolean`                           | 是否禁用触发表单字段验证                                                         | ``false``                 | - |

### Slider Events

| Name      | Description                                                                      | Parameters  | Since |
| --------- | ------------------------------------------------------------------------- | ----- | --- |
| input  | 当滑动输入条在滑动引起值变化时触发，返回当前的值                          | `(value: number)` | - |
| change | 当滑动输入条的值改变时触发 (若使用滑动，则在滑动结束时触发)，返回当前的值 | `(value: number)` | - |