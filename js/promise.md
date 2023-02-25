## promise
1. 概念  
**Promise 是异步编程的一种解决方案**，比传统的解决方案——回调函数和事件——更合理和更强大。它由社区最早提出和实现，ES6 将其写进了语言标准，统一了用法，原生提供了Promise对象。  
所谓Promise，简单说就是一个容器，里面保存着某个未来才会结束的事件（通常是一个异步操作）的结果。从语法上说，Promise 是一个对象，从它可以获取异步操作的消息。Promise 提供统一的 API，各种异步操作都可以用同样的方法进行处理。  （提供了一种更优雅的方式处理js异步任务）
2. 基本用法
Promise构造函数接受一个函数作为参数，该函数的**两个参数分别是resolve和reject**。它们是两个函数，由 JavaScript 引擎提供，不用自己部署。  
resolve函数的作用是，将**Promise对象的状态从“未完成”变为“成功”**（即从 pending 变为 resolved），在异步操作成功时调用，并**将异步操作的结果，作为参数传递出去；**
reject函数的作用是，将**Promise对象的状态从“未完成”变为“失败”**（即从 pending 变为 rejected），在异步操作失败时调用，并**将异步操作报出的错误，作为参数传递出去。**
Promise实例生成以后，可以用then方法分别指定resolved状态和rejected状态的回调函数。
2. 实例属性和方法  
**then：** 参数 两个函数 一个resolve 一个reject  
**catch：** rejcet  
**finally：** 在 执行完then,catch 之后执行   
**Promise.all：** Promise.all()方法用于将**多个 Promise 实例**，包装成一个新的 Promise 实例。
const p = Promise.all([p1, p2, p3]);
上面代码中，Promise.all()方法接受一个数组作为参数，p1、p2、p3都是 Promise 实例，如果不是，就会先调用下面讲到的Promise.resolve方法，将参数转为 Promise 实例，再进一步处理。另外，Promise.all()方法的参数可以不是数组，但必须具有 Iterator 接口，且返回的每个成员都是 Promise 实例。（接收promise类型的数组，如果数组成员不是promise，就用promise.resolve包装）  
  - 一个成功promise -> [res]
  - 两个成功promise -> [res, res]
  - 一个失败promise -> err
**Promise.race：** Promise.race()方法同样是将多个 Promise 实例，包装成一个新的 Promise 实例。
上面代码中，只要p1、p2、p3之中**有一个实例率先改变状态，p的状态就跟着改变。那个率先改变的 Promise 实例的返回值**，就传递给p的回调函数。
  - 一个成功promise -> 第一个结束的promise res
  - 两个成功promise -> 第一个结束的promise res
  - 一个失败promise -> 第一个结束的promise res
**Promise.allSettled：** Promise.allSettled()方法，用来确定**一组异步操作是否都结束**了（不管成功或失败）。所以，它的名字叫做”Settled“，包含了”fulfilled“和”rejected“两种情况。
  - 一个成功promise -> 都是包含 status，value 或者 reason 的数组对象
  - 两个成功promise -> 都是包含 status，value 或者 reason 的数组对象
  - 一个失败promise -> 都是包含 status，value 或者 reason 的数组对象
**Promise.any：**只要参数实例有一个变成fulfilled状态，包装实例就会变成fulfilled状态；如果所有参数实例都变成rejected状态，包装实例就会变成rejected状态。
  - 一个成功promise -> [res]
  - 两个成功promise -> [res, res]
  - 一个失败promise -> err
