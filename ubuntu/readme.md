# 修改path
## 临时修改
```
export PATH=/usr/local/bin:$PATH
```
## 永久修改(当前用户)
```bash
vim ~/.bashrc 
//在最后一行添上：(i)
export PATH=$PATH:xxx/xxx/xx
//关闭保存（esc->:wq），执行以下命令
source ~/.bashrc
```
## 永久修改(全部用户)
```bash
vim /etc/profile
//在最后一行添上：(i)
export PATH=$PATH:xxx/xxx/xx
//关闭保存（esc->:wq），执行以下命令
source /etc/profile
```

