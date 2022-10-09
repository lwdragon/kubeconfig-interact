# kubeconfig-community

## 项目功能

通过向本项目提交pr，实现kubeconfig的自动生成，并通过邮件进行分发。

## 项目处理流程

1.用户A需要fork本仓库，在对应社区下的文件夹创建yaml文件，

+ yaml文件名称规范为：服务名+用户+时间，例如以下内容：

  ~~~bash
  demo_username_20221009
  ~~~

+ yaml文件内容参考demo_username_20221009.yaml文件

2.用户A需要向本仓库提交pr请求， 需要运维人员进行补充信息（集群，命名空间）、审核后即可合入。

3.合入后服务会向配置中的邮件发送kubeconfig配置的邮件。