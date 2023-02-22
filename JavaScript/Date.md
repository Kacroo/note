**时间处理函数**
function formatDateTime(date){
var y = date.getFullYear()
var m = date.getMonth() + 1
m = m < 10 ? ('0' + m) : m
var d = date.getDate()
d = d < 10 ? ('0' + d) : d
var h = date.getHours()
h = h < 10 ? ('0' + h) : h
var minute = date.getMinutes()
minute = minute < 10 ? ('0' + minute) : minute
var second = date.getSeconds()
second = second < 10 ? ('0' + second) : second
return y + '-' + m + '-' + d + ' ' + h + ':' + minute + ':' + second
}
var d = new Date()
console.log(formatDateTime(d))

**Date()对象**
// 日期格式
var date = new Date()
console.log(date) // 2022-01-13T06:00:58.816Z

// 日期格式转时间戳(精确到毫秒)
console.log(date.getTime()) // 1642053732522
// 日期格式转时间戳(精确到秒，后三位取 0)
console.log(Date.parse(date)) // 1642053882000

// 时间戳转日期
console.log(new Date(1642053732522)) // 2022-01-13T06:02:12.522Z

// 日期格式转字符串：函数

// 字符串转时间戳
var string = '2022-01-13 14:10:24'
console.log(Date.parse(string.replace(/-/g,'/'))) // 1642054224000
// 字符串转日期格式
console.log(new Date(Date.parse(string.replace(/-/g,'/')))) // 2022-01-13T06:10:24.000Z
