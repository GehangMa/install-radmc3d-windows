radmc3d需要unix环境shell（mac、linux自带）安装，因此windows系统需要**额外安装WSL**以运行radmc3d.

Since the installation of [radmc3d](https://github.com/dullemond/radmc3d-2.0/tree/master) needs **Unix Shell**, **WSL--windows subsystem for linux** should be needed.

## 首次安装 WSL First time WSL installation
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

## 使用SHELL配置Fortran 和 PYTHON USE SHELL TO INSTALL FORTRAN AND PYTHON

radmc3d 需要 fortran 和 python 配置，需要在wsl里安装（与windows主系统里是否安装无关）

Since radmc3d is runned by fortran and python codes, fortran and python should be installed in WSL (even though you already have those in windows main system)

### 国内换源

如果你是在中国大陆，为保证安装软件速度正常，请将下载源替换成[清华源](https://mirrors.tuna.tsinghua.edu.cn/help/ubuntu/)
> cat /etc/os-release #先查看Ubuntu版本
>
> cp /etc/apt/sources.list /etc/apt/sources.list.bak #备份原始源
>
> vim /etc/apt/sources.list #打开后替换成清华源
>
> apt update #更新列表
>
> apt-get upgrade #更新软件

如果显示权限问题的报错内容或无法换源，请在指令前加 “sudo ” （管理员运行该指令）

---
### Python installation

> sudo apt-get install python-pip #install pip
>
> sudo apt-get install python-dev #install the python developing environment
> 
> pip install -U numpy==1.21.5 #新版不兼容 numpy 2.0.0 cannot be used for radmc3d, so we have to degrade it.
>
> pip install scipy
>
> pip install matplotlib
>
> pip install astropy

所需python已配置完毕

The python and its modules needed is installed.

### Fortran 

> sudo apt install gfortran
>
> gfortran --version #to check if it is installed successfully

所需Fortran已配置完毕

Fortran compiler needed is installed.

## Install radmc3d

在设置中把默认Terminal换成Linux SHELL

In the setting of your computer, set SHELL as the **default terminal**

前往radmc3d所在的文件夹，右键选择Terminal启动SHELL，然后按官方教程进行安装。

Find the main folder of radmc3d, open the terminal (now it is **SHELL**) to install it, following the [official instruction](https://www.ita.uni-heidelberg.de/~dullemond/software/radmc-3d/manual_radmc3d/index.html)

**如果python指令报错，请换成python3指令**

**If the 'python' command cannot be used, replace it with 'python3' instead**
