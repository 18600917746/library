#几种实现双向绑定的做法 [mvvm的实现原理](https://github.com/DMQ/mvvm)
    目前几种主流的mvc(vm)框架都实现了单向数据绑定，而我所理解的双向数据绑定无非就是在单向绑定的基础上给可输入元素（input、textare等）添加了change(input)事件，来动态修改model和 view，并没有多高深。所以无需太过介怀是实现的单向或双向绑定。

>发布者-订阅者模式（backbone.js）

     一般通过sub, pub的方式实现数据和视图的绑定监听，更新数据方式通常做法是 vm.set('property', value)
>脏值检查（angular.js）

    DOM事件，譬如用户输入文本，点击按钮等。( ng-click )
    XHR响应事件 ( $http )
    浏览器Location变更事件 ( $location )
    Timer事件( $timeout , $interval )
    执行 $digest() 或 $apply()
>数据劫持（vue.js）