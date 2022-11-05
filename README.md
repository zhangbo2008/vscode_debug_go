# vscode_debug_go



2022-11-05,12点06


继续vscode+go

vscode remote-wsl 调试golang没反应
	一次比较无语的浪费了挺长时间的经历，用vscode remote-wsl 插件调试wsl里面的golang程序时，没反应，单步调试的那些按钮都是灰的【这里没有截图，因为解决完问题才想起来记录…】
	去网上差了好多资料都告诉我远程调试要配置debugger的配置文件，添加remote的ip地址啥的，还有要安装dlv，搞了半天也没搞成功，然后偶然间看到一个评论说wsl2才支持远程调试…就把wsl去升级了一下，贼简单，然后就成功了…
	————————————————
	版权声明：本文为CSDN博主「NJU_lemon」的原创文章，遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接及本声明。
	原文链接：https://blog.csdn.net/qq_39618369/article/details/120773510
	经过我实验确实是这样的. wsl 之后vscode才可以调试go代码!!!!!!!!!

wsl -l -v

wsl --set-version Ubuntu-18.04 2





	在网上找到一种解决方式是：
	管理员权限打开Powershell，输入如下命令:

	netsh winsock reset



iris+go

用vscode+wsl2运行go #注意wsl不能运行go.必须2才行.



    go env -w GOPROXY=https://goproxy.cn,direct

    mk iris_go
    cd iris_go
    go mod init iris_go
    go mod tidy  #这个句子每次更改库包之后需要运行一下.
    go get github.com/kataras/iris/v12@latest

