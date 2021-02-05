# map

​	make() 初始化 map



```go
	bb := make(map[string]int) //初始化map
	bb["张三"] = 18
	bb["李四"] = 19
	bb["王五"] = 20
	fmt.Println(bb)

	//遍历
	for k := range bb {
		fmt.Println(k) // 遍历key
	}

	for _, value := range bb {
		fmt.Println(value) // 遍历value
	}
	fmt.Printf("%T", bb)
	//删除
	delete(bb, "李四")
	fmt.Println(bb)

	//元素为map类型的slice
	var slice1 = make([]map[string]int, 5) //初始化切片
	slice1[0] = make(map[string]int, 1)    //初始化map
	slice1[0]["张三"] = 1
	fmt.Println(slice1)  //[map[张三:1] map[] map[] map[] map[]]

 //元素为slice类型的map
	var map1 = make(map[string][]int, 1)
	map1["first"] = make([]int, 0, 1)
	// map1["fitst"][0] = 6    //这个是错误的 吸取教训
	map1["first"] = append(map1["first"], 6) //slice 用append 增加
	fmt.Println(map1) //map[first:[6]]
	map1["first"][0] = 999
	fmt.Println(map1)	// map[first:[999]]

```



