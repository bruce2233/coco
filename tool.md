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

```bash 
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
# ":-" means using ZSH_CUSTOM if it's not null, else using the after.
# check details by `man bash and search ${parameter:-word}`
```



# git

`git clone xxx.git abc #do not create xxx directory`
