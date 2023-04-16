#### Vue Scoped原理

当style标签加上scoped属性时，scoped会在DOM结构以及css样式上加上唯一性的标识**data-v-xxx**属性，从而达到样式私有化，不污染全局的作用。

#### ref是什么

- 获取DOM引用
- ref和v-for使用在同一标签上时，ref获取到的是DOM引用数组

