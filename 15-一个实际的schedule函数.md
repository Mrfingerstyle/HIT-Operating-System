### 一个schedule函数
---
- Linux 0.11 schedule()
- 求最大的counter
- 跳转去执行
---
- counter 表示 时间片 优先级
- counter承担了时间片的作用
- counter代表的优先级可以动态调整
- 阻塞的进程在就绪以后优先级高于非阻塞进程
- IO 正是前台进程的特征
---
- counter作用整理
> 保证了响应时间的界
> 经过IO以后 counter变大 IO时间越长 counter越大 
> 照顾了IO进程 变相的照顾了前台进程
> 后台进程一直按照counter运转 近似JSF调度
> 每个进程只用维护一个counter 简洁高效
> 简单的算法折中了大多数任务的需求
