# Linux 代码片段

```shell
# 输出并执行命令
cs (){
    echo $1
    eval $1
}

# 举例

cs 'mkdir 1'
```

```shell
# shell 判断命令是否存在异常退出返回 1 返回码 （目前有点问题）

isExist (){
    if ! [ -x "$(command -V $1)" ]; then
     echo 'Error: '$1' is not installed.' >&2
     exit 1
    fi
}

# 举例
isExist 'git'
```

