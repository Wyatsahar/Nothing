# 常量 const

iota 是 常量内行的计数

```go
const(
	a1 = 1
  a2
  a3
  a4 = iota
  a5
)

fmt.Println(a1,a2,a3,a4,a5)   //1 1 1 3 4
```

