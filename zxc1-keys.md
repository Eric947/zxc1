### 01-项目目录说明：
1. src/
2. budid/  webpack相关代码
3. config/  本地服务器配置
4. .eslintignore  eslist 排除文件
5. .eslinttrc  eslint配置文件

### 02-准备-代码规范-自定义指令-lintfix：
1. 结尾没有;
2. 必须使用全等 ===
3. 不允许出现未使用的变量
4. 不允许出现一行以上空行
5. 在package中添加
    "lintfix": "eslint --ext .js,.vue src --fix",
自动修正代码
6. 在package中添加
    "dev": "webpack-dev-server --inline --progress --config build/webpack.dev.conf.js --open",
>npm run dev 自动打开浏览器
7. 关闭eslint 在build/webpack.base.conf.js中注释掉
       ...(config.dev.useEslint ? [createLintingRule()] : []),

### 03-准备-element-ui:
1. 适用于vue项目-PC端项目
2. 在main.js 引入
3. >npm i element-ui -S  下载
4. 在main.js  import
5 .在main.js  Vue.use(ElementUI);