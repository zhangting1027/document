# git 文档

## 常见指令

`git init` 初始化git仓库（新建本地仓库）

`git clone` 将已有的线上仓库拉下来

`git add .` 将最近的修改全部缓存

`git commit -m "updated information"` 创建一次提交

`git pull` 将该分支的最新代码拉下来并于本地代码合并，请注意该指令需要将本地代码缓存后才能使用 即`git add .` => `git commit -m "xxx"` => `git pull`

`git push` 提交代码至线上仓库

`git checkout xxx` 切换至xxx分支 

`git checkout -b xxx` 创建并切换到xxx分支

## 解决冲突

### 多人合作时：

`git push` 提示仓库有最新代码，要先执行`git pull`

`git pull` 后如果有代码冲突：

和你需要合并代码的小伙伴确认后，然后修改冲突的代码

创建一个以 **人名_日期_版本号_conflict** 分支  比如：`git checkout -b zhuim_20221013_01_conflict`

再次执行 `git add .` => `git commit -m "xxx"` => `git push`

到github上的对应仓库执行 **pull request**

### 单人：

`git push` 提示仓库有最新代码，要先执行`git pull`

`git pull` 后如果有代码冲突：

修改冲突的代码

再次执行 `git add .` => `git commit -m "xxx"` => `git push`