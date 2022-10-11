# kubeconfig-community

## 项目功能

​	通过向本项目提交pr，实现kubeconfig的自动生成，并通过邮件进行分发。

## 项目处理流程

1.用户A需要fork本仓库，在对应社区下的文件夹创建yaml文件

+ yaml文件名称规范为：服务名+用户+时间，例如以下内容：

  ~~~bash
  service_username_20221011
  ~~~

+ yaml文件内容参考doc/service_username_20221011.yaml文件

  ~~~bash
  ServiceName: os-infra  # 申请kubeconfig的服务名称，服务名称模板见：doc/ServiceName.txt
  UserName: zhuchao      # 用户
  Role: admin/developer/viewer # 申请角色，admin为拥有所有限制，developer为开发者权限， viewer只能查看日志 
  TimeLimit: 7       # 时间限制，单位：天
  ~~~

2.用户A需要向本仓库提交pr请求， 经管理员审核后即可合入， 合入后即向github绑定的邮箱发送邮件，而申请的kubeconfig文件见邮件附件。

