# 切片 slice

切片是引用类型 , 都指向了一个底层数组  所有修改元素修改底层数组

不支持直接比较, 只能和 nil比较

切片 未初始化情况  等于 nil



make([]int , 5 ,10)  // [0,0,0,0,0]

copy() // 新开辟内存 存放切片  

len(slice) //查看长度

cap(slice) //查看容量



切片指向了一个底层的数组

切片的长度就是他元素的个数

切片的容量是底层数组从切片的第一个元素到最后一个元素的数量







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
	array1 := [9]int{1, 2, 3, 4, 5, 6, 7, 8, 9}
	slice1 := array1[0:4]      //从哪里开始 从0开始 取几位
	fmt.Println(slice1)        //[1 2 3 4]
	fmt.Printf("%T\n", slice1) //[]int
	slice2 := array1[3:]
	fmt.Printf("len(slice1)=%d cap(slice1)=%d\n", len(slice1), cap(slice1))
	// len(slice1)=4 cap(slice1)=9
	fmt.Printf("len(slice2)=%d cap(slice2)=%d\n", len(slice2), cap(slice2))
	// len(slice2)=6 cap(slice2)=6
	fmt.Println(slice2)
	// [4 5 6 7 8 9]
	slice2[0] = 99
	fmt.Println(array1) //[1 2 3 99 5 6 7 8 9]
	fmt.Println(slice2) //[99 5 6 7 8 9]


	//从切片中删除元素 3  
	a := []int{1, 2, 3, 4, 5, 6, 7, 8, 9}
	a = append(a[:2], a[3:]...)
	fmt.Println(a) //[1 2 4 5 6 7 8 9]


```

