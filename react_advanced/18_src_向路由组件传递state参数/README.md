# 向路由组件传递state参数
- 上面两种传递参数的形式都会在地址栏中观察到
- state参数可以不在地址栏中显示
    - 第一个花括号表示jsx表达式,第二个表示一个对象{{  }}
    - 既然是对象,就可以带上多组key-value的形式
- 接收state参数: const {  } = this.props.location.state
- 常用写法: something || {} ; 前面有值我们就用前面的对象,没有的话,使用的就是空对象

- 总结: 向路由组件传递state参数
    - 	路由链接(携带参数)：<Link to={{pathname:'/demo/test',state:{name:'tom',age:18}}}>详情</Link>
	- 注册路由(无需声明，正常注册即可)：<Route path="/demo/test" component={Test}/>
	- 接收参数：this.props.location.state
	- 备注：刷新也可以保留住参数









