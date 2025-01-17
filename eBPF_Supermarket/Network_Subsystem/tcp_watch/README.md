基于目前已有eBPF小工具，以及linux网络协议栈相关探测点，该项目在主机空间实现以下功能：

- 记录TCP连接层面相关信息
- 记录TCP包层面相关信息
- 从TCP包中提取HTTP1/1.1相关信息
- 暴露HTTP接口提供给Prometheus以进行可视化

项目开发规划：

- [x]   搭建基础开发框架和自动编译管道。
- [x]   根据相关工具代码，设计并实现TCP连接信息的记录
- [x]   根据相关工具代码，设计并实现各个TCP连接发送与接收包信息的记录
- [ ]   更具相关工具代码，设计并实现TCP错误包信息的记录
- [ ]   调查相关资料，实现从TCP包中抽取HTTP信息并记录
- [ ]   讨论与Prometheus的连接方案并实现
- [ ]   设计并添加工具的控制参数，提高工具的可用性
- [ ]   编写相关文档