# vue-doc-example
vue非官方文档示例(全)

所有代码基于vue@2.6.10版本

每章节包括一个md说明文件以及一个html代码文件。原则是md文件尽可能的详细，并对官方文档进行补充；html文件尽可能的简单，最大化的将所有可能列出来,给予最直观的反馈。

基础部分，不使用v-on的缩写@，v-bind的缩写:，等到进阶部分所有代码都使用缩写。

能不写样式就不写样式，本文档重点想做的是语法，如果样式能帮助理解，我会加上一些的。

### 开始的开始
由于html标签不区分大小写，由于vue会在某些地方进行大小写转换，所以写代码的时候需要特别遵守下面的代码规范。
####  事件名使用 kebab-case 格式
事件名不存在任何自动化的大小写转换。而是触发的事件名需要完全匹配监听这个事件所用的名称。举个例子，如果触发一个 camelCase 名字的事件：
this.$emit('myEvent')
则监听这个名字的 kebab-case 版本是不会有任何效果的：
<my-component v-on:my-event="doSomething"></my-component>
不同于组件和 prop，事件名不会被用作一个 JavaScript 变量名或 property 名，所以就没有理由使用 camelCase 或 PascalCase 了。并且 v-on 事件监听器在 DOM 模板中会被自动转换为全小写 (因为 HTML 是大小写不敏感的)，所以 v-on:myEvent 将会变成 v-on:myevent——导致 myEvent 不可能被监听到。

#### props属性使用camelCase格式