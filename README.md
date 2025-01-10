# Ubuntu
# 常用指令

## CUDA
wys@wys-Victus-by-HP-Gaming-Laptop-15-fa1xxx:~/Downloads$ sudo sh ./cuda_12.1.1_530.30.02_linux.run
[sudo] password for wys: 
===========
= Summary =
===========

Driver:   Not Selected
Toolkit:  Installed in /usr/local/cuda-12.1/

Please make sure that
 -   PATH includes /usr/local/cuda-12.1/bin
 -   LD_LIBRARY_PATH includes /usr/local/cuda-12.1/lib64, or, add /usr/local/cuda-12.1/lib64 to /etc/ld.so.conf and run ldconfig as root

To uninstall the CUDA Toolkit, run cuda-uninstaller in /usr/local/cuda-12.1/bin
***WARNING: Incomplete installation! This installation did not install the CUDA Driver. A driver of version at least 530.00 is required for CUDA 12.1 functionality to work.
To install the driver using this installer, run the following command, replacing <CudaInstaller> with the name of this run file:
    sudo <CudaInstaller>.run --silent --driver

Logfile is /var/log/cuda-installer.log


## Vim

### 快捷键

```
模式切换
Normal 模式（正常模式）：按 Esc 键进入。
Insert 模式（插入模式）：按 i 键进入。
Visual 模式（可视模式）：按 v 键进入。
Command 模式（命令模式）：按 : 进入。
```

### 复制黏贴

```
复制 ： (普通模式)yy nyy 
	  （v模式）y 
粘贴 ： (普通模式) p P 
剪切 ：+y
黏贴 ： （普通） +p
```

### Normal 模式快捷键

#### 光标移动

- `h`：向左移动一个字符。
- `j`：向下移动一行。
- `k`：向上移动一行。
- `l`：向右移动一个字符。
- `w`：移动到下一个单词的开头。
- `b`：移动到前一个单词的开头。
- `e`：移动到当前单词的结尾。
- `0`：移动到行首。
- `$`：移动到行尾。
- `gg`：移动到文件开头。
- `G`：移动到文件结尾。
- `H`：移动到屏幕顶部。
- `M`：移动到屏幕中部。
- `L`：移动到屏幕底部。

#### 编辑操作

- `x`：删除当前字符。
- `dd`：删除当前行。
- `dw`：删除到下一个单词的开头。
- `d$`：删除到行尾。
- `D`：删除到行尾（相当于 `d$`）。
- `yy`：复制当前行。
- `yw`：复制到下一个单词的开头。
- `y$`：复制到行尾。
- `p`：在光标后粘贴。
- `u`：撤销上一步操作。
- `Ctrl+r`：重做上一步操作。

#### 查找与替换

- `/text`：查找 `text`。
- `n`：跳到下一个匹配项。
- `N`：跳到上一个匹配项。
- `:%s/old/new/g`：全局替换 `old` 为 `new`。
- `:s/old/new/g`：当前行替换 `old` 为 `new`。

### Insert 模式快捷键

- `i`：在当前光标位置进入插入模式。
- `I`：在当前行首进入插入模式。
- `a`：在当前光标后进入插入模式。
- `A`：在当前行尾进入插入模式。
- `o`：在当前行下方新建一行并进入插入模式。
- `O`：在当前行上方新建一行并进入插入模式。
- `Esc`：退出插入模式，返回正常模式。

### Visual 模式快捷键

- `v`：进入字符可视模式。
- `V`：进入行可视模式。
- `Ctrl+v`：进入块可视模式。
- `y`：复制选中的文本。
- `d`：删除选中的文本。
- `>`：缩进选中的文本。
- `<`：反缩进选中的文本。

### Command 模式快捷键

- `:w`：保存文件。
- `:q`：退出 Vim。
- `:wq`：保存并退出 Vim。
- `:q!`：强制退出，不保存修改。
- `:e filename`：打开文件 `filename`。
- `:vsp filename`：垂直分割窗口并打开文件 `filename`。
- `:sp filename`：水平分割窗口并打开文件 `filename`。

### 窗口管理

