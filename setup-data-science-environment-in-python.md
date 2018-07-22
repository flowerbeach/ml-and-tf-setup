# 配置 Python 科学计算环境

## 使用 conda（在 Windows 上推荐使用）

新建虚拟环境

```
conda create --name {env-name}
source activate {env-name}
```

安装依赖

```
conda install numpy
conda install pandas
conda install matplotlib
conda install jupyter
```

启动 IPython 环境

```
jupyter notebook
[or]
jupyter notebook --no-browser
```

## 使用 pip

新建虚拟环境

```
mkvirtualenv {env-name}
workon {env-name}
```

安装依赖

```
pip install numpy
pip install pandas
pip install matplotlib
pip install jupyter
```

**注意**：当使用 Python2 运行最新的 Jupyter 时，需要保证 IPython 版本小于 6，将`pip install jupyter`替换为：

```
pip install ipython==5.0.0
pip install jupyter
```

启动 IPython 环境

```
jupyter notebook
[or]
jupyter notebook --no-browser
```

## 配置 Jupyter 默认不打开浏览器

```
jupyter notebook --generate-config
[edit ~/.jupyter/jupyter_notebook_config.py]
c.NotebookApp.open_browser = False
```

## 配置 Jupyter 允许从其他设备连入

```
[edit ~/.jupyter/jupyter_notebook_config.py]
c.NotebookApp.ip = '*'
```

## 配置 Jupyter 使用密码登录

```
mkdir ~/.jupyter
jupyter notebook password
```
