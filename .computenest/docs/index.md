# 服务模版说明文档

## 服务说明

本文介绍基SpringBoot+软件包的ecs集群版服务快速上手流程，本示例对应的Git仓库地址：[springboot-scaling-ecs-demo](https://github.com/aliyun-computenest/springboot-scaling-ecs-demo)。

本示例会自动的构建计算巢服务，具体的服务构建流程为：
1. 上传文件并构建计算巢文件部署物
2. 创建计算巢服务并关联文件部署物

创建过程大约持续1分钟，当服务变成待提交后构建成功。

## 服务架构

本部署架构为集群ecs部署，通过eip 8080端口访问，配备负载均衡和弹性伸缩组，具体如图所示:
<img src="architecture.png" width="1500" height="700" align="bottom"/>

## 服务构建计费说明

测试本服务构建无需任何费用，创建服务实例涉及的费用参考服务实例计费说明。

### 部署步骤

0. 部署链接
 ![image.png](1.png)
1. 单击部署链接，进入服务实例部署界面，根据界面提示，填写参数完成部署。
 ![image.png](2.png)
2. 参数填写完成后可以看到对应询价明细，确认参数后点击**下一步：确认订单**。
 ![image.png](3.png)
3. 确认订单完成后同意服务协议并点击**立即创建**，进入部署阶段。
    ![image.png](4.png)
    ![image.png](5.png)
4. 等待部署完成后就可以开始使用服务，进入服务实例详情点击visitUrl。
    ![image.png](6.png)
5. 部署结果
    ![image.png](7.png)
6. 弹性扩缩容
    ![image.png](8.png)
    ![image.png](9.png)
    ![image.png](10.png)
    ![image.png](11.png)
   等待结束执行后可以看到资源中新增了3台ecs，完成了扩缩容。
    ![image.png](12.png)

## 服务详细说明

基础服务说明请参考SpringBoot软件包部署单机版，本文在此基础上新增了slb和ess的配置。

1. slb给ecs配置负载均衡并绑定对应的eip。
2. ess配置增加弹性伸缩能力可以随时扩缩容。


## 服务配置

[创建代运维服务完成实例运维](https://help.aliyun.com/zh/compute-nest/create-a-hosted-operations-and-maintenance-service?spm=a2c4g.11186623.0.i24#task-2167552])

[创建包含变配功能的服务](https://help.aliyun.com/zh/compute-nest/use-cases/create-a-service-that-supports-specification-changes-and-change-the-specifications-of-a-service-instance?spm=a2c4g.11186623.0.i3])

[创建包含服务升级功能的服务](https://help.aliyun.com/zh/compute-nest/upgrade-a-service-instance?spm=a2c4g.11186623.0.i17#task-2236803)

## 服务交付

[自定义服务架构图](https://help.aliyun.com/zh/compute-nest/customize-a-service-architecture?spm=a2c4g.11186623.0.0.56e736bfyUdlFm])

[服务文档上线流程](https://help.aliyun.com/zh/compute-nest/use-cases/publish-documents-to-compute-nest?spm=a2c4g.313309.0.i0])

[将服务上架云市场并上到云市场售卖](https://help.aliyun.com/zh/compute-nest/publish-a-service-to-alibaba-cloud-marketplace?spm=a2c4g.11186623.0.i7])

## 其他

[实例代码源地址](https://atomgit.com/flow-example/spring-boot)

[软件包package.tgz构建流程参考](https://help.aliyun.com/document_detail/153848.html)