- `Ctrl+w s`：水平分割窗口。
- `Ctrl+w v`：垂直分割窗口。
- `Ctrl+w c`：关闭当前窗口。
- `Ctrl+w o`：关闭其他窗口，只保留当前窗口。
- `Ctrl+w w`：切换到下一个窗口。
- `Ctrl+w h`：切换到左边的窗口。
- `Ctrl+w j`：切换到下边的窗口。
- `Ctrl+w k`：切换到上边的窗口。
- `Ctrl+w l`：切换到右边的窗口。

### 缓冲区管理

- `:bnext` 或 `:bn`：切换到下一个缓冲区。
- `:bprev` 或 `:bp`：切换到上一个缓冲区。
- `:bfirst`：切换到第一个缓冲区。
- `:blast`：切换到最后一个缓冲区。
- `:bd`：删除当前缓冲区。

### 标签页管理

- `:tabnew filename`：在新标签页中打开文件 `filename`。
- `:tabnext` 或 `:tabn`：切换到下一个标签页。
- `:tabprev` 或 `:tabp`：切换到上一个标签页。
- `:tabclose` 或 `:tabc`：关闭当前标签页。
- `:tabonly`：关闭其他标签页，只保留当前标签页。

## Anaconda

### 环境

```
conda activate
conda create -n [env_name] python=3.8
conda activate [env_name]
```

### 装包

```
conda install 
pip install 
```

### 删环境

```
conda remove -n xxxxx(名字) --all
```

### 删包

```
conda activate  xx
conda remove --name  xx
```

### 指令集

- **conda create --name newenv --file environment.yml**：从“environment.yml”文件创建一个名为“newenv”的新环境。
- **conda install --file requirements.txt**：从“requirements.txt”文件中安装包。
- **conda export --name myenv > environment.yml**：将“myenv”环境导出到“environment.yml”文件。
- **conda list --explicit**：列出所有已安装的包，包括依赖关系
- **conda update --all**：更新所有已安装的包。
- **conda install --dry-run**：模拟一个包的安装，而不实际安装它。
- **conda pack**：打包一个Conda环境。
- **conda env**：管理Conda环境。
- **conda clean**：清理Conda缓存。
- **conda config**：管理Conda配置。
- **conda config**：管理Conda配置。
- **conda list**：列出当前环境中安装的包。
- **conda search**：搜索一个或多个包。
- **conda uninstall**：卸载一个或多个包从当前环境中。

## Typora

* 

  ```
   Ctrl+shift+] 或者 星号*＋空格
  ```

  * ```
    先回车(Enter)、再Tab 键 
    ```

    * ```
      先回车(Enter)、再Tab 键 
      ```

      

###### 增大标题等级：Ctrl+=

插入表格：`Ctrl+t`

加粗：**ctrl+b**

斜体：*ctrl+i*

插入表格：Ctrl+t

代码：``ctrl+shift` +``

超链接：[ctrl+k](https://blog.csdn.net/MS_SONG/article/details/122384983)

数学公式：

- $$ + 回车
- ctrl + shift + m





## bash

### 快捷键

```
 ctrl+A 把光标移到命令行开头
 ctrl+E 把光标移到命令行末尾
 ctrl+C 强制中止当前的命令
 ctrl+L 清屏，相当于clear命令
 ctrl+U 删除或剪切光标之前的命令，我输入了一行很长的命令，不用使用退格键一个一个字符的删除，使用这个快捷键会更加方便
 ctrl+K 删除或剪切光标之后的内容
 ctrl+Y 粘贴ctrl+U或ctrl+K剪切的内容
 ctrl+R 在历史命令中搜索，按下ctrl+R之后，就会出现搜索界面，只要输入搜索内容，就会从历史命令中搜索
 ctrl+D 退出当前终端
 ctrl+Z 暂停，并放入后台，这个快捷键牵扯工作管理的内容
 ctrl+S 暂停屏幕输出
 ctrl+Q 恢复屏幕输出
```

## snap

```
snap list
sudo snap search xxx
sudo snap install xxx
sudo sanp remove xxx
sudo apt autoremove --purge snapd(全部清空)
```



## 万能指令

```
sudo nautilus
```

## 性能分析

```
top
```

磁盘占用

```
df -h
```



# 环境配置

## apt换源

```
sudo cp -v /etc/apt/sources.list /media/wys/Ventoy/note/ubuntu
sudo gedit /etc/apt/sources.list
```

```
deb http://mirrors.aliyun.com/ubuntu/ focal main restricted universe multiverse

