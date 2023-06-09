## 如何为组件添加 CSS 的 class？

传递一个字符串作为 `className` 属性：

```React
render() {
  return <span className="menu navigation-menu">Menu</span>
}
```

CSS 的 class 依赖组件的 props 或 state 的情况很常见：

```React
render() {
  let className = 'menu';
  if (this.props.isActive) {
    className += ' menu-active';
  }
  return <span className={className}>Menu</span>
}
```

**提示**

如果你经常发现自己写类似这样的代码，[classnames](https://www.npmjs.com/package/classnames#usage-with-reactjs) 的 package 可以简化这一过程。

## 可以使用行内样式吗？

可以，在style查看关于样式的文档。

## 行内样式不好 (bad) 吗？

从性能角度来说，CSS 的 class 通常比行内样式更好。

## 什么是 CSS-in-JS?

“CSS-in-JS” 是指一种模式，其中 CSS 由 JavaScript 生成而不是在外部文件中定义。

_注意此功能并不是 React 的一部分，而是由第三方库提供。_ React 对样式如何定义并没有明确态度；如果存在疑惑，比较好的方式是和平时一样，在一个单独的 `*.css` 文件定义你的样式，并且通过className指定它们。

## 可以在 React 中实现动画效果吗?

React 可以被用来实现强大的动画效果。参见 [React Transition Group](https://reactcommunity.org/react-transition-group/)、[React Motion](https://github.com/chenglou/react-motion) 以及 [React Spring](https://github.com/react-spring/react-spring) 等示例。