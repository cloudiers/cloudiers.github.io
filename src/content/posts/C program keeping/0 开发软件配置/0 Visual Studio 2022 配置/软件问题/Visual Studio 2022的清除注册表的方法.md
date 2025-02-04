1）通过vs自带工具完成卸载

2）通过微软提供的开源卸载工具VisualStudioUninstaller可以清理MSI、MSU等残留插件

[链接地址](https://github.com/Microsoft/VisualStudioUninstaller/releases)

![[_attachments/TotalUninstaller.zip]]

下载TotalUninstaller后解压，右键以管理员权限运行.exe文件

输入Y之后按enter键，等待程序执行，结束会自己关闭

3）删除安装目录

C:\Program Files\Microsoft Visual Studio

C:\Program Files(x86)\Microsoft Visual Studio

删除整个Microsoft Visual Studio文件夹：shift+delete

4）删除注册表
win+R

输入路径：计算机\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\VisualStudio（唯一）

按路径找到visual studio注册表，右键删除