deb http://mirrors.aliyun.com/ubuntu/ focal-security main restricted universe multiverse

deb http://mirrors.aliyun.com/ubuntu/ focal-updates main restricted universe multiverse

deb http://mirrors.aliyun.com/ubuntu/ focal-proposed main restricted universe multiverse

deb http://mirrors.aliyun.com/ubuntu/ focal-backports main restricted universe multiverse

deb-src http://mirrors.aliyun.com/ubuntu/ focal main restricted universe multiverse

deb-src http://mirrors.aliyun.com/ubuntu/ focal-security main restricted universe multiverse

deb-src http://mirrors.aliyun.com/ubuntu/ focal-updates main restricted universe multiverse

deb-src http://mirrors.aliyun.com/ubuntu/ focal-proposed main restricted universe multiverse

deb-src http://mirrors.aliyun.com/ubuntu/ focal-backports main restricted universe multiverse
```

```
sudo apt update
sudo apt upgrade
```

```

deb https://mirrors.ustc.edu.cn/ubuntu/ jammy main restricted universe multiverse
deb-src https://mirrors.ustc.edu.cn/ubuntu/ jammy main restricted universe multiverse
deb https://mirrors.ustc.edu.cn/ubuntu/ jammy-updates main restricted universe multiverse
deb-src https://mirrors.ustc.edu.cn/ubuntu/ jammy-updates main restricted universe multiverse
deb https://mirrors.ustc.edu.cn/ubuntu/ jammy-backports main restricted universe multiverse
deb-src https://mirrors.ustc.edu.cn/ubuntu/ jammy-backports main restricted universe multiverse
deb https://mirrors.ustc.edu.cn/ubuntu/ jammy-security main restricted universe multiverse
deb-src https://mirrors.ustc.edu.cn/ubuntu/ jammy-security main restricted universe multiverse
deb https://mirrors.ustc.edu.cn/ubuntu/ jammy-proposed main restricted universe multiverse
deb-src https://mirrors.ustc.edu.cn/ubuntu/ jammy-proposed main restricted universe multiverse
```

## Nvidia

### 指令

```
ubuntu-drivers devices 查看显卡硬件支持的驱动类型（在使用前需要sudo apt update更新源）
nvidia-smi 查看当前显卡驱动（若没有会返回错误，该命令应为显卡驱动自动安装，切勿按照提示手动安装）
nvcc -V 查看系统安装的cuda驱动（注意这是系统当前使用的cuda驱动，也可以同时存在多个cuda，使用conda+pytorch可以在多个虚拟环境中管理不同的cuda版本
```

### 安装

```
nvidia-smi
lspci | grep -i NVIDIA   检查硬件支持

//禁用nouveau驱动
sudo  gedit  /etc/modprobe.d/blacklist-nouveau.conf
文末添加
blacklist nouveau
blacklist lbm-nouveau
options nouveau modeset=0
alias nouveau off
alias lbm-nouveau off
:qw!
closed:
echo options nouveau modeset=0 | sudo tee -a /etc/modprobe.d/nouveau-kms.conf
完成后会显示"options nouveau modeset=0
sudo update-initramfs -u //更新配置文件
完成后会显示"update-initramfs: Generating /boot/initrd.img-5.15.0-83-generic"
shutdown -r now
lsmod | grep nouveau

//内核源码(可选)
sudo apt-get install linux-headers-$(uname -r)
gcc -v

//开发组件
sudo apt-get update
sudo apt-get install gcc
sudo apt-get install build-essential
sudo apt-get install libprotobuf-dev libleveldb-dev libsnappy-dev libopencv-dev libhdf5-serial-dev protobuf-compiler
sudo apt-get install --no-install-recommends libboost-all-dev
sudo apt-get install libopenblas-dev liblapack-dev libatlas-base-dev
sudo apt-get install libgflags-dev libgoogle-glog-dev liblmdb-dev
sudo apt-get install pkg-config

