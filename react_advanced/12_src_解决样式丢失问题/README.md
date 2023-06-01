# 解决样式丢失问题
1. 在书写路由路径的时候,在路由路径上加上/atguigu/home等
2. 通过浏览器请求相应的历史,如果请求的东西不存在,会将index.html返回
3. 项目进行打包了以后才会有漂亮的react的logo出现,这才是最关键的

## 总结;解决多级路径刷新页面样式丢失的问题
```
1.public/index.html 中 引入样式时不写 ./ 写 / （常用）
2.public/index.html 中 引入样式时不写 ./ 写 %PUBLIC_URL%(只适用于react框架) （常用）
3.使用HashRouter(很少用,不美观)
```



