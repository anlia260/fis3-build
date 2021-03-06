# <%=pkg.name%>

*<%=pkg.desc%>*

## 目录结构

```
build                   构建脚本（预留）

map
    - manifest.json     静态资源映射表

mock                    模拟数据
    - server.conf       模拟数据配置（支持rewrite、redirect、proxy）
    - *.json            本地模拟数据

app                     单页应用入口页面
    - *.html

modules                 模块目录
    - lib               工具库包
        - mod1
        - ...
    - conf              配置包
        - *.js
    - coms              功能组件包（业务无关）
        - mod1
        - ...
    - buss              业务组件包（按需加载）
        - mod1
        - ...
    - page              页面包（类似多页模式中的页面，由router控制）
        - mod1
        - ...
    - app               应用入口模块
        - *.js

resource                静态资源目录
    - css               样式资源
    - images            媒体资源（包含图片、视频、动画等）
    - js                静态脚本（使用script方式在页面引入）

partials                代码片段
    - *.html             html代码片段
    
package.json            包说明
README.md               说明文档
.editorconfig           编辑器配置
.gitignore              git忽略配置
LICENSE                 版权声明
```

## 环境要求

*nodejs 6.x*

## 常用命令


*更多命令参见 <a href="http://fis.baidu.com/fis3/docs/api/command.html" target="_blank" title="点击了解更多...">>> fis3 命令行</a>*


### 构建工具安装

```
npm install --only=dev
```

### 开启本地服务

*开启一个node服务器。ctrl+c退出，但服务继续运行在后台*

```
fis3 server start
```

### 开发调试

*预览项目，支持文件watch、浏览器自动刷新*

```
fis3 release -wL
```

### 发布部署

*todo：结合gitlab构建*

```
fis3 release prod -d ./output
```


### 关闭本地服务

```
fis3 server stop
```


