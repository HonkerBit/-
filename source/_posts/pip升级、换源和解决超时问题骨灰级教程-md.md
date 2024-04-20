---
title: pip升级、换源和解决超时问题骨灰级教程
date: 2023-12-28 
tags: 
- Python
- pip
categories:
- Python
keywords: pip升级,换源,超时问题解决
---

#  升级pip

在之前的文章中已经讲了如何配置环境变量：[解决“‘python’不是内部或外部命令，也不是可运行的程序或批处理文件”](http://t.csdn.cn/iRz1U)

在刚安装好python编译器时，使用pip工具时经常会出现这样的问题：

![img](pip%E5%8D%87%E7%BA%A7%E3%80%81%E6%8D%A2%E6%BA%90%E5%92%8C%E8%A7%A3%E5%86%B3%E8%B6%85%E6%97%B6%E9%97%AE%E9%A2%98%E9%AA%A8%E7%81%B0%E7%BA%A7%E6%95%99%E7%A8%8B-md/7885147a7a4a4495b454d34042d74e42.png)![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)编辑

提示需要升级pip版本,如果pip的版本太老，很多包都无法安装

先尝试在命令行使用命令升级：

```
python -m pip install --upgrade pip
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)

这样就是升级成功了

![img](pip%E5%8D%87%E7%BA%A7%E3%80%81%E6%8D%A2%E6%BA%90%E5%92%8C%E8%A7%A3%E5%86%B3%E8%B6%85%E6%97%B6%E9%97%AE%E9%A2%98%E9%AA%A8%E7%81%B0%E7%BA%A7%E6%95%99%E7%A8%8B-md/c15267c4efe8471c87f969d8700b98ce.png)![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)编辑



如果不成功，干脆删掉pip

```python
pip uninstall pip
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)

然后在官网下载pip包：[pip · PyPI](https://pypi.org/project/pip/)

点击Download files,下载压缩包

![img](pip%E5%8D%87%E7%BA%A7%E3%80%81%E6%8D%A2%E6%BA%90%E5%92%8C%E8%A7%A3%E5%86%B3%E8%B6%85%E6%97%B6%E9%97%AE%E9%A2%98%E9%AA%A8%E7%81%B0%E7%BA%A7%E6%95%99%E7%A8%8B-md/c0172dd3b1e2437397c39de40d46df5f.png)![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)编辑



 下载好的压缩包：

![img](pip%E5%8D%87%E7%BA%A7%E3%80%81%E6%8D%A2%E6%BA%90%E5%92%8C%E8%A7%A3%E5%86%B3%E8%B6%85%E6%97%B6%E9%97%AE%E9%A2%98%E9%AA%A8%E7%81%B0%E7%BA%A7%E6%95%99%E7%A8%8B-md/3b676ad892de4155954743a2f15a9a6f.png)![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)编辑

解压压缩包，在文件目录输入cmd打开命令行或者打开命令行cd进入文件夹：

> cd 目标目录 

 ![img](pip%E5%8D%87%E7%BA%A7%E3%80%81%E6%8D%A2%E6%BA%90%E5%92%8C%E8%A7%A3%E5%86%B3%E8%B6%85%E6%97%B6%E9%97%AE%E9%A2%98%E9%AA%A8%E7%81%B0%E7%BA%A7%E6%95%99%E7%A8%8B-md/e9d8454af30d43d3b93d77d685e8a88b.png)![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)编辑

在命令行输入命令安装pip

```python
python setup.py install
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)

 安装完成输入命令检查pip的版本：

![img](pip%E5%8D%87%E7%BA%A7%E3%80%81%E6%8D%A2%E6%BA%90%E5%92%8C%E8%A7%A3%E5%86%B3%E8%B6%85%E6%97%B6%E9%97%AE%E9%A2%98%E9%AA%A8%E7%81%B0%E7%BA%A7%E6%95%99%E7%A8%8B-md/efab185a74ca4713beed0043f72c2e85.png)![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)编辑

##  pip的换源

安装库总失败、安装速度太慢我们可以把镜像源切换为国内源，速度快到起飞

**临时使用国内镜像安装**格式：

```python
pip install 包名 -i 镜像源
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)

一些常用的国内源：

清华大学：https://pypi.tuna.tsinghua.edu.cn/simple

阿里云：https://mirrors.aliyun.com/pypi/simple

中国科学技术大学 https://pypi.mirrors.ustc.edu.cn/simple

豆瓣：http://pypi.douban.com/simple


 永久替换：

### windows：

在pip子目录下建立pip的配置文件：pip.ini

打开 appdata 文件夹，在资源管理器的地址栏输入 `%appdata%` 后回车：

![在这里插入图片描述](pip%E5%8D%87%E7%BA%A7%E3%80%81%E6%8D%A2%E6%BA%90%E5%92%8C%E8%A7%A3%E5%86%B3%E8%B6%85%E6%97%B6%E9%97%AE%E9%A2%98%E9%AA%A8%E7%81%B0%E7%BA%A7%E6%95%99%E7%A8%8B-md/20210508192633540.png)![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)编辑
 新建一个 pip 文件夹，在 pip 文件夹里面新建一个配置文件 `pip.ini`：

```python
# coding: GBK
[global]
index-url = https://pypi.tuna.tsinghua.edu.cn/simple
[install]
trusted-host = https://pypi.tuna.tsinghua.edu.cn
#清华大学：https://pypi.tuna.tsinghua.edu.cn/simple
#阿里云：http://mirrors.aliyun.com/pypi/simple/
#豆瓣：http://pypi.douban.com/simple/
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)

![img](pip%E5%8D%87%E7%BA%A7%E3%80%81%E6%8D%A2%E6%BA%90%E5%92%8C%E8%A7%A3%E5%86%B3%E8%B6%85%E6%97%B6%E9%97%AE%E9%A2%98%E9%AA%A8%E7%81%B0%E7%BA%A7%E6%95%99%E7%A8%8B-md/2ad6cc393fd94c71b45c5f8e7a864a0d.png)![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)编辑

 **Linux**：同样需要建立子目录并在此pip目录下建立内容同上的 pip.conf的位置文件：

```python
cd ~
mkdir pip
cd pip
vi pip.ini
#内容同windows环境下。
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)

再次使用 pip时，即会使用新镜像源

## 解决超时问题

使用 pip 安装第三方库时，可能遇到超时问题，导致下载中断，并提示：ReadTimeoutError: HTTPSConnectionPool (host=‘files.pythonhosted.org’, port=443): Read timed out. 等错误信息。主要原因在于网络连接不稳定。

解决办法：

换源，超时设置，还源+超时设置【狗头】

```python
pip --default-timeout=100 install 包名 -i http://pypi.do
uban.com/simple/ --trusted-host pypi.douban.com
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)

