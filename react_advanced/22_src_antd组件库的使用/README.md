## antd组件库的使用
- material-ui 国外
- ant-design 国内蚂蚁金服
    - 安装；npm add antd
    - antd也有很多子库， 不同的库实现不同的功能
    - 来点复杂的：日期选择器，想要实现一些别的功能，查看API即可
- 适用：搭建成熟的后台管理系统，系统比较成型
- vantUI适用于移动端 for Vue
- import 'antd/dist/antd.css' 此处不合理，因为这个文件太大了，我们最好做到按需引入样式

## 总结：antd的按需引入+自定主题
	1.安装依赖：yarn add react-app-rewired customize-cra babel-plugin-import less less-loader
	2.修改package.json
		....
			"scripts": {
				"start": "react-app-rewired start",
				"build": "react-app-rewired build",
				"test": "react-app-rewired test",
				"eject": "react-scripts eject"
			},
		....
	3.根目录下创建config-overrides.js  + 自己加的：yarn add babel-plugin-import 
		//配置具体的修改规则
		const { override, fixBabelImports,addLessLoader} = require('customize-cra');
		module.exports = override(
			fixBabelImports('import', {
				libraryName: 'antd',
				libraryDirectory: 'es',
				style: true,
			}),
			addLessLoader({
                // 这里有个坑，配置目前已经被修改了，使用新属性来配置
				lessOptions:{
					javascriptEnabled: true,
					modifyVars: { '@primary-color': 'green' },
				}
			}),
		);
	4.备注：不用在组件里亲自引入样式了，即：import 'antd/dist/antd.css'应该删掉

### 自定义主题
- antd(less) => css 
- 我们要用的就是修改底层的less文件，

做法：
1. yarn add less less-loader
2. 配置文件其实就是上述配置文件的最终版本
