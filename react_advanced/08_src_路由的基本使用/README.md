# React路由
1. SPA的理解(单页面;多组件)
- 单页面应用
- 整个应用只有一个完整的页面
- 点击页面中的链接`不会`刷新页面,只会做页面的局部刷新
- 数据都需要通过ajax请求获取,并在前端异步展现

2. 路由的理解(前端路由其实就是靠浏览器当中的路径;路由其实没有拿到前面的东西)
- 一个路由就是一个映射关系
- key为路径,value可能是function[后端路由]或component

3. 路由分类
- 后端路由：
    - 理解： value是function, 用来处理客户端提交的请求。
    - 注册路由： router.get(path, function(req, res))
    - 工作过程：当node接收到一个请求时, 根据请求路径找到匹配的路由, 调用路由中的函数来处理请求, 返回响应数据
- 前端路由：
    - 浏览器端路由，value是component，用于展示页面内容。
    - 注册路由: <Route path="/test" component={Test}>
    - 工作过程：当浏览器的path变为/test时, 当前路由组件就会变为Test组件

4. 前端路由的原理(靠着浏览器的history来进行路由跳转)

5. react-router-dom(专门给web人员使用)的理解
- react的一个插件库
- 专门用来实现一个SPA应用
- 基于react的项目基本都会用到此库

6. 印记中文(推荐)

7. react router for web
- 下载：npm i react-router-dom
- 此处需要下载：npm i react-router-dom@5

8. 书写路由的步骤
- 区分导航区和展示区
- 步骤：点击导航链接引起路径变化； 路径的变化被路由器监测到，进行匹配组件然后展示
- **单页面，多组件**

9. html文件抽取成组件

10. 使用ctrl+/ 来进行注释

11. 路由跳转
- 原生html中，靠<a>跳转不同的页面
- 在React中靠路由链接实现切换组件--编写路由链接

12. 注册路由
- 是自结束标签

13. 路由的最基本使用;在最外面包裹BrowserRouter
- 整个路由用一个路由器扩起来才行
- 在index.js中全部包裹起来才行
```
ReactDOM.render(
	<BrowserRouter>
		<App />
	</BrowserRouter>,
	document.getElementById('root')
)
```

14. 根据路由地址进行相关跳转操作
```
{/* 注册路由 */}
<Route path="/about" component={About} />
<Route path="/home" component={Home} />
```

15. **总结:路由的基本使用
    1.明确好界面中的导航区、展示区
    2.导航区的a标签改为Link标签(通过Link标签来实现组件的切换操作)
    ```
    <Link to="/xxxxx">Demo</Link>
    ```
    3.展示区写Route标签进行路径的匹配
    ```
    <Route path='/xxxx' component={Demo}/>
    ```
    4.**<App>的最外侧包裹了一个<BrowserRouter>或<HashRouter>**


