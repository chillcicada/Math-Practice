# Math Practice

> 大学数学实验的相关内容

## features

- Pure Python
- Jupyter Lab instead of jupyter notebooks, with almost all scientific computing languages or DSLs
- Quarto, for directly rendering documents from Jupyter notebooks
- Typst, use typst instead of latex for better document rendering
- ...

## setup

> git clone / degit / download zip
>
> 请确保您已正确配置 python 环境

配置虚拟环境（use powershell as default）：

```ps1
cd "/path/to/this/folder"
python -m venv .venv
.venv/scripts/activate.ps1
# or use bash
# .venv/scripts/activate
# or use cmd
# .venv/scripts/activate.cmd
```

配置依赖（use powershell as default）：

```ps1
# 最小环境依赖
# minimal environment
pip install jupyter scipy matplotlib
```

可选配置：

```ps1
# 用于 vsc / pycharm 渲染长列表
pip install pandas
```

```ps1
# 用于 lint / format
# 由于我是全局启用 ruff，你也可以在全局环境中安装
pip install ruff
```

> [!IMPORTANT]
> 如果您需要为本项目做贡献，`ruff` 和 `pre-commit` 是必须的，可以运行下面的命令来安装环境：

```ps1
pip install -r requirements.txt
# 这将安装 jupyter scipy matplotlib pre-commit 和 ruff
```

---

配置 JupyterLab 和 Quarto （用于渲染文档，可选）

> 推荐此部分使用 vscode 作为编辑器，vscode 提供了更好的文档相关支持
>
> - Jupyter 插件包，提供 Jupyter in vscode LSP 本体
> - python 插件包，推荐使用 vscode 官方的配置，提供 python 语言支持
> - Quarto 插件，提供 Jupyter in vscode 扩展
> - Tinymist LSP 和 Typst Preview，提供 Typst 的相关服务（可选，源于 quarto 的 latex 导出功能并不好，因而推荐 typst 导出 pdf）

```ps1
# quarto for jupyterlab
pip install jupyterlab-quarto
# enable quarto
jupyter labextension install jupyterlab-quarto
# 中文支持
pip install jupyterlab-language-pack-zh-CN
# enable locale zh
jupyter lab --locale=zh-CN
```

你也可以运行 `jupyter lab` 来启动 JupyterLab，并在 ui 界面配置相关插件

## appendix

### matlab in jupyterLab / vscode

> refer to [mathworks official documentation](https://ww2.mathworks.cn/help/matlab/matlab_external/install-the-matlab-engine-for-python.html)

```ps1
cd "<matlabroot>\extern\engines\python"
# recommended
python -m pip install .
# or, this requires you add global python scripts path to the system environment
# pip install matlabengine
# or in old version
# python setup.py install
```

in vscode, you can add and config the extension `Matlab` and `Matlab in VSCode` to enable matlab language support

in jupyterlab, you can run `pip install jupyter-matlab-proxy` to add matlab kernel support, refer to [repo](https://github.com/mathworks/jupyter-matlab-proxy)

## acknowledgement

- pycharm and vscode
- jupyterlab
- quarto
- typst

# license

MIT

!!自己的作业自己做!!
