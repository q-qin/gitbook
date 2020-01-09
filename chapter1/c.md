### ES6 风格编码规范
  - 定义变量使用 `let` ,定义常量使用 `const`
  - 静态字符串一律使用单引号或反引号，动态字符串使用反引号
  - 推荐使用解构赋值，如

    ```
    const arr = [1, 2, 3, 4];
    // 推荐
    const [first, second] = arr;
    // 不推荐
    const first = arr[0];
    const second = arr[1];
    ```
  - 推荐使用扩展运算符（...）拷贝数组，对象亦如此
    ```
    const items = [1, 2, 3, 4, 5];
    // 推荐
    const itemsCopy = [...items];
    // 不推荐
    const itemsCopy = items;
    ```
  - 除必需要使用函数表达式的场合外，尽量用箭头函数代替。尽量不要省参数括号，如`list.forEach((m)=>{})`

### 其他规范
  - 避免 this.$parent
  - 除了三目运算，if,else 等禁止简写，如
  ```
  // 不推荐
  if (true) alert(name);
  ```
  - 如无特殊情况，变量统一放到 `data()` 内，避免组件重用时代码不被执行

