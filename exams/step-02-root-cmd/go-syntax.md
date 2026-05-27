# Go Syntax Examination

## Part 1 — init() 与包级变量

### 题目 1

写一个 Go 程序：

要求：

1. 定义一个包级变量 `appName`
2. 在 `init()` 中修改它
3. 在 `main()` 中打印最终值
4. 观察执行顺序

---

### 题目 2

阅读下面代码，写出输出结果，并解释原因：

```go
package main

import "fmt"

var value = 1

func init() {
    value += 2
}

func main() {
    value += 3
    fmt.Println(value)
}
```

---

## Part 2 — defer

### 题目 3

写一个函数：

```go
func demo()
```

要求输出顺序为：

```txt
start
middle
cleanup
```

并使用 `defer` 实现。

---

### 题目 4

解释下面代码为什么会输出 `3 2 1`：

```go
func main() {
    defer fmt.Println(1)
    defer fmt.Println(2)
    defer fmt.Println(3)
}
```

---

## Part 3 — 多返回值与 error

### 题目 5

实现：

```go
func divide(a int, b int) (int, error)
```

要求：

- 正常返回商
- 除数为 0 时返回 error

---

### 题目 6

为什么 Go 项目里大量出现：

```go
if err != nil {
    return err
}
```

请从“Go 的错误处理哲学”角度回答。

---

## Part 4 — goroutine

### 题目 7

解释：

```go
go ws.Subscribe(program)
```

和：

```go
defer cleanup()
```

本质区别是什么？

---

### 题目 8

写一个 goroutine 示例：

要求：

1. 主 goroutine 打印 `main`
2. 后台 goroutine 打印 `worker`
3. 让程序不要过早退出
