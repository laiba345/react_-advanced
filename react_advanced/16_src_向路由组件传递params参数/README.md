# 向路由组件传递params参数
- 此处已经变成三级路由了
- 点击消息，想要生成相应的内容，可以在state当中进行配置操作
- 在react中书写结构的话，可以在{}中配置相应的结构，使用到相应方法的时候，也可以使用
将结构以return的形式返回出去才行
- 在react当中，动态的内容通过{}来进行表示出来, 区别与vue中的内容通过{{  }} 来进行表示

## 回顾之前ajax是如何传递参数的
1. query
2. params
3. body
    - 请求体参数，还有两种编码形式：urlencoded；json


## 如何给路由组件传递参数
1. 携带params参数，携带参数的时候如果有别的表达式，需要用扩号扩上才行
2. 模版字符串中想引入一些花括号的东西，需要使用${}的形式
3. 使用:的形式来进行传递操作，
4. 最后传递拿到的内容就是在this.props.match.param 可以拿到最后的传递过来的params参数

## 总结笔记；向路由组件传递参数
1. param参数
    - 路由链接(携带参数):<Link to={'/demo/test/tom/18'}>详情</Link>
    - 注册路由(声明接收):<Route path="/demo/test/:name/:age" component={ Test } />
    - 接收参数：const { id, title } = this.props.match.params