//kmod--挂载驱动(可选)
sudo apt-get install kmod
sudo apt-get install linux-headers-$(uname -r)
export PATH=$PATH:/sbin:/usr/sbin:/usr/local/sbin
source ~/.bashrc

//卸载原有驱动
sudo apt-get remove nvidia-*

//安装
sudo chmod a+x NVIDIA-Linux-*******.run //加权限
sudo ./NVIDIA-Linux-x86_64-535.104.05.run -no-x-check -no-nouveau-check -no-opengl-files
# 参数解释
–no-x-check：表示安装驱动时不检查X服务（图形接口服务），如果没有关闭图形界面则必须加上，否则反之。
–no-nouveau-check：表示安装驱动时不检查nouveau驱动，这也是非必需的，因为我们已经在前面步骤中禁用驱动。
–no-opengl-files：表示只安装驱动文件，不安装OpenGL文件。这个参数不可省略，否则会导致登陆界面死循环，英语一般称为”login loop”或者”stuck in login”。 
continue installation

The distribution-provided pre-install script failed! Are you sure you want to continue? 
选择 yes 继续。

Would you like to register the kernel module souces with DKMS? This will allow DKMS to automatically build a new module, if you install a different kernel later? 
选择 No 继续。

选择install without signing

Nvidia's 32-bit compatibility libraries? 
选择 No 继续。

Would you like to run the nvidia-xconfigutility to automatically update your x configuration so that the NVIDIA x driver will be used when you restart x? Any pre-existing x confile will be backed up.  
选择 Yes


//挂载驱动
modprobe nvidia

nvidia-smi

//环境变量
sudo vim ~/.bashrc
bashCopy code
export PATH=$PATH:/usr/local/nvidia/bin
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/usr/local/nvidia/lib64
source ~/.bashrc
```

### 卸载

```
sudo apt-get --purge remove nvidia*
sudo apt autoremove
nvidia-smi
sudo /usr/bin/nvidia-uninstall
```

## Cuda

### 安装

```
https://developer.nvidia.com/cuda-toolkit-archive  //下载cuda安装包,优先runfile
https://developer.download.nvidia.com/compute/cuda/11.8.0/local_installers/cuda_11.8.0_520.61.05_linux.run
sudo apt-get install freeglut3-dev build-essential libx11-dev libxmu-dev libxi-dev libgl1-mesa-glx libglu1-mesa libglu1-mesa-dev  //安装CUDA依赖项
sudo sh cuda_11.8.0_520.61.05_linux.run //accept--cancel driver--install

//环境变量
sudo gedit ~/.bashrc
export PATH=/usr/local/cuda-版本/bin:$PATH  
export LD_LIBRARY_PATH=/usr/local/cuda-版本/lib64:$LD_LIBRARY_PATH
export CUDA_HOME=/usr/local/cuda
source ~/.bashrc

//测试CUDA Toolkitdpkg -l | grep Nvidia
nvcc -V
dpkg -l | grep Nvidia

//驱动冲突(可选)
sudo sh ./cuda_10.2.<spec>.run --toolkit --silent --override
```

### 多版本管理

```
//修改环境变量//安装cuda9.0
sudo chmod +x cuda_9.0.176_384.81_linux.run
./cuda_9.0.176_384.81_linux.run

//修改环境变量
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/usr/local/cuda/lib64
export PATH=$PATH:/usr/local/cuda/bin
export CUDA_HOME=$CUDA_HOME:/usr/local/cuda

//查看/usr/local/cuda软连接
cd /usr/local
# 方法１
ll
# 方法２
stat cuda

//删除旧的软连接，建立新的软连接(删除软连接不要使用sudo rm -rf ./cuda/，因为这样会把原来的文件全部删除掉)
sudo rm -rf ./cuda
sudo ln -s /usr/local/cuda-9.0 /usr/local/cuda


//下载cuda9.0对应的cudnn7.6.4
sudo cp cuda/include/cudnn*.h /usr/local/cuda-9.0/include
sudo cp cuda/lib64/libcudnn* /usr/local/cuda-9.0/lib64
sudo chmod a+r /usr/local/cuda-12.1/include/cudnn.h /usr/local/cuda-12.1/lib64/libcudnn*


