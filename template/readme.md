[![npm version](https://img.shields.io/npm/v/ucloud-ko-fileupload.svg)](https://www.npmjs.com/package/ucloud-ko-fileupload)
[![license](https://img.shields.io/npm/l/ucloud-ko-fileupload.svg)](https://www.npmjs.com/package/ucloud-ko-fileupload)
[![Build Status](https://api.travis-ci.org/yonyouyc/ucloud-ko-fileupload.png?branch=master)](https://api.travis-ci.org/yonyouyc/ucloud-ko-fileupload.png?branch=master)
# 附件上传下载统一组件

对所有附件组件进行了统一改造，支持es6 import，requirejs两种方式

## 如何使用

### 1.通过es6 import 引入

1.1安装依赖
```
npm install --save-dev ucloud-ko-fileupload

```
1.2页面引入

```
import 'ucloud-ko-fileupload/dist/index.css'
import 'ucloud-ko-fileupload'
```
1.3html页面使用
```
<ko-fileupload 
    params="
        id:id,
        groupname:'mygroupname'">
</ko-fileupload>

```
1.4注意事项

如果是ko是通过script标签中引入的方式需要在webpack.config中配置，
```
externals:{
    knockout: 'ko'
}
```
### 2.requirejs
1.1main.js引入依赖
```
// window.ctx.cdn指https://yc.yonyoucloud.com/cpu-cdn 或 http://yc.yonyou.com/cpu-cdn
ufileupload:window.ctx.cdn+'/js/ucloud/ufileupload/0.0.3/ucloud-ko-fileupload'
```
1.2页面引入依赖
```
define(['ufileupload'], function () {
    // your code
})
```
1.3html页面使用
```
<ko-fileupload 
    params="
        id:id,
        groupname:'mygroupname'">
</ko-fileupload>
```


通用备注：本组件依赖https://yc.yonyoucloud.com/cpu-cdn上的一些资源文件