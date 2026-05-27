# Architecture Examination

## Part 1 — Cobra Command Tree

### 题目 1

设计一个 CLI 命令树：

```txt
myapp
├── run
├── login
├── logs
└── session
```

要求：

1. 定义 root command
2. 注册至少两个 subcommand
3. 添加一个 PersistentFlag
4. 添加一个普通 Flag

---

### 题目 2

解释：

```go
rootCmd.AddCommand(runCmd)
```

在 Cobra 里到底做了什么？

---

## Part 2 — 启动流程设计

### 题目 3

为什么 Crush 的启动顺序是：

```txt
config
↓
db
↓
app
↓
ui
```

而不是反过来？

---

### 题目 4

如果你把：

```go
db.Connect(...)
```

放到：

```go
config.Init(...)
```

之前，会出现什么问题？

---

## Part 3 — 分层与职责

### 题目 5

为什么：

```txt
ui 不应该直接操作数据库
```

请从“分层设计”和“职责边界”角度回答。

---

### 题目 6

解释：

```txt
setupLocalWorkspace
```

和：

```txt
app.New
```

职责上的区别。

---

## Part 4 — 生命周期与清理

### 题目 7

为什么：

```go
defer cleanup()
```

应该在 workspace 创建成功后立刻注册？

---

### 题目 8

解释：

```txt
资源创建
↓
程序运行
↓
cleanup
```

这种生命周期管理模式的意义。
