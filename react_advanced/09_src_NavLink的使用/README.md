# 路由组件和一般组件
1. 路由组件一般放在pages文件夹当中
2. 最大的区别:路由组件会收到路由器四传递过来的3个最重要的props信息
    - history
    - location
    - match

## 总结区别
1.写法不同：
    一般组件：<Demo/>
    路由组件：<Route path="/demo" component={Demo}/>
2.存放位置不同：
    一般组件：components
    路由组件：pages
3.接收到的props不同：
    一般组件：写组件标签时传递了什么，就能收到什么
    路由组件：接收到三个固定的属性
    ```
    history:
		go: ƒ go(n)
		goBack: ƒ goBack()
		goForward: ƒ goForward()
		push: ƒ push(path, state)
		replace: ƒ replace(path, state)
	location:
		pathname: "/about"
		search: ""
		state: undefined
	match:
		params: {}
		path: "/about"
		url: "/about"
    ```

4. NavLink
- 和Link的区别;**点击NavLink会添加上相应的类名属性**
    - activeClassName="atguigu"
    - activeClassName的默认值是active
- 因为所有的内容其实都需要放在index.html中,所以可以直接在此处书写样式
    - 有时候样式在演示的时候会出现优先级不够,显示的时候有问题,可以使用!important提高优先级
