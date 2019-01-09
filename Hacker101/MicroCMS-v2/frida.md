# frida安装的那些坑

## 需要装的
* python
* setuptools(easy_install,理想情况不需要)
* frida
* frida-tools

## 最理想的安装方法

（可能需要sudo）

pip install frida

pip install frida-tools

完事。

## 备用方法

出于网络原因，pip直接安装frida可能会卡住，此时我们需要先把egg文件下到本地用setuptools进行安装

### 先装setuptools

https://pypi.org/project/setuptools/#files

下载最新版的.whl文件，命令行安装：
```
pip install (本地.whl文件路径).whl
```

### 通过setuptools安装frida

https://pypi.org/project/frida/#files

下载你需要的版本.egg文件，命令行安装：
```
easy_install (本地.egg文件路径).egg
```

如果你的python目录和默认不一致会报错（比如配置了python2/3双环境），需要显示调用：
```
python -m easy_install (本地.egg文件路径).egg
```

### 安装frida-tools

通常直接pip install frida-tools不会出问题，如果实在有问题就下载到本地

https://pypi.org/project/frida-tools/#files

解压运行setup.py安装吧

## 安装完成
命令行：
```
frida-ps
```
如果能显示当前系统进程则证明安装成功
