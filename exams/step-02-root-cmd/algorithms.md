# Algorithms Examination

## Part 1 — Stack / LIFO

### 题目 1

为什么：

```go
defer fmt.Println(1)
defer fmt.Println(2)
defer fmt.Println(3)
```

会输出：

```txt
3
2
1
```

请从“栈（Stack）”的角度解释。

---

### 题目 2

请自己实现一个：

```txt
Stack
```

要求支持：

- Push
- Pop
- Peek
- IsEmpty

语言不限（推荐 Go）。

---

## Part 2 — Dependency Order

### 题目 3

下面这些模块存在依赖：

```txt
config
↓
db
↓
app
↓
ui
```

请回答：

1. 为什么这是一个有向依赖关系？
2. 为什么启动顺序不能乱？
3. 这种问题在算法里更接近什么模型？

---

### 题目 4

什么是“拓扑排序（Topological Sort）”？

请尝试把 Crush 的启动流程和拓扑排序联系起来。

---

## Part 3 — Event Loop

### 题目 5

Bubble Tea 的：

```txt
Update -> View -> Wait next event
```

循环，本质上属于什么类型的系统？

请尝试类比：

- GUI
- 游戏循环
- Web Server

---

### 题目 6

假设你要实现一个最简单的 TUI event loop：

```txt
读取输入
更新状态
重新渲染
```

请写出伪代码。
