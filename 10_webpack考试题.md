### 选择题

1. `D`

2. `C`

3. `D`

4. `B`

5. `A`

6. `C`

7. `C`

8. `D`

9. `C`

10. `A`

11. `B`

12. `A`

13. `C`

14. `B`

    答案：D

15. `A`

16. `A`

17. `B`

18. `C`

19. `D`

    答案：A

20. `D`

21. `D`

22. `D`

    答案：A

23. `C`

24. `B`

25. `D`

    答案：C

26. `C`

27. `D`

28. `B`

29. `C`

    答案：D

30. `D`

### 填空题

1. `Node.js`；`webpack.config.js`；`CommonJS`；`js普通对象`；`json对象`

   答案：`模块化`；`~`；`~`；`对象或函数`；`对象或函数`

2. `loader`；`plugin`；`css modules`；`babel`

   答案：`~`；`~`；`postcss`；`~`

3. `bundle analyzer`

### 问答题

1. ```markdown
   - module：任何被入口直接或间接依赖的文件
   - chunk：一个用于分析依赖、生成资源列表的块
   - bundle：chunk打包合并后的资源文件
   ```

   参考答案：

   ```markdown
   - module：webpack将源码中所有文件视为module
   - chunk：chunk是webpack在打包期间，相对独立的打包通道。webpack会根据入口来创建对应的chunk，每个chunk可能对应一个或多个入口模块，webpack根据这些模块寻找依赖关系，然后依次解析，在chunk内部完成最终资源的生成
   - bundle：chunk打包完整后端资源，通常指最终打包完成的JS文件
   ```

   

2. ```markdown
   - loader原理：在读取模块文件内容后和进行抽象语法树分析前进行loader处理，即通过loader提供的函数将读取的源码字符串转换成符合处理后所要求的源码字符串
   - plugin原理：通过在控制打包全过程中的核心compiler对象提供的hooks钩子函数上注册，来在打包的某个特定阶段中调用plugin
   ```

   参考答案：

   ```markdown
   - loader：本质上是一个函数，该函数的作用是对某个模块的代码进行转换，返回另一种代码。webpack在读取模块代码后，如果根据配置匹配到了某些loader，则会将该模块的代码依次交给loader转换，当loader完成了代码转换，再进一步解析代码、分析依赖
   - plugin：本质上是一个对象，通常通过构造函数创建。该对象中提供apply方法，方法接收一个参数，该参数是webpack的编译对象，通过这个编译对象，apply方法可以注册一些钩子函数，从而参与到webpack的打包周期，完成对打包行为的改变和控制
   ```
