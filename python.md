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