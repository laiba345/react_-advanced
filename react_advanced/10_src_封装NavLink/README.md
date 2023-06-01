# 封装NavLink
- 想要继续获取高亮效果,还是需要使用到NavLink标签来进行实现
- 其实标签体是一个特殊的标签属性,通过标签体指定的Home或About也可以通过props获取
    - 可以通过this.props获取
    - 不过props中的值进行指定的时候,键名已经是固定的了
    - 不一定要配置标签体,直接通过解构赋值来进行相关操作即可

# NavLink与封装NavLink
- NavLink可以实现路由链接的高亮,通过activeClassName指定样式名
- 标签体内容是一个特殊的标签属性
- 通过this.props.children可以获取标签体内容