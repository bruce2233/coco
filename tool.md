#less 
`j` next line

`k` previous line

`d` next window

`b` previous window

`/pattern` search pattern

`n` next search result

`N` previous search result

# git

git config --global user.name "I am xxx"
git config --global user.email "123456xxx@gmail.com"

# zsh

## config in a fresh machine
```bash
sudo apt-get install zsh

sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
# ":-" means using ZSH_CUSTOM if it's not null, else using the after.
# check details by `man bash and search ${parameter:-word}`

vim ~/.zshrc
#replace ZSH_THEME="powerlevel10k/powerlevel10k"

source ~/.zshrc

git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting 

vim ~/.zshrc

# plugins=(
#     # other plugins...
#     z
#     zsh-syntax-highlighting  # 插件之间使用空行
# )

source ~/.zshrc

# if you need reinstall, run p10k configure
    
# p10k configure
```
```
reference link: https://zhuanlan.zhihu.com/p/441676276

```bash 
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k




# git

`git clone xxx.git abc #do not create xxx directory`
`git push -f origin HEAD~1:main` //回退remote 

`git log `

```bash
distribution=$(. /etc/os-release;echo $ID$VERSION_ID)
# ; is a separator

```


# wsl
`echo [boot]\nsystemd=true >> /etc/wsl.conf`
`#for Windows WSL: ubuntu config --default-user your-not-root-username`

```bash
echo "export PATH=$PATH:/usr/lib/wsl/lib" >> ~/.zshrc #for nvidia-smi
echo "export PATH=$PATH:/usr/local/cuda-12.1/bin" >> ~/.zshrc #for nvcc
#link: https://developer.nvidia.com/cuda-downloads?target_os=Linux&target_arch=x86_64&Distribution=WSL-Ubuntu&target_version=2.0&target_type=deb_local
```


# curl
```bash
curl -fsSL
# -f --fail : fail silently to avoid outputting html error infomation
# -s --silent
# -S --show-error
# -L --location : get redirected html
```
# docker 
docker run -it --runtime nvidia nvidia/cuda:12.1.0-devel-ubuntu20.04 /bin/bash
```bash
docker run --gpus all \
-it \
-v /mnt/g/github/consistency_models:/app/cm \
--network host \
--rm \
nvcr.io/nvidia/pytorch:23.03-py3 bash

cp /etc/apt/sources.list /etc/apt/sources.list.bak

echo -e "deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal main restricted universe multiverse\ndeb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal-updates main restricted universe multiverse\ndeb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal-backports main restricted universe multiverse\ndeb http://security.ubuntu.com/ubuntu/ focal-security main restricted universe multiverse" > /etc/apt/sources.list


#docker run -it  --name infallible_bassi nvidia/cuda:11.8.0-devel-ubuntu20.04 /bin/bash 
docker run -it  --runtime nvidia --name infallible_bassi pytorch/pytorch:2.0.0-cuda11.7-cudnn8-devel  /bin/bash

docker cp /etc/apt/sources.list   infallible_bassi:/etc/apt/sources.list && docker cp download/Miniconda3-py310_23.1.0-1-Linux-x86_64.sh infallible_bassi:/root/

pypi-server run  ~/pspkgs


apt update && apt install -y proxychains4 vim git libopenmpi-dev g++ wget

vim /etc/proxychains4.conf #socks5 172.19.0.1 10810

cd /root && bash Miniconda3-py310_23.1.0-1-Linux-x86_64.sh && su -


proxychains pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118 \
--extra-index-url http://172.19.3.206:8080/simple \
--trusted-host 172.19.3.206

wget https://download.open-mpi.org/release/open-mpi/v4.0/openmpi-4.0.4.tar.gz
tar -zxvf openmpi-4.0.4.tar.gz
cd openmpi-4.0.4
./configure
proxychains git clone https://github.com/bruce2233/consistency_models.git

cd consistency_models && proxychains pip install -e .
```

# docker rm infallible_bassi
ssh-keygen -f "/home/bruce/.ssh/known_hosts" -R "45.63.53.170"

# less
'/': search
n: next search result 