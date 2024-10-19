jupyter使用指南

1.在python的安装路径下的**Scripts**下打开命令行cmd或者powershell输入 **pip install jupyter**

2.在python的安装路径下的**Scripts**目录中，命令行cmd或者powershell输入命令：**jupyter-notebook --generate-config**

运行完这步，会生成一个文件修改**jupyter_notebook_config.py**,找到并用文本编辑器（例如VSCode）打开

3搜索c.ServerApp.root_dir,不改动该行，直接在下面添加新的一行c.NotebookApp.notebook_dir = '**你自己的工作目录**'

示例：

\## The directory to use for notebooks and kernels.

\#  Default: ''

\# c.ServerApp.root_dir = ''

c.NotebookApp.notebook_dir = 'C:\\\\Users\\\\aaaa\\\\Desktop\\\\new_test' (**新增的行，记得不要注释的#**)

tips:工作目录就是你要编辑的代码以及相关文件所在的目录，没想好的话可以创一个空的

4.在上一步配置jupyter的工作目录地址的时候，因为一个反斜线可能会发生转义，建议使用"\\\\\"**双反斜线**分割（本机就是因为反斜线配置地址配了很久）

5.在安装目录下（本机是"C:\\\Users\\\aaaa\\\python project\\\Scripts"）用命令行cmd或者powershell输入命令**jupyter-notebook**自动跳转到jupyter的web界面）

参考：[小白都能看懂的Jupyter安装教程，带你绕过很多坑（Windows版） - 知乎](https://zhuanlan.zhihu.com/p/127839755)

