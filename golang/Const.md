# 常量

Go 的常量定义可以限定常量类型，但不是必需的。如果定义常量时没有指定类型，那么该常量就是无类型常量，也叫字面常量。 
例子： 1:

```Go

1：
const limit = 512
const top uint16 = 1421
const Pi float64 = 3.1415926
const x,y int = 1,3 //多重赋值
2：
const (
    Cyan = 0
    Black = 1
    White = 2
)
3：iota的使用
const (
    a = iota  //a == 0
    b = iota  //b ==1
    c = iota  //c == 2
)
const d = iota //d==0,因为const的出现，iota被重置为0

```
