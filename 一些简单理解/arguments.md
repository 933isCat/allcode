



# arguments(函数才能用，每个函数都有，存储实参的一个伪数组。如get（1,2,3）=arguments=[1,2,3])（arguments会把函数的实参看成一个伪数组）

```js
// arguments 的使用  只有函数才有 arguments对象  而且是每个函数都内置好了这个arguments
// 伪数组 并不是真正意义上的数组
	// 1. 具有数组的 length 属性
	// 2. 按照索引的方式进行存储的 
	
	// 3. 它没有真正数组的一些方法 pop()  push() 等等
```

## 遍历arguments

```js
// 遍历arguments
        function get() {
            for (var i = 0; i < arguments.length; i++) {
                arguments[i]
                //console.log(arguments[i]);这个叫遍历。

            }
            return arguments
        }
        var weiarr = get(2, 1, 3, 4, 1);
        console.log(weiarr);
```

## arguments使用方法

```js
//利用arguments计算出 实参的最大值
        function getMax() {
            var max = arguments[0];
            for (var i = 1; i < arguments.length; i++) { /先遍历 实参 也就是arguments里面的元素
                if (arguments[i] > max) {
                    max = arguments[i]
                }
            }
            return max
        }
        console.log(getMax(1, 234, 5, 6, 7));
        console.log(getMax(9, 5, 2, 1, 5, 6, 222));
```

```js
//利用函数翻转用户输入的实参
        function getArr() {
            var newArr = [];
            for (var i = 0; i < arguments.length; i++) {
                newArr[newArr.length] = arguments[arguments.length - i - 1]
            }
            return newArr
        }
        console.log(getArr(1, 2, 3, 4, 2, 2, 11));
```

```js
//函数冒泡排序 实参比大小 排序
        function sort() {
            for (var i = 0; i < arguments.length - 1; i++) {
                for (var j = 0; j < arguments.length - i - 1; j++) {
                    if (arguments[j] > arguments[j + 1]) {
                        var temp = arguments[j]
                        arguments[j] = arguments[j + 1]
                        arguments[j + 1] = temp
                    }
                }
            }
            return arguments
        }
        console.log(sort(2, 34, 1, 4, 56, 7));
```



# 













