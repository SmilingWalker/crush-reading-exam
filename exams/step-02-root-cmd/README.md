# Step 02 | root.go 启动流程 Examination

本组题目对应 Crush 源码走读 Step 2：`internal/cmd/root.go`。

重点覆盖：

- Go 包级变量初始化与 `init()`
- Cobra command / flags / subcommands
- `defer` 与资源清理
- `go` goroutine 与后台订阅
- `config -> db -> app -> ui -> program.Run()` 启动链路
- 启动流程中的依赖顺序与分层设计

## 文件说明

```txt
go-syntax.md      Go 语法题
architecture.md   架构与设计理解题
algorithms.md     算法 / 数据结构题
answers.md        参考答案与讲解
```

建议先完成前三个文件，再看 `answers.md`。
