**this**
new 绑定 > 显示绑定 > 隐式绑定 > 默认绑定
箭头函数的绑定无法被修改，其 this 指向其上一层作用域

null 本身是基本类型，typeof(null)结果为'object'的原因：不同的对象在底层都表示为二进制，在 JS 中二进制的前三位为 0 的话会被判定为'object'类型，而 null 的二进制全是 0。

**Object 对象方法**

> 'a' in myObject // myObject 对象及其原型链上是否有'a'属性
> myObject.hasOwnProperty('a') // myObject 对象本身是否有'a'属性
> Object.defineProperty([对象名],[属性名(String)],[属性描述(Object)]) // 为一个对象新增一个属性
> ps: writable // 是否可修改

      configurable // 是否可配置
      enumerable // 是否可枚举

> myObject.propertyIsEnumerable('a') // 属性'a'在 myObject 中是否可枚举
> Object.keys(myObject) // 返回一个数组，包含 myObject 本身的可枚举属性
> Object.values(myObject) // 返回一个数组，包含 myObject 本身的可枚举键值
> Object.entries(myObject) // 返回一个数组，包含 myObject 本身的可枚举键值对
> Object.getOwnPropertyNames(myObject) // 返回一个数组，包含 myObject 本身的所有属性

**for...of 遍历数组**
var arr = [1,2,3]
for (var v of arr){
console.log(v) // 1 2 3
}
for...of 循环首先会向被访问对象请求一个迭代器对象，然后通过调用迭代器对象的 next()方法来遍历所有返回值。
因为数组有内置的@@iterator，所以 for...of 可以直接用在数组上；
var arr = [1,2,3]
var it = arr[Symbol.iterator]()
console.log(it.next()) // { value:1, done:false }
console.log(it.next()) // { value:2, done:false }
console.log(it.next()) // { value:3, done:false }
console.log(it.next()) // { done:true }