//测试cudnn
sudo cat /usr/local/cuda/include/cudnn.h | grep CUDNN_MAJOR -A 2
# 输出为
#define CUDNN_MAJOR 7
#define CUDNN_MINOR 6
#define CUDNN_PATCHLEVEL 4
--
#define CUDNN_VERSION (CUDNN_MAJOR * 1000 + CUDNN_MINOR * 100 + CUDNN_PATCHLEVEL)

#include "driver_types.h"

//测试CUDA
nvcc -V
# 输出
nvcc: NVIDIA (R) Cuda compiler driver
Copyright (c) 2005-2017 NVIDIA Corporation
Built on Fri_Sep__1_21:08:03_CDT_2017
Cuda compilation tools, release 9.0, V9.0.176
```





## Cudnn

- [cudnn](https://developer.nvidia.com/cudnn-downloads)
- [cudnn-archive](https://developer.nvidia.com/rdp/cudnn-archive)

### 安装

```
tar -xzvf cudnn-10.1-linux-x64-v8.0.5.39.tgz //下载的cudnn的压缩包 .gz格式
tar -xJvf cudnn-linux-x86_64-8.9.7.29_cuda12-archive.tar.xz  // .xz格式
archive

//赋权限
cd /usr/local/cuda
sudo chmod 666 include
sudo cp cudnn-*/include/cudnn*.h /usr/local/cuda/include 
sudo cp cudnn-*/lib/libcudnn* /usr/local/cuda/lib64 
sudo chmod a+r /usr/local/cuda/include/cudnn*.h /usr/local/cuda/lib64/libcudnn*

sudo cat /usr/local/cuda/include/cudnn_version.h | grep CUDNN_MAJOR -A 2
```



## 搜狗

1.download sougou

 https://shurufa.sogou.com   x86-64

2.install fcitx

```
sudo apt update
sudo apt install fcitx
```

3.manage language

```
setting
->language support
->choose fcitx
->Apply Ststem-Wide
->Close
```

4.manage auto-set

```
sudo cp /usr/share/applications/fcitx.desktop /etc/xdg/autostart/
```

5.remove ibus

```
sudo apt purge ibus
```

6.install sougou

```
sudo dpkg -i sogoupinyin_4.0.1.2800_x86_64.deb
```

7.install depdency

```
sudo apt install libqt5qml5 libqt5quick5 libqt5quickwidgets5 qml-module-qtquick2
sudo apt install libgsettings-qt1
```

8.peizhi

```
sudo reboot
->config
在“Input Method Configuration”界面 —> 点击左下角“+” —> 取消“Only Show Current Language” —> 搜索框输入“sougou” —> 选中“sogoupinyin” —> 点击“OK”；
(4) 选中添加的“sogoupinyin” —> 点击“^”
(5) 关闭配置界面，打开火狐浏览器，测试输入法OK；
```



## Terminator

### 下载

```
sudo add-apt-repository ppa:gnome-terminator
sudo apt update
sudo apt install terminator
```

### 重置

```
sudo apt-get install dconf-tools
gsettings set org.gnome.desktop.default-applications.terminal exec /usr/bin/gnome-terminal
gsettings set org.gnome.desktop.default-applications.terminal exec-arg "-x"
```

### 再

```
gsettings reset org.gnome.desktop.default-applications.terminal exec
gsettings reset org.gnome.desktop.default-applications.terminal exec-arg
```

### 优先级

```
sudo update-alternatives --install /usr/bin/x-terminal-emulator x-terminal-emulator /usr/bin/terminator 50
```

### ctl+shift+E失灵

```
搜狗-->设置-->高级-->系统功能
```

## 网卡

```
sudo apt install flex bison
git clone https://github.com/intel/backport-iwlwifi.git
cd backport-iwlwifi
cd iwlwifi-stack-dev

sudo make

sudo make defconfig-iwlwifi-public

sudo make install
```

```
https://www.intel.com/content/www/us/en/support/articles/000005511/wireless.html

wifi6 AX210 160MHz

sudo cp iwlwifi-* /backport-iwlwifi/fw-binaries
```

```
size_t dirname_len = strlen(dirname);
size_t basename_len = strlen(basename);
size_t newname_len = dirname_len + basename_len + 1;
size_t tmpname_len = dirname_len + 13;

