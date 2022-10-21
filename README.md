# kubeconfig-interact

## 功能

​	通过向本项目提交pr，实现kubeconfig的自动生成，并通过邮件进行分发。

## 申请流程

1.用户A需要fork本仓库，在对应社区下的文件夹创建yaml文件

+ yaml文件名称规范为：日期+用户+服务名，例如以下内容：

  ~~~bash
  20221011_zhu_infra-scan-tools
  ~~~

+ yaml文件内容参考模板文件： doc/20221011_zhu_infra-scan-tools.yaml文件，详细见：[模板文件](https://github.com/Open-Infra-Ops/kubeconfig-interact/blob/main/doc/20221011_zhu_infra-scan-tools.yaml)

  ~~~bash
  ServiceName: infra-scan-tools  # 申请kubeconfig的服务名称，服务名称模板见：doc/ServiceName.txt
  UserName: zhuchao99    # 用户名称；限制：由数字、小写字母组成，不能含有特殊字符，最长长度为20，不能包含大写字母。
  Role: admin/developer/viewer # 申请角色；admin为拥有所有权限，developer为开发者权限，进入容器权限， viewer只能查看日志 
  TimeLimit: 7       # 时间限制；单位：天；限制：必须为数字类型，不能小于0。
  ~~~

+ ServiceName详细见： [ServiceName](https://github.com/Open-Infra-Ops/kubeconfig-interact/blob/main/doc/ServiceName.txt)

2.用户需要向本仓库提交pr请求， 经管理员审核后即可合入， 合入后即向github绑定的邮箱发送邮件，而申请的kubeconfig文件见邮件附件。

## 注意事项

1.发起PR请求，默认为允许本项目及其服务使用github绑定的邮箱作为接受邮箱。

2.PR请求中的文件只能新增，不能修改， 详细解释：不能对之前创建的还在有效期的文件进行修改。

3.用户对相同的服务提交两次pr， 只能以最后发送的kubeconfig有效。详细解释：用户提交一次PR后，已经申请对该服务的权限，并在有效期内再次对相同的服务提交PR， 则新创建的kubeconfig有效，而之前的生成的kubeconfig失效。

4.允许用户一次提交PR中包含对多个服务的权限申请。

