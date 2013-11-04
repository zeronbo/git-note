#Git权威指南学习笔记

##第2章

+	`git add`：将修改内容加入提交暂存区。
+	`git add -u`：将所有修改过的文件加入暂存区。
+	`git add -A`：将本地删除文件和新增文件都登记到提交暂存区。
+	`git add -p`：将一个文件内的修改进行有选择性的添加。

##第3章

**tips：**

+	通过命令：`git config --global core.quotepath false`，可解决在使用git命令
	查看具有中文的文件或路径时显示的字符串为八进制字符编码，
	如：`"Git\346\235\203\345\250\201\346\214\207\345\215\227.md"`。
+	Cygwin中设置忽略文件名大小定，编辑文件`~/.inputrc`，在其中
	添加`set completion-ignore-case on`。
+	取消Git Windows下对文件权限的检测，防止因权限变更而需要重新提交文件。命令：
	`git config --system core.fileMode false`。

##第4章

**tips：**

+	`git rev-parse --git-dir`：显示版本库.git目录所在的位置。
+	`git rev-parse --show-toplevel`：显示工作区根目录。
+	`git rev-parse --show-prefix`：显示当前目录相对于工作区根目录的相对目录路径。
+	`git rev-parse --show-cdup`：显示从当前目录后退(`cd ..`)到工作区的根的深度。
+	`git config -e`：设置版本库级别的配置文件(注：需要在有.git文件夹的目录下执行)。
+	`git config -e --global`：设置全局配置文件，修改的文件为用户主目录下的`.gitconfig`
	文件，windows路径一般为：`C:\用户\XXX\.gitconfig`，Linux路径一般为：`/home/XXX/.gitconfig`
	`XXX`指代用户名。
+	`git config -e --system`：设置系统级配置文件，Windows路径一般为Git安装根路径下的`etc/gitconfig`文件
	Linux路径为：`/etc/gitconfig`文件。
+	配置优先级为：`git config -e` > `git config -e --global` > `git config -e --system`。
+	`git commit --allow-empty -m <msg>`：可执行一个空白提交，`msg`为具体的提交信息。
+	`git log --pretty=fuller`：可显示完整的日志信息。
+	`git commit --amend --reset-author`：修改最新的提交信息，`--amend`对刚刚的提交进行修补，不会
	产生另外新的提交，`--reset-author`将Author(作者)的ID同步修改，否则只会影响提交者(Commit)的ID。
	如果上次的提交是一个空的提交，需执行命令`git commit --amend --allow-empty --reset-author`。
+	`git clone demo demo-step-1`：将本地库demo克隆(备份)为。

##第5章

+	`git log --stat`：查看每次提交的文件变更统计。
