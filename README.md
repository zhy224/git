# git
# Linux 使用 git 上传代码到 GitHub
# --------------------------生成rsa--------------------------
git config --global user.name 'zhy224'
git config --global user.email '412724740@exp.com'
ssh-keygen -t rsa -C “412724740@exp.com”
# ----------添加id_rsa.pub内容到GitHub账号ssh中----------
sudo vim ~/.ssh/id_rsa.pub
# ---------查看连接情况------------
ssh -v git@github.com
# ---------创建本地仓库------------
git init
git add .
git commit  -m 'comment'
# ------------------------创建远程连接----------------------
git remote add origin https://github.com/zhy224/xxx.git
# 将本地仓库更新到远程连接
git push origin master
# 输入github账号密码
zhy224
zy04110224
# ------------------------删除本地分支---------------------
# 查看本地分支
git branch
# 删除本地分支
git branch -d 分支名称
# ------------------------删除远程分支---------------------
# 查看所有的分支
git branch -a
# 删除远程分支，我们需要先把分支切换到master
git checkout master
# 删除远程分支
git push origin --delete 远程分支名称
