# Anaconda

https://mirrors.tuna.tsinghua.edu.cn/anaconda/archive/

###### 解压

```
bash Anaconda3-2021.11-Linux-x86_64.sh
```

###### 查看版本号 初始化

```
conda init 
conda --version
```

###### 找不到conda命令--conda未加入环境变量

```
echo 'export PATH="/home/你的用户名/anaconda3/bin:$PATH"' >> ~/.bashrc
echo 'export PATH="/home/wys/Public/anaconda3/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```

###### conda镜像源更改

```
conda config --show channels #查看目前已有的镜像
conda config --add channels 
https://mirrors.aliyun.com/anaconda/pkgs/main/
https://mirrors.aliyun.com/anaconda/pkgs/free/#添加清华源
conda config --set show_channel_urls yes#从channel中安装包时显示channel的url,这样就可以知道包的安装来源
conda config --set show_channel_urls  #验证一下配置是否成功
```

pip换源

```
pip config get global.index-url --查看
pip config set global.index-url https://mirrors.aliyun.com/pypi/simple/
pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple
```

conda换源

```
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
 
 
```



###### 冷门包源

```
国内常用的anaconda镜像：
http://mirrors.aliyun.com/pypi/simple/ #阿里
https://pypi.tuna.tsinghua.edu.cn/simple/ #清华
http://pypi.douban.com/ #豆瓣
http://pypi.mirrors.ustc.edu.cn/ #中国科学技术大学

建议下面也全部添加，虽然有些可能用不到，但是实际包含比较冷门的包
conda config --add channels http://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/
conda config --add channels http://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/fastai/
conda config --set show_channel_urls yes
```

###### 虚拟环境配置

```
conda activate
conda create -n [env_name] python=3.8
conda activate [env_name]
```

###### 虚拟环境安装依赖--自动添加至python

```
conda install con
pip install
```

###### 删包跑路

```
conda remove -n xxxxx(名字) --all
conda remove xxxx(包名)
```

###### 删除opencv包

```
conda activate  xx
conda remove --name  xx
```

###### 基础指令

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
