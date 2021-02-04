# 切片 slice

切片是引用类型 , 不支持直接比较, 只能和 nil比较

```go
	var a1 []int                    //定义切片 没有长度的数字就是 切片
	var a2 []string                 //定义切片 没有长度的数字就是 切片

	fmt.Println(a1 == nil)          //true
	fmt.Println(a2 == nil)          //true
	fmt.Println(a1)                 //[]

	a1 = []int{1, 2, 3, 4, 5}       //初始化切片
	a2 = []string{"张三", "李四", "王五"} //初始化切片

	fmt.Println(a1 == nil)          //false
	fmt.Println(a2 == nil)          //false


//由数组得到切片
	array1 := [5]int{1, 2, 3, 4, 5}
	slice1 := array1[0:4]//从哪里开始 取几位
	fmt.Println(slice1)				//[1 2 3 4]
	fmt.Printf("%T\n", slice1) //[]int
```

