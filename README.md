# wepy-com-loading

一个阻塞页面的加载动画组件。

此组件依赖 [wepy](https://github.com/Tencent/wepy) 1.7.0+。

如果你正在使用 wepy 2.x，请移步 [wepy2-com-loading](https://github.com/fudiwei/wepy2-com-loading)。

---

## 用法

安装：

``` shell
npm install @skit/wepy-com-loading --save
```

导入：

``` html
<template>
    <ui-loading />
</template>
<script>
    import Wepy from 'wepy';
    import UILoading from '@skit/wepy-com-loading';

    export default class DemoPage extends Wepy.page {
        components = {
            'ui-loading': UILoading
        };
    }
</script>
```

### 可配置项

#### 属性：

*无*

#### 方法：

``` javascript
/**
 * 显示加载对话框。
 * @param {Object} options 配置项。
 * @param {String} options.content 提示文本。
 */
this.$invoke('ui-loading', 'show', {
    content: '加载中'
});

/**
 * 显示加载对话框。
 * @param {String} content 提示文本。
 */
this.$invoke('ui-loading', 'show', '加载中');

/**
 * 隐藏加载对话框。
 */
this.$invoke('ui-loading', 'hide');
```