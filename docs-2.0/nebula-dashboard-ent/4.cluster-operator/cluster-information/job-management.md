# 集群作业管理

Dashboard 可以管理指定图空间中的作业，包括查看、停止、恢复图空间内的作业，并支持查看单个作业的详情。

!!! note

    如何执行作业，请参见[作业管理](../../../3.ngql-guide/4.job-statements.md)。

## 前提条件

NebulaGraph 集群版本需要为企业版 3.4.0 及以上或 NebulaGraph 社区版 3.3.0 及以上。

## 入口

1. 在 Dashboard 企业版顶部导航栏，单击**集群管理**。
2. 单击目标集群右侧**详情**。
3. 在左侧导航栏，单击**集群信息**->**作业管理**。
4. 选择任意一个在线的 Graph 服务地址，输入登录 NebulaGraph 的账号（非 Dashboard 登录账号）和对应密码。
5. 在左上角选择目标图空间。

## 查看作业

选择图空间后，页面会默认展示所有未过期的作业信息。用户可以通过上方筛选框快速查找作业。方法如下：

- 选择作业状态进行筛选。状态包括`QUEUE`、`RUNNING`、`FINISHED`、`FAILED`、`STOPPED`、`SUCCEEDED`。状态说明请参见[作业管理](../../../3.ngql-guide/4.job-statements.md)。
- 选择时间进行筛选。
- 选择`作业命令`或`作业 ID`筛选。选择后输入要搜索的内容。
- 页面的作业数据默认不自动更新，可以调整**更新频率**让页面自动更新，也可以单击![setup](https://docs-cdn.nebula-graph.com.cn/figures/refresh-220616.png)按钮手动更新。
- 在目标作业右侧的`操作`列单击`详情`，可以查看更多详细信息，包括`任务 ID`、`Host`、`错误码`等。

## 停止作业

在目标作业右侧的`操作`列单击`停止作业`，可以停止未完成的作业，点击后该作业状态变为`STOPPED`。

## 重新执行作业

在目标作业右侧的`操作`列单击`重新执行`，可以重新执行状态为`FAILED`、`STOPPED`的作业，点击后该作业状态变为`RUNNING`。

!!! note

    - 如果有多个状态为`STOPPED`的`BALANCE DATA`作业，只能重新执行最新的一个。
    - 已完成的作业无法重新执行。
