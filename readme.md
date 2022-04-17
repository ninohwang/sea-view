## 相关记录

### `transform` 和 `animation` 的效果共存问题
这个小网页，一开始是 `sea-like` `sea-half-mask` `sun-like` 三个元素是并列同一层级的。但是之后发现 `sea-like` 上面想同时实现 360 度旋转的动画、和 `:hover` 会自动放大（利用 `transfrom` ）,但是发现两个效果不能放在同一个元素上。

似乎有说法 `transform` 和 `animation` 不能同时存在同一个元素上。（又多验证了几下，确实如此）

所以，把 sea-like 放置在了一个父元素下，并让它的父元素承担 :hover 点击被放大的效果。

### 元素渐变背景的颜色改变时如何实现平滑过渡效果
ref: https://www.zhangxinxu.com/wordpress/2018/03/background-gradient-transtion/

```js
globalThis.CSS.registerProperty({
    name: cssVarName,
    syntax: '--var-name',
    inherits: false,
    initialValue: 'transparent'
})
```
### 事件 mouseenter vs mouseover
