## Set
1. 概念  
ES6 提供了新的数据结构。**它类似于数组，但是成员的值都是唯一的，没有重复的值**。Set 本身是一个构造函数，用来生成 Set 数据结构。
2. 实例属性和方法  
Set 结构的实例有以下属性。  
Set.prototype.constructor：构造函数，默认就是Set函数。  
Set.prototype.size：返回Set实例的成员总数。  
Set 实例的方法分为两大类：操作方法（用于操作数据）和遍历方法（用于遍历成员）。下面先介绍四个操作方法。  
Set.prototype.add(value)：添加某个值，返回 Set 结构本身。  
Set.prototype.delete(value)：删除某个值，返回一个布尔值，表示删除是否成功。  
Set.prototype.has(value)：返回一个布尔值，表示该值是否为Set的成员。  
Set.prototype.clear()：清除所有成员，没有返回值。
3. 遍历操作  
Set 结构的实例有四个遍历方法，可以用于遍历成员。  
Set.prototype.keys()：返回键名的遍历器  
Set.prototype.values()：返回键值的遍历器  
Set.prototype.entries()：返回键值对的遍历器  
Set.prototype.forEach()：使用回调函数遍历每个成员  
4. 特点
- 需要特别指出的是，**Set的遍历顺序就是插入顺序**。这个特性有时非常有用，比如使用 Set 保存一个回调函数列表，调用时就能保证按照添加顺序调用。
-  扩展运算符（...）内部使用for...of循环
## WeakSet
1. 概念  
WeakSet 结构与 Set 类似，也是不重复的值的集合。但是，它与 Set 有两个区别。  
首先，**WeakSet 的成员只能是对象**，而不能是其他类型的值。  
其次，**WeakSet 中的对象都是弱引用，即垃圾回收机制不考虑 WeakSet 对该对象的引用，也就是说，如果其他对象都不再引用该对象，那么垃圾回收机制会自动回收该对象所占用的内存，不考虑该对象还存在于 WeakSet 之中**。（每个对象多次引用时会有一个引用数，WeakSet 中该对象不会增加引用数，当该对象的引用数为0时，垃圾回收机制会清除包括WeakSet中的对象）  
**WeakSet 的成员是不适合引用的，因为它会随时消失**。
2. 实例属性和方法  
WeakSet 结构有以下三个方法。  
WeakSet.prototype.add(value)：向 WeakSet 实例添加一个新成员。  
WeakSet.prototype.delete(value)：清除 WeakSet 实例的指定成员。  
WeakSet.prototype.has(value)：返回一个布尔值，表示某个值是否在。
# Map
1. 概念  
为了解决这个问题，ES6 提供了 Map 数据结构。它类似于对象，也是键值对的集合，**但是“键”的范围不限于字符串，各种类型的值（包括对象）都可以当作键**。也就是说，Object 结构提供了“字符串—值”的对应，Map 结构提供了“值—值”的对应，是一种更完善的 Hash 结构实现。如果你需要“键值对”的数据结构，Map 比 Object 更合适。
2. 实例属性和方法  
size  
set  
get  
has  
delete  
clear  
3. 遍历方法    
Map 结构原生提供三个遍历器生成函数和一个遍历方法。  
Map.prototype.keys()：返回键名的遍历器。  
Map.prototype.values()：返回键值的遍历器。  
Map.prototype.entries()：返回所有成员的遍历器。  
Map.prototype.forEach()：遍历 Map 的所有成员。  
4. 特点  
**Map 也可以接受一个数组作为参数。该数组的成员是一个个表示键值对的数组。**（参数接收二维数组）
## weakMap
1. 概念   
WeakMap结构与Map结构类似，也是用于生成**键值对的集合**。WeakMap**只接受对象作为键名**（null除外），不接受其他类型的值作为键名。
不过，现在有一个提案，允许 Symbol 值也可以作为 WeakMap 的键名。一旦纳入标准，就意味着键名存在两种可能：对象和 Symbol 值。
weakMap也是弱引用（类map的结构，只接收对象作为键名，未来可以允许symbol支持键名）
2. 实例属性和方法  
set  
get  
has  
delete  