### 必须注释
  - 以下情况，务必添加注释
  ```
  1.公共组件使用说明
  2.各组件中重要函数或者类说明
  3.复杂的业务逻辑处理说明
  4.特殊情况的代码处理说明,对于代码中特殊用途的变量、存在临界值、函数中使用的hack、使用了某种算法或思路等需要进行注释描述
  5.注释块必须以/**（至少两个星号）开头**/；
  6.单行注释使用//；
  7.多重 if 判断语句
  ```

### 注释规则
- data 注释
    - 单行属性，注释写在行尾
    ``` 
    data(){
        return {
            productName: 'productName',// 产品名称
        }
    }
    ```
    - 多行属性，注释写在行上
    ```
    data(){
        return {
            // swiper配置
            swiperOption:{
                loop: true,
                autoplay: true,
                ...
            }
        }
    }
    ```
- props、computed、watch 注释
    - 统一采用行上注释
    ```
    props:{
        // 当前页码
        pageIndex : {
            type : Number,
            default : 1
        },
    }
    ```

- methods 注释
    - 【1】无参数时，采用 "//"进行注释
    ```
    methods:{
        // 重置
        reset(){
            this.pageIndex=1;
            this.search = {};
            this.list=[];
        }
    }
    ```
    - 【2】有参数时，需进行功能、参数、返回值说明。
    ```
    methods:{
        /**
        * @desc 切换tab
        * @param index [Int] 切换tab的index
        * @param ...
        */
        switchTab(index,[...args]){
            ...
        }
    }
    ```
