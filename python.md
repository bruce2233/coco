# conda

```bash
conda create -n your_env_name
#如无法在D:\anaconda\envs下创建环境请修改文件夹权限

conda remove -n your_env_name
#强烈建议创建一个新的文件夹并更改用户权限
code ~/.condarc
# channels:
#   - defaults
# show_channel_urls: true
# default_channels:
#   - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main
#   - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/r
#   - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/msys2
# custom_channels:
#   conda-forge: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
#   msys2: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
#   bioconda: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
#   menpo: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
#   pytorch: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
#   pytorch-lts: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
#   simpleitk: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
conda clean -i
#清除索引
```

## pip
pip config edit --editor vim
pip cache list

## import
sys.path会添加python文件的所在的目录, 而不会添加$pwd
python会检查sys.path中内容
绝对路径引用的不是文件系统的路径, 而是python包的路径. 
解决办法1: PYTHONPATH=$(pwd) + cmd, argument must be the first position instead of 'cmd + PYTHONPATH=$(pwd)' 
解决方法2: 在导入包之前sys.path.append(os.getcwd())

##  .py文件 jupyter 支持
'''# %%''' 作为分隔符

## VSCode 调试
1. cwd: ${workspaceFolder}/your-project
2. program: (cwd+)file_path
3. args: ["",""......]
