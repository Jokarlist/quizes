### 选择题

1. `D`

   解析：父组件可以通过`$children`访问子实例，并非`$childrens`

2. `CE`

   答案：BE

   解析：

   - B：v-else不能用于template元素上，因为template最中不会渲染到页面上，会导致v-else指令作用于一个不存在的dom上，会失效
   - D：v-if需要不停的销毁和创建元素，频繁的操作DOM，会消耗更大的性能。如果要频繁的切换某节点，使用v-show(切换开销小，初始开销大)。如果不需要频繁切换某节点，使用v-if(切换开销大，初始开销小)

3. `A`

4. `ACD`

5. `AC`

   解析：

   - B：通过 this.$refs.cmpName 获取到的为该组件实例
   - D：通过 this.$refs.domName 获取到的为一个数组，该数组为通过v-for渲染出来的元素的集合

6. `AC`

   解析：

   - B：除了在表单元素上使用外，v-model 还可以用于组件上
   - D：修饰符 .trim 只可以删除文本首尾的空白字符

7. `BCD`

   解析：

   - A：除了数组外，还可以使用对象、数字、字符串

8. `CD`

   解析：

   - C：v-bind可以没有参数，没有参数时，可以绑定一个包含键值对的对象
   - D：绑定prop时，prop必须在子组件中声明

9. `C`

   解析：监听组件的原生事件时，需要使用修饰符 .native

10. `D`

    答案：A

    解析：v-text更新的是元素的textContent

11. `A`

    答案：B

    解析：想要隐藏未编译的Mustache标签，需要配合css规则，如[v-cloak]{ display: none }

12. `AB`

    解析：

    - C：计算属性函数式配置时默认只有getter，当想要使用setter时，可以采用对象式配置，如：{ get() {}, set() {} }
    - D：计算属性setter函数的参数为计算属性更新后的值

13. `AC`

    解析：

    - B：同时多次更改同一个数据，watch函数只会执行一次，默认为异步，如果想要同步监听，可以配置sync: true
    - D：监听器默认情况下，只监听引用值的变化，若想监听对象属性值的变化，可以开启深度监听deep: true

14. `D`

    解析：能够第一个拿到data数据的钩子函数为：created，故在beforeCreate函数内无法拿到data，其值为undefined

15. `ACE`

    答案：ABCE

    解析：

    - B：除数组变异方法外，还可以通过Vue.set/Vue.delete更改数组数据
    - C：Vue是异步更新视图的，故多次更改数据不会导致页面重新渲染多次
    - E：在nextTick中，会使用Promise(微任务)、MutationObserver(微任务)、setImmediate(宏任务)、setTimeout(宏任务)

16. `D`

17. `AB`

    答案：B

18. `D`

19. `B`

20. `AB`

21. `BC`

    答案：BDE

    解析：

    - B：不可以，mutation只能同步更改数据
    - D：还可以通过辅助函数提交mutation
    - E：非store实例，而是一个store上下文对象

22. `B`

    答案：C

    解析：过滤器参数，为前一个表达式的结果，并非第一个表达式的结果

23. `C`

    解析：当bind和update时触发相同的行为，而不关系其它钩子时，可以进行函数式简写，如：Vue.derective(‘v-xxx’, function (el, binding) {})

24. `D`

    解析：`<transition>`组件不会被渲染成为任何真实元素，`<transition-group>`组件才会以一个真实元素呈现，默认为`<span>`

25. `CD`

    解析：

    - A：以render为主
    - B：可以同时存在，只不过Vue脚手架默认不能存在template选项

### 填空题

1. `push`；`pop`；`shift`；`unshift`；`splice`；`sort`；`reverse`

2. `router-link`；`router-view`

3. `state`；`mutations`；`actions`；`getters`；`namespaced`；`modules`；`strict`

4. `mapState`；`mapGetters`；`mapMutations`；`mapActions`

5. `v-enter`；`v-enter-to`；`v-enter-active`；`v-leave`；`v-leave-to`；`v-leave-active`

6. `-`

   答案：`install`

7. `mixin`

   答案：`Vue.mixin`

8. `-`

   答案：`异步`

