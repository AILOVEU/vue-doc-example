# vue-doc-example
vue非官方文档示例(全)

所有代码基于vue@2.6.10版本

每章节包括一个md说明文件以及一个html代码文件。原则是md文件尽可能的详细，并对官方文档进行补充；html文件尽可能的简单，最大化的将所有可能列出来,给予最直观的反馈。

基础部分，不使用v-on的缩写@，v-bind的缩写:，等到进阶部分所有代码都使用缩写。

原则上尽量不写样式，本文档重点想做的是语法，如果样式能帮助理解，我会加上一些的。

### 开始的开始
由于html标签不区分大小写，由于vue会在某些地方进行大小写转换，所以写代码的时候需要特别遵守下面的代码规范。
####  1.事件名使用 kebab-case 格式
事件名不存在任何自动化的大小写转换。而是触发的事件名需要完全匹配监听这个事件所用的名称。举个例子，如果触发一个 camelCase 名字的事件：
this.$emit('myEvent')
则监听这个名字的 kebab-case 版本是不会有任何效果的：
<my-component v-on:my-event="doSomething"></my-component>
不同于组件和 prop，事件名不会被用作一个 JavaScript 变量名或 property 名，所以就没有理由使用 camelCase 或 PascalCase 了。并且 v-on 事件监听器在 DOM 模板中会被自动转换为全小写 (因为 HTML 是大小写不敏感的)，所以 v-on:myEvent 将会变成 v-on:myevent——导致 myEvent 不可能被监听到。

#### 2.props属性使用camelCase格式

#### 3.动态参数、动态插槽名，禁止使用驼峰和分割符

### 项目的使用方式
- 直接点击html，使用浏览器打开。推荐使用chrome浏览器或firefox以获取更好的用户体验
- 如果你想在编译器中直接操作，你可以全局安装[http-server](https://www.npmjs.com/package/http-server)，使用命令http-server ./ 把当前目录作为静态资源目录来访问

### 学习路线
- [vue](https://github.com/AILOVEU/vue-doc-example)
- [vue-cli](https://github.com/AILOVEU/vue-cli-doc-example)（计划中）
- [vue-router](https://github.com/AILOVEU/vue-router-doc-example)（暂时未公开）
- [vuex](https://github.com/AILOVEU/vuex-doc-example) （暂时未公开）
- [vue-ssr](https://github.com/AILOVEU/vue-ssr-doc-example)（计划中）

md文件会尽快补上

如果觉得该项目还不错，请喝杯奶茶吧

![](http://cdn.ailoveu.top/img/20200627223308.jpg)
![](http://cdn.ailoveu.top/img/20200627223307.jpg)



