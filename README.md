
#### 2. 配置git :
`git config --global user.name "用户名"`  
`git config --global user.email "邮箱"`  
### 3. 配置github ssh key

#### 第一步：检查本地主机是否已经存在ssh key  
`cd ~/.ssh`  
`ls`  
观察是否存在  
id_rsa  id_rsa.pub  
如果存在，说明已经有SSH Key

---

#### 第二步 (ssh key不存在时)  
`ssh-keygen -t rsa -C "邮箱"`  

---

#### 第三步 (ssh key存在时)
`cat id_rsa.pub`  
拷贝秘钥 ssh-rsa开头到最后  

---

#### 第四步
1.打开GitHub点击用户头像，选择setting  
2.点击SSH and GPG keys  
3.点击New SSH key  
4.填写标题(随便写)  
5.填写ras (复制的那些东西)  
6.提交  

---

#### 第五步
cmd命令行中输入  
`ssh -T git@github.com`  
观察输出信息是否成功

---

### (clone)克隆项目 :
`git clone git@github.com:buyaozhiwangwomenzu/ourTeam.git`

### (push)推送项目 :
1. ` git add . `
2. ` git commit -m "提交信息" `
3. `git push`