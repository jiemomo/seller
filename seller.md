*快速创建vue项目步骤：*
- vue create project-name
- cd project-name
- npm run serve

*vue-cli3安装*
- npm insatll -g @vue/cli(已经安装好node，本次安装版本是10.13.1会自动安装npm6.4.x)

*图标字体的创建*
- 推荐：https://icomoon.io/app/#/select/font

*安装scss插件*
1. 使用到stylus这个css预处理器而不用其他预处理器的原因是：stylus来自node.js社区，与js关系密切，所以基于vue.js的开发，选择了stylus。
配置stylus环境：
- npm install stylus
- npm init webpack stylus
 (vue cli3以上的版本，如果是cli3版本，会提示： Command vue init requires a global addon to be installed.Please run npm install -g @vue/cli-init and try again.在新版中推荐使用  vue create)
- npm install
- npm install stylus --save-dev
- npm install stylus-loader --save-dev

*vue-resource 和 vue-axios*

1. 在vue2.0时，vue-resource已经不在更新，推荐使用axios。基于Promise的http请求客户端，可同时在浏览器和node.js中使用。
功能特性：
- 在浏览器中发送xmlhttprequest请求
- 在node.js中发送http请求
- 支持promise  api
- 拦截请求和响应请求
- 转换请求和响应数据
- 取消请求
- 自动转换JSON数据
- 客户端支持保护免受CSRF/XSRF攻击

2. 安装vue-axios：(此时用的是2.1.4版本)
- npm i vue-axios
- npm install --save axios vue-axios


*关于css样式优化:*
1. 影响布局的样式： display、position先写在前面;触发reflow,即影响它重绘的（比如width、height等）不被继承的css属性在布局之后，最后可被继承的字体颜色放在最后。

设计稿是根据iPhone6进行设计，设备像素是375，物理像素是750，dpr是2。

在浏览器中会发现一些自动添加的css兼容性代码，这是vue-loader中的postcss文件添加的。

实现手机端1px的边框主要用到：伪类和缩放。



