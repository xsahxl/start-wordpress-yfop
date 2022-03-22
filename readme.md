# WordPress 框架

> 快速部署和体验Serverless架构下的WordPress项目

- [WordPress 框架](#wordpress-框架)
  - [体验前准备](#体验前准备)
  - [代码与预览](#代码与预览)
  - [快速部署和体验](#快速部署和体验)
    - [在线快速体验](#在线快速体验)
    - [在本地部署体验](#在本地部署体验)
  - [项目使用注意事项](#项目使用注意事项)
  - [应用详情](#应用详情)

## 体验前准备

该应用案例，需要您开通:

- [阿里云函数计算](https://fcnext.console.aliyun.com/) 产品；并建议您当前的账号有一下权限存在`FCDefaultRole`。
- [阿里云文件存储](https://nasnext.console.aliyun.com/) 产品

## 代码与预览

- [:octocat: 源代码](https://github.com/devsapp/start-web-framework/tree/master/web-framework/php/wordpress/src)
- [:earth_africa: 效果预览](https://img.alicdn.com/imgextra/i4/O1CN01SIbofO1QhFdtCN6IB_!!6000000002007-2-tps-3316-1890.png)

## 快速部署和体验
### 在线快速体验

- 通过阿里云 **Serverless 应用中心**： 可以点击 [【🚀 部署】](https://fcnext.console.aliyun.com/applications/create?template=start-wordpress) ，按照引导填入参数，快速进行部署和体验。

### 在本地部署体验

1. 下载安装 Serverless Devs：`npm install @serverless-devs/s` 
    > 详细文档可以参考 [Serverless Devs 安装文档](https://github.com/Serverless-Devs/Serverless-Devs/blob/master/docs/zh/install.md)
2. 配置密钥信息：`s config add`
    > 详细文档可以参考 [阿里云密钥配置文档](https://github.com/devsapp/fc/blob/main/docs/zh/config.md)
3. 初始化项目：`s init start-wordpress -d start-wordpress`
4. 进入项目并部署：`cd start-wordpress && s deploy`

> 在本地使用该项目时，不仅可以部署，还可以进行更多的操作，例如查看日志，查看指标，进行多种模式的调试等，这些操作详情可以参考[函数计算组件命令文档](https://github.com/devsapp/fc#%E6%96%87%E6%A1%A3%E7%9B%B8%E5%85%B3) ;

## 项目使用注意事项

1. 项目Yaml中，声明了`actions`， 其对应的命令作用是初始化生成一个 NAS（多次执行， 会复用这个 default 生成的NAS）， 并且将 wordpress 工程上传到 NAS，执行函数的时候， nginx 配置 `root /mnt/auto/wordpress;` 指定了 web 的目录在 NAS 上。
2. 该示例中的 WordPress 默认使用 sqlite 数据库 (位于 NAS)

## 应用详情

本项目是将世界上最流行的 web 框架 wordpress 部署到阿里云 Serverless 平台（函数计算 FC）。

通过 Serverless Devs 开发者工具，您只需要几步，就可以体验 Serverless 架构，带来的降本提效的技术红利。

部署完成之后，您可以看到系统返回给您的案例地址，例如：

![图片alt](https://img.alicdn.com/imgextra/i4/O1CN01G8flYd1TccU270V0U_!!6000000002403-2-tps-2532-1596.png)

此时，打开案例地址，就可以进入 wordpress 配置页面：

![图片alt](https://img.alicdn.com/imgextra/i4/O1CN01SIbofO1QhFdtCN6IB_!!6000000002007-2-tps-3316-1890.png)

原理详情图:
![](https://img.alicdn.com/imgextra/i3/O1CN01HWMxXV25nZLpuRuop_!!6000000007571-2-tps-1887-1017.png)

-----

> - Serverless Devs 项目：https://www.github.com/serverless-devs/serverless-devs   
> - Serverless Devs 文档：https://www.github.com/serverless-devs/docs   
> - Serverless Devs 钉钉交流群：33947367    