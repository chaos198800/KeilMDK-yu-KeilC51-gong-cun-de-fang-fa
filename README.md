# Keil MDK 与 Keil C51 共存的方法

在嵌入式开发领域，Keil MDK（主要用于ARM Cortex-M系列等MCU）和Keil C51（针对8051系列MCU的开发）都是不可或缺的工具。当开发者需要在这两者之间切换时，可能会遇到软件之间的冲突。但无需担心，本文档提供了详细的步骤，帮助您在同一台计算机上顺利安装并共存这两款软件。

## 安装与配置指南

### 1. 软件准备
- 确保从官方渠道或可靠的来源下载Keil MDK和Keil C51的安装包。
- 注意：为了避免后续的路径冲突，我们强烈推荐使用本文档的安装顺序。

### 2. 安装步骤
#### Keil C51 安装
1. **启动安装**：首先，运行Keil C51的安装程序。
2. **自定义路径**：在安装向导中，更改默认安装路径至比如`C:\Keil_C51`。
3. **完成安装**：遵循屏幕指示直至安装完毕，避免自动启动软件。

#### Keil MDK 安装
1. **后续安装**：紧接着安装Keil MDK，使用默认路径`C:\Keil_v5`或保持与C51相同的自定义路径结构。
2. **特别注意**：安装MDK时，不要覆盖C51的安装。

### 3. 共存配置
- **文件转移与合并**：手动将C51安装目录下的`C51`文件夹复制到MDK的安装目录中。
- **修改配置**：进入两个版本的`UV4`文件夹，复制C51的UV4文件至MDK的UV4目录，对于同名文件选择跳过。
- **编辑TOOLS.INI**：在MDK安装目录下，打开`TOOLS.INI`文件，并将C51的相关配置追加到底部，记得调整路径至正确位置。

### 4. 注册与激活
- **CID提取**：分别在两版本中打开“License Management”，提取CID。
- **使用注册机**：利用对应的注册机生成序列号，分别为C51和MDK进行注册。

### 完成
按照上述步骤，您将能在同一Keil环境下无缝地切换C51和MDK的编译器，大大提升了开发效率。记住，每个步骤都很重要，尤其是配置文件的修改，以确保软件能正确识别和使用相应的组件。祝您的嵌入式开发之路更加顺畅！

## 下载链接

[KeilMDK与KeilC51共存的方法](https://pan.quark.cn/s/5ba1f3505c5b)