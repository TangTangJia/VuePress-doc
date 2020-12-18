# 基础组件
[[toc]]

## 按钮
<br/>
<template>
  <a-button type="primary">Primary</a-button>
  <a-button type="danger">Danger</a-button>
  <a-config-provider :auto-insert-space-in-button="false">
    <a-button type="primary">按钮</a-button>
  </a-config-provider>
</template>

::: details 查看代码
```html
<template>
	<a-button type="primary">Primary</a-button>
	<a-button type="danger">Danger</a-button>
	<a-config-provider :auto-insert-space-in-button="false">
		<a-button type="primary">按钮</a-button>
	</a-config-provider>
</template>
```
:::

### API
| 属性        | 说明           | 类型  | 默认值    |
|------------- |-------------| -----| ------- |
| shape     | 设置按钮形状 | circle 、round |     -    |
| ghost      | 幽灵属性，使按钮背景透明      |   boolean |     false    |
| onClick | 点击按钮时的回调     |    (event) => void |     -    |

## Switch 开关
<br/>
<a-switch default-checked  />

::: details 查看代码
```html
<template>
  <div>
    <a-switch default-checked @change="onChange"/>
  </div>
</template>
```
``` js
export default {
  data() {
    return {};
  },
  methods: {
    onChange(checked) {
      console.log(`a-switch to ${checked}`);
    }
  }
};
```
:::

## DatePicker 日期选择框
<br/>
<template>
  <div>
      <div>
        <a-date-picker />
      </div>
    <br/>
      <div>
        <a-range-picker />
      </div>
    <br/>
    <a-week-picker placeholder="Select week" />
  </div>
</template>

::: details 查看代码
``` html
<template>
  <div>
    <a-date-picker @change="onChange" />
    <br />
    <a-range-picker @change="onChange" />
    <br />
    <a-week-picker placeholder="Select week" @change="onChange" />
  </div>
</template>
```
``` js
export default {
  methods: {
    onChange(date, dateString) {
      console.log(date, dateString);
    },
  }
```
:::
