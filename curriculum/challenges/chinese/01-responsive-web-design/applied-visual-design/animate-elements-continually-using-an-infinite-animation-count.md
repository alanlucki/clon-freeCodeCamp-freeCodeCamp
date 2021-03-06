---
id: 587d78a8367417b2b2512ae3
title: 使用无限的动画计数制作永不停止的动画
challengeType: 0
videoUrl: 'https://scrimba.com/c/cVJDVfq'
forumTopicId: 301041
dashedName: animate-elements-continually-using-an-infinite-animation-count
---

# --description--

之前的关卡里介绍了一些动画属性以及 `@keyframes` 规则的用法。 还有一个常用的动画属性是 `animation-iteration-count`，这个属性允许你控制动画循环的次数。 下面是一个例子：

`animation-iteration-count: 3;`

在这种情况下，动画将在运行 3 次后停止，但可以通过设置该值为 `infinite` 来继续运行动画。

# --instructions--

把 `animation-iteration-count` 属性值改成 `infinite`，以使右边的球持续跳跃。

# --hints--

`animation-iteration-count` 属性应有一个值 `infinite`。

```js
assert($('#ball').css('animation-iteration-count') == 'infinite');
```

# --seed--

## --seed-contents--

```html
<style>

  #ball {
    width: 100px;
    height: 100px;
    margin: 50px auto;
    position: relative;
    border-radius: 50%;
    background: linear-gradient(
      35deg,
      #ccffff,
      #ffcccc
    );
    animation-name: bounce;
    animation-duration: 1s;
    animation-iteration-count: 3;
  }

  @keyframes bounce{
    0% {
      top: 0px;
    }
    50% {
      top: 249px;
      width: 130px;
      height: 70px;
    }
    100% {
      top: 0px;
    }
  }
</style>
<div id="ball"></div>
```

# --solutions--

```html
<style>
  #ball {
    width: 100px;
    height: 100px;
    margin: 50px auto;
    position: relative;
    border-radius: 50%;
    background: linear-gradient(
      35deg,
      #ccffff,
      #ffcccc
    );
    animation-name: bounce;
    animation-duration: 1s;
    animation-iteration-count: infinite;
  }

  @keyframes bounce{
    0% {
      top: 0px;
    }
    50% {
      top: 249px;
      width: 130px;
      height: 70px;
    }
    100% {
      top: 0px;
    }
  }
</style>
<div id="ball"></div>
```
