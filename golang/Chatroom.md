# 项目chatroom

## 学习了Tcp协议的调用

1：流程

```Go
服务器
ln,err:=net.Listen("tcp",":8088")
if err!=nil{
    fmt.Printf("Listen failed: %v",err)
    os.Exit(-1)
}
defer ln.Close()
conn,err:=ln.Accept()
if err!=nil{
    fmt.Printf("Accept failed: %v",err)
    os.Exit(-1)
}
defer conn.Close()
客户端
conn,err:=Dial("tcp",":8088")
if err!=nil{
    fmt.Printf("Dial failed： %v",err)
}

