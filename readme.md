# git 演示

1. 确认有没有git插件
	1. windows-->prefernce-->team--git
	
2. 打开git视图
    * 点击 右上角带+号的小图标--> 选择Git
    
3. clone 代码
    * 点击git视图中,第二个链接，
    * 在弹出界面中，输入git仓库的地址
	
4. 提交新建文件 	
   * 新建的文件，小图标中有？号
   * 右键菜单-->team-- add to index;小图标变为+号
   * 右键菜单-->team-- commit;小图标变为黄色的小图标
   * 右键菜单-->team-- push;代码提交到远程服务器中；
 
5. 提交修改的文件 	
   * 新建的文件，小图标右边有大于号
   * 右键菜单-->team-- commit;小图标变为黄色的小图标
   * 右键菜单-->team-- push;代码提交到远程服务器中；
   
6. 更新代码
   * 右键菜单-->team-- synchoinze workspace
   * 右键菜单-->team-- Fetch 
   * 右键菜单-->team-- Merge

7. 合并代码（两个人修改同一个代码文件）
   * 右键菜单-->team-- synchoinze workspace
   * 如果发现服务器上有新代码,*要保证本地修改的代码，已commit*
   * 右键菜单-->team-- Fetch 
   * 右键菜单-->team-- Merge
8. 应用多个远程仓库
   1. 编辑项目本地库(.git)目录下的config文件,配置多个远程库，
'''
[remote "origin"]
    url = https://github.com/junctioner/gitdemo.git
    fetch = +refs/heads/*:refs/remotes/origin/*
[remote "gitee"]
    url = https://gitee.com/junctioner/giteeDemo.git
    fetch = +refs/heads/*:refs/remotes/origin/*
'''
    2. pull操作
        * 使用以下命令，可以分别从两个远程仓库pull：
git pull origin master
git pull mirror master12
    3. push操作
使用以下命令，可以分别push到两个远程仓库：
git push origin master
git push mirror master

