闭包：一个函数在定义它的词法作用域之外执行，并保持对原有作用域的引用，这个引用就叫闭包。

**this**绑定：new绑定 > 显示绑定 > 隐式绑定 > 默认绑定

**---JS数组处理函数---**

*splice*：
    （1）删除功能：arr.splice(index,num)，index为起始位置，num为删除个数
    （2）插入功能：arr.splice(index,0,insertVal)，index为插入位置，insertVal为插入项
    （3）替换功能：arr.splice(index,num,insertVal)，index为起始位置，num为删除个数，insertVal为插入项

*slice*:通过索引位置获取新数组，不会改变原数组，返回一个新的数组。
    `arr.slice(start,end)`
    arr:原数组
    start:必填；新数组的起始位置；若为负数则倒数
    end:选填；新数组的结束位置；若不填则默认到结尾；若为负数则倒数

*join*:把数组中的元素合并为一个字符串
    `arr.join(sep)`
    sep:分隔符；字符串；不传或传入undefined则默认以逗号分隔

*concat*:用与连接两个或多个数组，返回一个新的数组
    `arr.concat(arr...)`

*增删*:arr.push()末尾加  arr.pop()末尾减  arr.unshift()开头加  arr.shift()开头减

*every*:用于判断数组中是否每一个元素都符合条件，返回布尔值，参数为一个函数

*some*:用于判断数组中是否有满足条件的元素，返回布尔值，参数为一个函数

*filter*:用于过滤数组，返回满足条件的新数组，参数为一个函数

*map*:用于遍历处理数组，返回处理后的新数组

*reduce*:https://blog.csdn.net/Symin_/article/details/120346080

**---JS数组处理函数---**

**---JS字符串处理函数---**

*substring*:用于提取字符串中位于两下标间的字符，返回一个新的字符串
    `String.substring(start,end)`
    String:待处理字符串
    start:必填；非负整数；起始位置
    end:选填；非负整数；结束位置；若不填则默认到结尾
        ps：1>该方法返回的字符串包括start位置的字符但不包括end位置的字符
            2>若start == end，则返回空串
            3>若start > end，处理前会交换两参数位置
            4>若start或end为负数，则会被替换为0

*substr*:用与返回一个从指定位置开始的指定长度的字符串，返回一个新的字符串
    `String.substr(start,length)`
    start:必填；起始位置；若为负数，则倒数
    length:选填；指定长度；若不填则默认到结尾

*slice*:提取指定下标之间的字符串，返回一个新的字符串
    `String.slice(start,end)`
    类似于substring，区别：当参数为负数时，slice倒数，substring被替换为0

*split*:用于把字符串分割成片段创建一个字符串数组
    `String.split(sep,length)`
    sep:必填；字符串或正则
    length:选填；要分割的段数

*charAt*:返回指定位置的字符
    `String.charAt(index)`
    index:指定位置；若为负数或大于字符串长度则返回空

*concat*:连接两个或多个字符串
    `String.concat(String...)`

*replace*:对字符串进行查找和替换操作，返回一个新的字符串
    `String.replace(searchVal,replaceVal)`
    searchVal:查找的值；字符串或正则
    replaceVal:要替换的值

*大小写转换*:toLowerCase()  toUpperCase()  toLocalLowerCase()  toLocalUpperCase()

**---JS字符串处理函数---**

**---JS对象处理函数---**

*assign*:用于将可枚举的属性从一个或多个源对象分配到目标对象，返回目标对象
    `Object.assign(targetObj,sourceObj...)`
    targetObj:目标对象
    sourceObj:源对象
        ps:若有同名属性，则后面的源对象属性覆盖前面的属性
    
*is*:用于判断两个对象是否相等（浅拷贝）
    `Object.is(Obj1,Obj2)`

*defineProperty*:用于给对象添加属性
    `Object.defineProperty(Obj,propName,description)`
    Obj:源对象
    propName:字符串；属性名
    description:属性描述；对象类型
    https://www.cnblogs.com/junjun-001/p/11761252.html#commentform
    
**---JS对象处理函数---**
