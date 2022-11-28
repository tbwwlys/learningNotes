# <font color=MediumPurple>ES6 新特性</font>

## <font color=blue>1、支持 let 和 const </font>

```js
let a = 1;
cont b = 2;
```

<p>这样就避免了使用 var 声明变量引发的变量提升等问题</p>

## <font color=blue>2、支持了模块化</font>

```js
//导出 main.js
export let name = 'zzz';
export function fun(arg) {
    return arg;
} 
//导入
import {name, sixuetang} from 'main.js'
```

<p>将需要导出的函数或变量前面加 export代表导出,import 代表导入,上面的示例是从 mian.js的文件中导入 name变量和 fun函数

## <font color=blue>3、支持解构</font>

```js
// 从数组中取值
const arr = [1, 2, 3, 4, 5];
let [a, b] = arr;//取到了第一项和第二项的值
let [a, , , b] = arr; //取到 第一项和第四项的值
// 从对像中取值
const obj = {
    a: 1,
    b: 2,
    c: 3
}
let {a, b, c} = obj; //将对象的key值和对应的变量名称一一对应起来
//交换两个变量的值
let a = 1;
let b = 2;
[a, b] = [b, a]; //将a和b交换位置后放置到原始的数组中
```

## <font color=blue>4、支持扩展运算符</font>

```js
// 拷贝数组
let arr = [1, 2, 3];
let arr1 = [1,...arr];// 将arr 放到 arr1 中得到 [1, 1, 2, 3]
// 合并数组
let arr2 = [1, 2, 3];
let arr3 = [4, 5, 6];
let arr4 = [...arr2,...arr3];
// 将数组扩展为函数参数
function zzz(x, y, z) {
    return x + y + z;
}
const numbers = [1, 2, 3];
zzz(...numbers);// 传入数组的扩展作为参数
// 克隆对象、合并对象
let obj = {name: 'zzz', age: 18};
let obj1 = {city: 'ja'};
let obj2 = {...obj, ...obj1};
// 排除一些对象属性
let params = {
    name: 'zzz',
    age: 18,
    type: 1
}
let {type, ...other} = params;
console.log(other); //输出 { name: 'zzz', age: 18 } other可以写任意命名比如 nameAge

```

## <font color=blue>5、支持直接在参数上赋值</font>

```js
function fun(name = 'zzz', age = 18){}
```

## <font color=blue>6、支持对象属性的简写</font>

```js
const name = 'zzz', age =18, city = 'ja';
const userInfo = {
    name: name;
    age: age;
    city: city;
}
```

##  <font color=blue>7、支持 async 、await异步调用方式</font>

```js
async function fun(params) {
    let res = await getList(params) 
    if(res.code === 1) {
            
    }
}
```



## <font color=blue>8、支持 includes 方法</font>

```js
let arr = [1, 2, 3];
if(arr.includes(2)){
    // ...
}//判断arr中是否包含 2 ，如果包含就返回true
```

## <font color=blue>9、指数操作符</font>

```js
2**10 //1024
```

## <font color=blue>10、支持Object.keys、Object.values、Object.entries</font>

```js
// Object.keys
const obj = {a: 1, b: 2,c: 3};
const keys = Object.keys(obj); // [ 'a', 'b', 'c' ] 对象的键的集合
//Object.values
const values = Object.values(obj); //[ 1, 2, 3 ] 值的集合
// Object.entries
const entries = Object.entries(obj); // [ [ 'a', 1 ], [ 'b', 2 ], [ 'c', 3 ] ] 键值对的集合 
entries：entry复数 条目;入境次数;记录
```

## <font color=blue>11、null传导运算符 ?.     null判断运算符 ??</font>

```js
// null传到运算符
const obj = {a: 1, b: 2,c: 3}; 
let num = (obj && obj.a) || 'null'; //这里返回1
let num = obj?.a?.b || 'null'; // 安全的找到对象obj中a的值，如果没找到则返回 null，从左往右如果有一个找不到则返回undefined ， 这里 a 里面是没有 b 的所以返回 undefined ，但我这里又设置了 短路 或|| 所以返回 null
//null 判断运算符??
let num = obj.a ?? null; //这里返回 a 的值 1;当obj中没有属性a时，就会返回 null
```

## <font color=blue>12、模板字符串</font>

```js
// ${变量名}
const name = 'zzz';
const age = 18;
const myInfo = `myname is ${name},my age is ${age}.`; //返回 myname is zzz,my age is 18.
// 变量的运算
const result = `${name} ${age > 18 ? '成年了' : '未成年'}`; //返回 zzz 未成年结束
```



> <font color=Feldspar size=16>I don't want to fail, so I fight on. </font>
>
> <font style="background:DarkSeaGreen" size=5>因为我不甘失败所以要奋斗。</font>

