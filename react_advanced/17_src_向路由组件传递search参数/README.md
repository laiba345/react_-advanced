# 向路由组件传递search参数
1. 形如 key=value&key=value的编码形式就是urlencoding编码的形式
2. 需要明确清楚自己的需求,很关键; 截取数组的某一部分的值,使用slice() 函数
3. 为啥叫做search函数, 因为其落在search属性上

## 总结search参数
1. 路由链接(携带参数): <Link to={'/demo/test?name=tom&age=18'}>详情</Link>
2. 注册路由(无需声明,正常注册即可): <Route path="/demo/test" component={Test}/>
3. 接收参数: this.props.location.search
备注: 获取到的search是urlencoded编码字符串,需要借助querystring解析







