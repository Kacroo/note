**联合类型和交叉类型**：
const name:String | undefined   --- 联合类型，name的类型可以为String或undefined


**interface和type的区别**:
1.类型别名；interface只能是对象类型，type可以是联合类型、交叉类型、基础类型等。
2.合并声明；interface重名会合并，type重名会报错。
3.默认导出；interface支持声明同时导出，type要先声明再导出。
4.扩展性；interface可以继承，从而扩展多个接口或类，type没有扩展功能只能交叉合并。
    interface Person {
        name:string
    }
    interface User extends Person{
        age:number
    }


    // 3、type类型 & type类型
    type Person = { name:string }
    type User = Person & { age:number }
    
    // 4、interface类型 & type类型
    interface Person{
        name:string
    }
    type User = { age:number } & Person
    
    **any和unknown**
    any类型的值可以被赋予任意值，也可以付给其他值；
    unknown可以被赋予任意值，但是只能付给any或自身
    unknown不能读任何属性，也不能调用方法； 
