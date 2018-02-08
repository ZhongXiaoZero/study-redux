关于redux的一些总结


store 保存数据的地方，容器

createStore方法生产store

state，因为store里面包含着所有的数据，需要获取某个时候的数据，就需要对store生成快照。这个时点的数据集合就是state

Redux 规定， 一个 State 对应一个 View。只要 State 相同，View 就相同。你知道 State，就知道 View 是什么样，反之亦然。

Action state的变化会导致View的变化，其实就是个行为，如果触发了一个行为就会导致state要发生变化，Action就是View发出的通知（

Action是一种对象，里面的type是必须有的，代表着行为的名称，当然可以带的内容，相当于这次行为所携带的信息。

store.dispatch()是View 发出Action的唯一方法。

Reducer Store收到action以后，必须给出一个新的State，这样的View才可以变化。这种State的计算过程就叫做Reducer。