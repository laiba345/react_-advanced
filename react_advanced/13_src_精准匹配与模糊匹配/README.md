# 精准匹配与模糊匹配
- 精准匹配要求完完全全一样的精准匹配，
    - 在注册路由的时候加上exact属性,默认值为true，
    ```
    {/* 注册路由 */}
    <Switch>
        <Route exact path="/about" component={About}/>
        <Route exact path="/home" component={Home}/>
    </Switch>
    ```
- **严格匹配不要轻易开启**，如果是路径跳转出错，可以考虑是否是严格匹配导致的问题

## 路由的严格匹配与模糊匹配总结
1.默认使用的是模糊匹配（简单记：【输入的路径】必须包含要【匹配的路径】，且顺序要一致）
2.开启严格匹配：<Route exact={true} path="/about" component={About}/>
3.严格匹配不要随便开启，需要再开，有些时候开启会导致无法继续匹配二级路由



