## 配置git账户
git config --global user.email drizzly-ni@163.com
git config --global user.name drizzly-ni

## 生成密钥
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"

## 将id_rsa.pub内容复制到github
![](/blogs/Blog远程仓库同步更新/9fc2554a3dfb5424.png)

## 同步更新源仓库
git remote add upstream https://github.com/apache/flink.git（建议使用ssh，即git开头的连接）
git fetch upstream （同步分支）

## 将新增合并到本分支上
git merge upstream/main