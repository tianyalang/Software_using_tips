# VS Code

[toc]

## 快捷键

+ `Ctrl + Shift + L` 相同内容，多选，实现同时修改
+ `Alt+鼠标左键` 自由多光标，实现多位置光标处同步编辑
+ `Alt + Shift + 鼠标左键` 长光标，实现按列编辑

## 配置

### 三个json配置文件的作用

+ tasks.json 单次运行一个脚本视为一个 task,相应的配置文件为 tasks.json
+ settings.json 整个文件夹或者多个文件夹视为一个工作空间,配置文件为 settings.json
+ launch.json 调试环境的配置文件叫 launch.json

这些配置文件是需要手动编辑的, 编辑完保存好就会替代默认的配置文件生效

### 配置 markdown

原生只支持渲染基本语法，不包括**公式、mermaid**
三个插件

+ Markdown All in One: 公式代码提示
+ Markdown Preview Enhancde: mermaid 画图支持
+ markdownlint: 代码规范提示

### 配置 python

#### 相对路径无效的问题

```python
import os, sys
os.chdir(sys.path[0])    # 相对路径指定到当前文件的同级，默认是根文件夹
```

#### python 调试bug

**进入调试模式，调试条很快消失**
用户设置和工作空间设置中，均不指定python解释器路径，可正常调试
调用 pdb/ipdb模块调试，似乎更方便

断点打在空行，无效

## 代码格式化

配置`flake8`和`yapf`并关闭`pylint`工具。
在工作区域输入以下内容：

```json
{
"python.linting.flake8Enabled": true,
"python.formatting.provider": "yapf",
"python.linting.flake8Args": ["--max-line-length=248"],
"python.linting.pylintEnabled": false
}
```