snprintf(newname, newname_len,"%s%s", dirname, basename);
env = getenv("KCONFIG_OVERWRITECONFIG");
if (!env || !*env) {
snprintf(tmpname, tmpname_len,"%s.tmpconfig.%d", dirname, (int)getpid());
out = fopen(tmpname, "w");
} else {
*tmpname = 0;
out = fopen(newname, "w");
}
```



## Anaconda

### 安装

```
https://mirrors.tuna.tsinghua.edu.cn/anaconda/archive/
bash Anaconda3-2021.11-Linux-x86_64.sh
conda init 
conda --version

//加环境
echo 'export PATH="/home/你的用户名/anaconda3/bin:$PATH"' >> ~/.bashrc
echo 'export PATH="/home/wys/Public/anaconda3/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc

//改镜像
conda config --show channels #查看目前已有的镜像
conda config --add channels 
https://mirrors.aliyun.com/anaconda/pkgs/main/
https://mirrors.aliyun.com/anaconda/pkgs/free/#添加清华源
conda config --set show_channel_urls yes#从channel中安装包时显示channel的url,这样就可以知道包的安装来源
conda config --set show_channel_urls  #验证一下配置是否成功


//pip
pip config get global.index-url --查看
pip config set global.index-url https://mirrors.aliyun.com/pypi/simple/
pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple

//codna
conda clean -i 清除缓存
sudo gedit ~/.condarc 
//粘贴
channels:
 - defaults
show_channel_urls: true
default_channels:
 - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main
 - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/r
 - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/msys2
custom_channels:
 conda-forge: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
 msys2: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
 bioconda: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
 menpo: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
 pytorch: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
 pytorch-lts: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
 simpleitk: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
 //测试
 conda install scrapy
 
 //冷门包源
 //国内常用的anaconda镜像：
http://mirrors.aliyun.com/pypi/simple/ #阿里
https://pypi.tuna.tsinghua.edu.cn/simple/ #清华
http://pypi.douban.com/ #豆瓣
http://pypi.mirrors.ustc.edu.cn/ #中国科学技术大学

建议下面也全部添加，虽然有些可能用不到，但是实际包含比较冷门的包
conda config --add channels http://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/
conda config --add channels http://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/fastai/
conda config --set show_channel_urls yes


```



## Vim

### 安装

```
sudo apt-get install vim-gtk
```

### 插件

```
sudo vim /etc/vim/vimrc
if has("syntax")
	syntax
endif
set nu                           // 在左侧行号
set tabstop                  //tab 长度设置为 4
set nobackup               //覆盖文件时不备份
set cursorline               //突出显示当前行
set ruler                       //在右下角显示光标位置的状态行
set autoindent             //自动缩进

#vimrc文件添加插件
Plugin 'luochen1990/rainbow' 
#插件更新
PlugUpdate
#插件安装
`PlugInstall
#插件查找
PlugSearch
#插件状态
PlugStatus
#插件管理
Vundle
```



## 卡机动画去除

```
sudo cp /etc/default/grub /etc/default/grub.bak
sudo nano /etc/default/grub
GRUB_TIMEOUT_STYLE=hidden 并将其更改为 GRUB_TIMEOUT_STYLE=menu
你想完全去除开机图像，找到 GRUB_BACKGROUND 配置项并注释掉或删除它
```



## 鱼香

```
wget http://fishros.com/install -O fishros && . fishros
```





# 日常Bug

## 火狐视频损坏

```
sudo apt-get install ffmpeg	//若否
sudo apt-get install flashplugin-installer 
```

## Ubuntu22.04g++版本问题

```
sudo add-apt-repository ppa:ubuntu-toolchain-r/test
sudo apt update
sudo apt install gcc-12 g++-12
sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-12 60
sudo update-alternatives --install /usr/bin/g++ g++ /usr/bin/g++-12 60

```

## 卸载无用驱动器

```
sudo umount xxx
sudo lsof /Path/to/target
sudo kill -9 [PID]
sudo umount -f /Path/to/target
```

## Vim:insert 下esc失灵:	Ctrl + q

## 
