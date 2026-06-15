# github本地上传远程总流程
# 1. 进入项目文件夹
cd D:\CSS\第二章\26_GIT远程仓库托管网站
# 2. 初始化 Git 仓库
git init
# 3. 添加所有文件到暂存区（或指定文件）
git add .                # 添加所有文件
或者 git add index2.html
# 4. 提交到本地仓库
git commit -m "首次提交"
# 5. 将本地默认分支从 master 重命名为 main（可选，但推荐）
git branch -M main
# 6. 添加远程仓库（使用 SSH 地址）
git remote add origin git@github.com:iscyh-hub/breatingheart.git
# 7. 推送到远程 main 分支，并建立上游跟踪
git push -u origin main
# 如果本地已经是 master 分支，想推送到远程 main
方法A：在推送前重命名本地分支
bash
git branch -M main          # 将本地 master 重命名为 main
git push -u origin main
方法B：直接推送本地 master 到远程 main
bash
git push -u origin master:main
#后续日常更新
bash
git add .
git commit -m "更新说明"
git push
