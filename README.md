创建greet服务

$ mkdir go-zero-greet

$ cd go-zero-greet

$ go mod init go-zero-greet

$ goctl api new greet

$ go mod tidy

接下来我们就可以在greetlogic.go中编写业务代码


启动服务

$ cd greet
$ go run greet.go -f etc/greet-api.yaml

访问服务

$ curl -i -X GET http://localhost:8888/from/you


生成Dockerfile文件
cd ./greet
goctl docker --go greet.go


在项目根目录写docker-composer.yml

