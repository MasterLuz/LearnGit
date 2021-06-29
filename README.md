# LearnGit

> 零碎的知识点

## Log

### git log
git log 默认输出commit hash, author, date, message
| 指令 | 功能 | 
| - | - |
| --oneline | 仅仅输出commit hash的前7个字符和message |
| --stat | 增加文件增删改的统计数据|   
| -p | 增加文件具体的增删改内容|
| --pretty=format:"" | 格式化输出|
| --author="xxx" | 仅输出指定名字的用户| 
| -n | 指定要输出的数量 | 
| --after '10-1-2019'| 仅输出2019年1月10号后的commit信息（注意外国的日期顺序和我们不一致）
| --before '' | 同`--after`,输出某日期前的Commit信息 |
| --merges | 输出merge信息 | 
| --no-merges | 不输出merge信息 |
| --decorate | 显示Branch和tag信息（据说，我没发现啥区别）|
### git show \<hash-code\> 
功能同 `git log -p`, 但是只显示一个commit, 未指定hash-code则表示HEAD
### git shortlog 
| 指令 | 功能 |
| - | - |
| 无 | 根据作者分组输出commit message(其他不输出， 根据作者名排序) |
| -s | 仅输出各个作者commit的数量|
| -n | 输出同无参数，只是输出顺序与其相反|
### git log --pretty=format:""
| 格式 | 内容 |
| - | - |
| %H | hash |
| %h | hash缩写 | 
| %T | 树状hash |
| %t | 树状hash缩写 | 
| %P | 父hash | 
| %p | 父hash缩写 |
| %an | 作者名 | 
| %ae | 作者邮箱 |
| %ad | 日期 |

## 创建删除远程分支
1. `git checkout -b newBranch`, 先在本地创建新分支
1. `git push origin newBranch:newBranch`, 在远程创建同名分支
1. `git push origin --delete newBranch`, 删除远程分支