9. `getter`；`setter`；`readable`；`writable`；`configurable`；`-`

   答案：`get`；`set`；`value`；`writable`；`configurable`；`enumerable`

10. `depend`；`inject`

    答案：`provide`；`inject`

11. `v-model`；`sync`

12. `-`

    答案：`model`

13. `strict`

    答案：`strict: true`

14. `-`

    答案：`is`

### 问答题

1. ```markdown
   - created是在组件配置数据注入并完成数据响应式后，即组件实例创建完成后运行的钩子函数
   - mounted是在虚拟dom树渲染成真实dom树并挂载到页面某个根元素上时运行的钩子函数
   ```

   参考答案：

   ```markdown
   - created：在模板渲染完成前调用，此时不能对dom进行操作
   - mounted：在模板渲染完成后调用，此时可以对dom进行操作
   ```
   
   
   
2. ```markdown
   - computed是计算属性，创建每一个计算属性时会自动的记录相应依赖，当依赖发生变化时computed函数会自动运行，完成数据响应式变化
   - methods是组件实例的方法，方法只能手动调用而不会自动运行
   ```
   
   参考答案：
   
   ```markdown
   - computed：计算属性是基于他们的依赖进行缓存的，只有他的相关依赖发生改变时才会重新求值。
   - methods：只要重新渲染，总是会执行methods函数
   ```

### 拓展题

1. ```markdown
   - VueRouter的原理：通过在BOM中的history API的状态栈手动添加记录而实现的链接跳转，并且阻止了链接跳转时页面刷新的默认事件
   ```

   
   
2. ```markdown
   - Vue2的响应式原理：
   ```

   
   
3. ```markdown
   - Vuex的原理：首先建立一个存储数据的仓库state，不对其中的数据进行直接操作，而是通过mutations和actions中的提供的方法对其间接的操作，这样便可在数据发生改变时接受到通知并可以按意愿做各种处理
   ```

   
   
4. ```markdown
   - beforeCreate：实例初始化之后，进行数据侦听（data observation）和事件/侦听器（event/watcher）的配置之前被调用。该钩子主要用于实例初始化之后完成数据响应式之前进行操作
   - created：实例创建完成后调用，此时已完成数据响应式，即data侦听、computed、methods以及event/watcher的配置已完成，可获取到响应式数据。该钩子主要用于虚拟dom树创建前对响应式数据进行处理
   - beforeMount：挂载开始之前调用，相关的render函数首次被调用。
   - mounted：实例被挂载后调用，此时el被新创建的vm.$el替换了。若根实例挂载到了一个文档内的元素上，当mounted被调用时vm.$el也在文档内。
   - beforeUpdate：在数据发生改变后，DOM被更新之前被调用。该钩子主要用于现有DOM被更新前进行访问并执行操作，例如移除手动添加的事件监听器。
   - updated: 在数据更改导致的虚拟DOM重新渲染和更新完毕之后被调用。该钩子此时可以进行依赖于DOM的操作，但是大多数情况下应避免在此期间更改状态，若需要改变状态，通常使用computed或watcher取代之。
   - beforeDestroy：实例销毁之前调用，此时实例仍然完全可用，还可以获取真实dom。该钩子主要在组件失活前进行操作。
   - destroyed：实例销毁后调用。该钩子被调用后，对应vue实例的所有指令都被解绑，所有事件监听器被移除，所有的子实例也都被销毁。
   ```

   
   
5. ```markdown
   1. 导航被触发。
   2. 在失活的组件里调用 beforeRouteLeave 守卫。
   3. 调用全局的 beforeEach 守卫。
   4. 在重用的组件里调用 beforeRouteUpdate 守卫 (2.2+)。
   5. 在路由配置里调用 beforeEnter。
   6. 解析异步路由组件。
   7. 在被激活的组件里调用 beforeRouteEnter。
   8. 调用全局的 beforeResolve 守卫 (2.5+)。
   9. 导航被确认。
   10. 调用全局的 afterEach 钩子。
   11. 触发 DOM 更新。
   12. 调用 beforeRouteEnter 守卫中传给 next 的回调函数，创建好的组件实例会作为回调函数的参数传入
   ```

   

   
