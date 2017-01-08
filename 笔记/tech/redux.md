+ `createStore` 函数接受另一个函数作为参数，返回新生成的 Store 对象

+ 只要 State 相同，View 就相同。你知道 State，就知道 View 是什么样，反之亦然

+ State 的变化，会导致 View 的变化。但是，用户接触不到 State，只能接触到 View。所以，State 的变化必须是 View 导致的。Action 就是 View 发出的通知，表示 State 应该要发生变化了。

  ​

+ State 的变化，会导致 View 的变化。但是，用户接触不到 State，只能接触到 View。所以，State 的变化必须是 View 导致的。Action 就是 View 发出的通知，表示 State 应该要发生变化了。

+ `store.dispatch()`是 View 发出 Action 的唯一方法

+ Store 收到 Action 以后，必须给出一个新的 State，这样 View 才会发生变化。这种 State 的计算过程就叫做 Reducer。

+ Store 允许使用`store.subscribe`方法设置监听函数，一旦 State 发生变化，就自动执行这个函数

+ `createStore`方法还可以接受第二个参数，表示 State 的最初状态。这通常是服务器给出的。注意，如果提供了这个参数，它会覆盖 Reducer 函数的默认初始值。

+ ​

  ```
  let store = createStore(todoApp, window.STATE_FROM_SERVER)
  ```

  ​

+ const store = createStore(reducer);

+ var current_state = store.getState();

+ store.dispatch(action)





es6