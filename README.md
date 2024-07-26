# install-radmc3d-windows
radmc3d需要unix环境shell（mac、linux自带）安装，因此windows系统需要**额外安装WSL**以运行radmc3d.

Since the installation of [radmc3d](https://github.com/dullemond/radmc3d-2.0/tree/master) needs **Unix Shell**, **WSL--windows subsystem for linux** should be needed.

## 首次安装WSL First time WSL installation
如果已安装WSL，请跳过这一段。

If you have already installed **WSL**, skip this section.

**以管理员身份**打开powershell 或 windows propmt

Open Powershell or Windows Prompt **in adminsitrator mode**

然后输入：

Then enter:

> wsl --install

WSL默认发行版是Ubuntu（这个不用管，wsl 1 2 都不用管，只要看版本号）

WSL will be installed with **Default Distribution** _Ubuntu_, please be aware of its version but ignore whether it is WSL 1 or 2

安装完毕打开wsl注册并使用SHELL

After the installation of WSL, register and start using SHELL

如果在中国大陆，请替换为清华源

# USE SHELL TO INSTALL GFORTRAN AND PYTHON

TODO
