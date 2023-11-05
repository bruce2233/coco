# Shell

## 执行.sh 文件的方式

1. `. <file>`
2. `./<file>`
3. `source <file>`
4. `sh <file>`

其中：1 和 3是等价的，都是在当前的shell 中执行命令

2和4是等价的，都是创建子shell，并在子shell中执行命令

所以当2、4执行shell文件后，export的环境变量会消失，因为是在子shell中执行，子shell会单向继承父shell的环境变量，而不会反过来

## history 命令

## \ 换行后一定不能有空格jobs -l

## zshell 
keybind for backward or forward word 
```shell
bindkey -M emacs '^[[1;5C' forward-word
bindkey -M emacs '^[[1;5D' backward-word
```
## kill
kill %1 #结束后台session为1的进程(非PID)