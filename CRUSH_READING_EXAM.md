# Crush Reading Examination

这个文件作为源码走读练习的入口，不覆盖仓库已有 README。

每读完一个 part，会新增一组 coding examination，覆盖三类内容：

1. Go 语法与标准写法
2. 源码中出现的设计模式 / 架构概念
3. 基础算法与数据结构练习

## 目录规划

```txt
exams/
  step-02-root-cmd/
    README.md
    go-syntax.md
    architecture.md
    algorithms.md
    answers.md
```

## 做题方式

建议先只看题目，不看 `answers.md`。

每组题目会尽量贴近当次走读内容。比如 Step 2 会围绕：

- `init()` 与包级变量初始化
- Cobra command / flags
- `defer` 与资源清理
- 启动流程编排
- config -> db -> app 的依赖顺序
