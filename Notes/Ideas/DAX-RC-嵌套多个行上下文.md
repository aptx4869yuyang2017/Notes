---
up:
  - "[[PowerBI DAX 概念 Concept]]"
related: 
created: 2025-01-19
tags: 
---
#### 嵌套多个表的行上下文

^7ceb87

![600](https://s1.vika.cn/space/2024/03/21/a20bd43b93344daaa6d2471c496c5635)


- 如果针对同一张表，新创建的行上下文会隐藏旧的行上下文
- 如果存在多个表，那么多个行上下文可以同时存在 
	- #todo 为了证明三个行上下文同时存在，得测试一下一个场景：==一个 Category 对应两个相同的 Product==
	- 这个三因子乘法，引用了三个表，激活了三个行上下文
	- 扫描行数太多会有性能问题，更快更容易理解的方案是使用 Related 获取1端表的信息 #domain/powerbi/performance #TODO **对比两种写法的执行计划**
	