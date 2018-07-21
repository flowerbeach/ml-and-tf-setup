# 安装 + 使用 Anaconda

## 使用 Miniconda

参考：https://conda.io/miniconda.html

```bash
# use Python3
wget https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh -O miniconda.sh
bash miniconda.sh -b -p $HOME/usr/miniconda
[edit ~/.bashrc]
export PATH=$HOME/usr/miniconda/bin:$PATH
```

## 配置国内镜像

```bash
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
conda config --set show_channel_urls yes
```

## 配置 conda （optional）

```bash
conda config --set always_yes yes
```

## 更新 conda

```bash
conda update conda
```

## 新建环境

```bash
conda create --name {env-name}
```

使用指定 Python 版本：

```bash
conda create --name {env-name} python=3.4
```

## 激活环境

```bash
source activate {env-name}
[or in Windows]
activate {env-name}
```

## 退出环境

```bash
source deactivate
[or in Windows]
deactivate
```

## 查看环境

```bash
conda env list
```

## 删除环境

```bash
conda env remove --name {env-name}
```

## 生成 `environment.yml`

```bash
conda env export > environment.yml
```

## 从 `environment.yml` 中创建环境

```bash
conda env create -f environment.yml
```

## 在环境中改变 Python 版本

```bash
conda install python=3.6
```

## 安装 Numpy + OpenCV

```bash
conda install numpy
conda install -c https://conda.binstar.org/menpo opencv
```

## 参考链接

[conda vs. pip vs. virtualenv](https://conda.io/docs/_downloads/conda-pip-virtualenv-translator.html)
