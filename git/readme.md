# 查看git代理状态
```
git config --global --get http.proxy
```
# 设置Http代理
```
git config --global http.proxy http://127.0.0.1:10809
git config --global https.proxy https://127.0.0.1:10809
```
# 设置socks代理
```
git config --global http.proxy 'socks5://127.0.0.1:10808'
git config --global https.proxy 'socks5://127.0.0.1:10808'
```

# 解除代理
```
git config --global --unset http.proxy
git config --global --unset https.proxy
```
# 删除commit-1
```
git log # 查看commit 历史
git reset --hard HEAD^ # 回滚到上次提交
git reset --hard xxxxx  # 回滚到xxxxx提交
git push origin master -f # 提交删除操作
```
# 删除commit-2
```
git log # 查看commit 历史
git rebase -i xxxxxx # xxxxx为目标commit的前一个commit
然后drop掉目标commit
git push origin master -f # 提交删除操作
```
