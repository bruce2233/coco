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


`distribution=$(. /etc/os-release;echo $ID$VERSION_ID)`
# ; is a sep

# wsl
`echo [boot]\nsystemd=true >> /etc/wsl.conf`