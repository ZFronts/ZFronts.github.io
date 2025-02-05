`注1：带*为必做，其余为选做`
`注2：由于笔者在物理机上已经安装过这些，所有操作都是在win10虚拟机上进行的，但并不影响各位在Windows系统的物理机上执行相同操作`
# *一、Anaconda的下载安装及使用：
## 1、Anaconda介绍：
Anaconda是一个为AI和数据科学提供支持的平台。它提供经过严格测试和验证的数据和AI模型。通过Anaconda Navigator，用户可以更轻松地访问数据科学工具和资源。

- 轻松搜索和安装数千个数据科学、机器学习和 AI 软件包
- 从桌面应用程序管理包和环境，或从命令行工作
- 跨硬件和软件平台部署
- Windows、MacOS 或 Linux 上的分发安装

`接下来两段的内容来源于博客：`[Anaconda介绍](https://blog.csdn.net/u011125673/article/details/115295955)
因为包含了大量的科学包，Anaconda 的下载文件比较大，如果只需要某些包，或者需要节省带宽或存储空间，也可以使用Miniconda这个较小的发行版（仅包Conda和Python）。
Anaconda利用工具/命令Conda来进行package和environment的管理，并且已经包含了Python和相关的配套工具。

**我们使用Anaconda的理由在于其卓越且便捷地管理受信任Python软件包和环境的能力。在Python的高级应用中，特别是在涉及人工智能领域（如cuda、pytorch等，这些工具对Python版本和软件包版本有特定要求和限制）时，Anaconda能够轻松解决版本兼容性问题，为我们提供极大的便利。**
## 2、Anaconda的下载安装：（也可以下载Miniconda）
访问Anaconda官网[Anaconda官网下载](https://www.anaconda.com/download/success)

选择Windows操作系统进行下载。
![Image](https://github.com/user-attachments/assets/75d47b10-dceb-4b71-8fb4-332e62181cd0)
`Miniconda的下载就在Anaconda下方`
![Image](https://github.com/user-attachments/assets/a9de01bd-de4c-40a7-9f2f-feda868ca389)

下载完成后运行安装程序，安装过程见下图

![Image](https://github.com/user-attachments/assets/42f79159-1089-49c0-98e7-2e768a8fab4c)

![Image](https://github.com/user-attachments/assets/c3440437-dcdc-4a49-af53-3e810a3f826f)

`选择仅个人的话，后面可能会报错`
![Image](https://github.com/user-attachments/assets/675ff56e-5152-4006-ba1a-22f92f748a08)

![Image](https://github.com/user-attachments/assets/8ae190d5-7ce6-4891-8813-1ea73506cb5d)

![Image](https://github.com/user-attachments/assets/f2e431c2-3bbf-4ed9-9f6e-8444e74711bb)

接下来等待安装完成，安装完成后一路“Next”直到完成界面
![Image](https://github.com/user-attachments/assets/e5ac0e79-3c5a-445c-84a8-50d47fbae270)

![Image](https://github.com/user-attachments/assets/85c5f4df-4806-4217-ab70-d8eed31a43a6)

![Image](https://github.com/user-attachments/assets/96f9ac92-66e2-4212-bbbb-4bc16ab43a42)
`3、4、5均参考博客：`[最新版最详细Anaconda新手安装+配置+环境创建教程](https://blog.csdn.net/qq_44000789/article/details/142214660)
## 3、设置环境变量：
### （1）打开环境变量界面：
- Win7：应该很少人用了，所以略，可以搜索引擎搜索
- Win10：设置→系统→关于→高级系统设置→环境变量

![Image](https://github.com/user-attachments/assets/b8149eb3-2e7a-4f82-b8a1-9b4440a1fecd)

![Image](https://github.com/user-attachments/assets/98e2e015-c281-43f3-ac1e-edc164afc43b)

![Image](https://github.com/user-attachments/assets/12e668b6-4ded-4cb5-bbc7-417ee359c6d6)

![Image](https://github.com/user-attachments/assets/87fa5132-768b-4501-a0cb-9ccf8915b151)

- Win11：设置→系统→系统信息→高级系统设置→环境变量

![Image](https://github.com/user-attachments/assets/d3bab8c6-8e46-46d8-817f-dc7409db45cc)

![Image](https://github.com/user-attachments/assets/cd4eac48-4683-408f-a0c2-a73e1d870856)

![Image](https://github.com/user-attachments/assets/e14fbd8e-bfd7-4a58-a5fc-92f2fabe3dd9)

![Image](https://github.com/user-attachments/assets/89ee76e6-d231-41a0-a436-67cab09f2088)

### （2）点击系统变量的“Path”变量，双击（或点击“编辑”），打开环境变量界面：

![Image](https://github.com/user-attachments/assets/8af42623-33b0-4597-849c-2577b5bcc65e)

![Image](https://github.com/user-attachments/assets/fe95ba6a-dc0d-4844-81eb-b3b7a8296e8f)
### （3）点击“新建”（知道安装目录相关路径的情况）或“浏览”（不知道安装目录相关路径的情况，推荐）：
新建Anaconda的4个相关路径：
- ~（安装目录根目录）
- \Scripts
- \Library\bin
- \Library\mingw-w64\bin

![Image](https://github.com/user-attachments/assets/ff621b9c-1e96-4ac3-abcd-eccd3df99f7f)
然后点击一路点击确认
### （4）验证：
“Win+R”打开运行窗口，输入“cmd”打开命令行窗口

![Image](https://github.com/user-attachments/assets/764deb6f-e5da-4aae-b12f-992bfb32c746)

输入“conda --version”命令，出现版本号即为设置成功
```shell
conda --version
```

![Image](https://github.com/user-attachments/assets/1af9f5d9-8dcb-4188-92c0-7cbc8183f52a)

## 4、Anaconda默认环境保存路径更改：
**没有修改的conda的pkgs和envs均保存在C盘，为了不占用系统盘的空间，我们需要修改保存的位置**
在C:/用户/用户名，找到.condarc文件，如果找不到打开cmd命令行输入以下命令
```shell
conda config --set show_channel_urls yes
```

![Image](https://github.com/user-attachments/assets/7b870b90-0168-44e2-8d22-2a82d5eb0db1)

使用**记事本**打开.condarc文件

![Image](https://github.com/user-attachments/assets/c0914343-8e47-48eb-8ab8-c9ce2056aaba)

 **删除其他的**，输入以下内容【注意修改为自己想要安装的盘，我这里修改为E盘】
```
envs_dirs:
  - E:\anaconda3\envs
pkgs_dirs:
  - E:\anaconda3\pkgs
```

![Image](https://github.com/user-attachments/assets/6d605ec1-5f6b-4ca5-b04d-173721cfd46c)

保存后关闭，在cmd命令行窗口中输入以下命令查看是否更改成功
```shell
conda info
```

![Image](https://github.com/user-attachments/assets/c73412c0-7b64-43c6-9179-8c082728a19b)
<ins>修改前为</ins>

![Image](https://github.com/user-attachments/assets/15e85dbc-d7e7-4491-bfef-40f143ec0b27)

## 5、Anaconda换源：
因为conda很多下载的东西在国外，默认的下载速度往往会很慢，这里建议修改为清华的镜像源（其它源如豆瓣源等请自行搜索）
打开cmd命令行窗口，输入以下命令（选一个源输入即可）
```
# 添加清华源
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/conda-forge/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/pytorch/
 
# 添加阿里云镜像源
conda config --add channels https://mirrors.aliyun.com/anaconda/pkgs/free/
conda config --add channels https://mirrors.aliyun.com/anaconda/pkgs/main/
 
# 添加中科大源
conda config --add channels https://mirrors.ustc.edu.cn/anaconda/pkgs/free/
conda config --add channels https://mirrors.ustc.edu.cn/anaconda/pkgs/main/
conda config --add channels https://mirrors.ustc.edu.cn/anaconda/cloud/conda-forge/
conda config --add channels https://mirrors.ustc.edu.cn/anaconda/cloud/msys2/
conda config --add channels https://mirrors.ustc.edu.cn/anaconda/cloud/bioconda/
conda config --add channels https://mirrors.ustc.edu.cn/anaconda/cloud/menpo/
 

# （可选）设置搜索时显示通道地址
conda config --set show_channel_urls yes
```

![Image](https://github.com/user-attachments/assets/b70932a5-a917-4695-936d-c1d0fb3fb051)

`参考博客：`[Anaconda conda常用命令：从入门到精通](https://blog.csdn.net/chenxy_bwave/article/details/119996001)
## 6、Anaconda常用命令：
基本上都可以在cmd命令行窗口中使用以下指令查询conda命令用法
```
conda -h
```

![Image](https://github.com/user-attachments/assets/dd6f5420-2dd6-4bb7-b23f-8843d9dda721)

以下列出几个最常用的
- 查看conda版本
```
conda --version
```
- 更新conda
```
conda update conda
```
- 查询某个命令的帮助
```
conda 具体命令 --help
```
- 创建虚拟环境
```
conda create -n 虚拟环境名 python=Python版本
```
这表示创建python版本为3.8、名字为env_name的虚拟环境。

创建后，env_name文件可以在Anaconda安装目录envs文件下找到。在不指定python版本时，自动创建基于最新python版本的虚拟环境
- 删除虚拟环境
```
# 删除指定虚拟环境及其中所有安装的包
conda remove --name 虚拟环境名 --all
# 删除指定虚拟环境中指定的包
conda remove --name 虚拟环境名 包名
```
- 查看有哪些虚拟环境
以下三条命令都可以
```
conda env list
conda info -e
conda info --envs
```
- 激活虚拟环境
```
conda activate 虚拟环境名
```
- 退出虚拟环境
```
conda deactivate
```
- 查询包的安装情况
```
conda list
```
- 包的安装和更新
```
# 安装最新版本的包
conda install 包名
# 安装某个特定版本的包
conda install 包名=版本号
# 将某个包更新到它的最新版本
conda update 包名
```
- 包的卸载
```
conda uninstall 包名
```
## 7、使用：
**按照上述流程配置好的Anaconda在cmd命令行窗口时是不会自动激活使用的**（Win11自带的wt终端会自动激活使用）
所以我们需要执行以下命令：
```
# 第一次运行的话需要先执行conda init
conda init
# [base]代表可选
conda activate [base]
```

![Image](https://github.com/user-attachments/assets/2dd5368b-07aa-417c-8a85-bec1a482980f)

或者在应用菜单中找到“Anaconda Prompt应用”

![Image](https://github.com/user-attachments/assets/7edb40d0-6532-4fd8-9a9d-e17fe26a3796)

# *二、Visual Studio Code的下载安装及使用：
## 1、Visual Studio Code介绍：
Visual Studio Code（简称 VS Code）是由微软开发的一款免费、开源、跨平台的代码编辑器，适用于 Windows、macOS 和 Linux 系统。它结合了轻量级编辑器的灵活性和集成开发环境（IDE）的强大功能，逐渐成为开发者中备受欢迎的工具之一。

**核心特点**
- 轻量且高效：
        启动速度快，占用系统资源少，适合快速编辑或大型项目开发。
        原生支持多种编程语言（如 JavaScript、Python、Java、C++ 等），通过扩展可支持更多语言。
- 强大的扩展生态系统
        市场（Extensions Marketplace）提供数千款插件，涵盖调试、主题、代码补全、版本控制等功能。
        热门扩展：Python、Prettier（代码格式化）、GitLens（Git 增强）、Live Server（实时网页预览）等。
- 智能代码辅助
        IntelliSense：基于上下文自动补全代码，支持变量、函数名和模块的智能提示。
        语法高亮、代码折叠、错误检查（Linting）等功能提升编码效率。
- 集成调试工具
        内置调试器，支持断点、变量监视、调用堆栈跟踪，可直接调试 Node.js、Python、C# 等语言。
        通过扩展支持更多调试场景（如浏览器调试）。
- Git 版本控制集成
        直接可视化操作 Git，支持提交、拉取、推送、分支管理、冲突解决等功能。
- 终端与任务运行
        内置终端（支持 PowerShell、CMD、Bash 等），可直接运行脚本或命令。
        可配置任务（Tasks）自动化构建、测试流程。
- 高度可定制
        主题和图标包自由更换（如 Material Theme、One Dark Pro）。
        用户设置（JSON 文件）支持键盘快捷键、界面布局、功能开关的个性化配置。
- 跨平台协作
        Live Share 功能支持多人实时协作编辑和调试，类似远程结对编程。

**适用场景**
- Web 开发：前端（HTML/CSS/JavaScript）、后端（Node.js、Python、PHP）开发。
- 脚本与自动化：Python、Shell、PowerShell 等脚本编写。
- 数据科学：通过扩展支持 Jupyter Notebook、数据可视化。
- 云开发：集成 Azure、Docker、Kubernetes 等工具。
## 2、VS Code的下载安装：
访问VS Code官网[VS Code官网下载](https://code.visualstudio.com/Download)

选择Windows操作系统进行下载。

![Image](https://github.com/user-attachments/assets/645fdba3-c363-4063-be75-5ec969cde19c)

下载完成后运行安装程序，安装过程见下图

![Image](https://github.com/user-attachments/assets/cb393099-1322-4086-b949-467500982de7)

![Image](https://github.com/user-attachments/assets/ff795e66-eb54-4631-b0bf-9756fa8395ad)

![Image](https://github.com/user-attachments/assets/43e6cfa4-5ef3-4dd4-b451-1f84640b7e9d)

![Image](https://github.com/user-attachments/assets/f73a6145-3028-488a-b7e7-e27dcb86d6c3)

![Image](https://github.com/user-attachments/assets/911d7d11-5e27-4edf-ba4f-2733bdaa1930)

![Image](https://github.com/user-attachments/assets/a6028658-0479-4f39-8f2b-1136252da537)

## 3、VS Code的配置：
### （1）中文设置：
如下图所示操作
![Image](https://github.com/user-attachments/assets/c7475514-caf7-428e-ae1e-7fb2a628f6bd)

![Image](https://github.com/user-attachments/assets/63368200-448e-4008-97af-fd95630baf97)
重启后即为中文界面

![Image](https://github.com/user-attachments/assets/a5115d59-0f75-4ede-b9f2-981fdf94a0ab)

### （2）自动保存设置：
打开设置界面
![Image](https://github.com/user-attachments/assets/3ec71acb-c793-4a19-8089-39a64f519f79)
将自动保存设置为“**onFucusChange（当VS Code失去鼠标焦点时）**”

![Image](https://github.com/user-attachments/assets/eeec895e-d17c-4284-9979-28c3a785d80f)

![Image](https://github.com/user-attachments/assets/57c664ea-eb96-4b8b-943d-659e75fce904)

### （3）Python插件安装：

![Image](https://github.com/user-attachments/assets/42bc94b5-4e6b-4d79-b0ec-1a75cd12793a)

安装完成后需要重启VS Code
### （4）Python解释器设置：
在命令栏中输入
```
>Python:Select Interpreter
```

![Image](https://github.com/user-attachments/assets/82739a66-1505-4389-9bd5-80ed8e6ad626)

![Image](https://github.com/user-attachments/assets/7353a097-23e9-4169-8cc9-5dc1af214a30)

## 4、使用VS Code运行Python程序：
### （1）编写.py文件：
先新建一个文件夹，并打开
![Image](https://github.com/user-attachments/assets/60ab37a6-99ee-47af-8fc2-d89eb70b311c)

![Image](https://github.com/user-attachments/assets/df94d94d-44a5-40da-9832-b2f021f65c18)

再新建一个.py文件
![Image](https://github.com/user-attachments/assets/a8377fe3-f815-4e54-8e15-e8cf91961eb7)

输入以下代码
```python
print('Hello World!')
```

![Image](https://github.com/user-attachments/assets/a5d524ac-6217-4a1d-a917-f11be260d1c9)

### （2）运行.py文件
有三种运行方法
一种是**在终端中输入命令**运行，如图所示打开终端，并输入以下命令（**这种方法需要注意命令执行的路径**）：

![Image](https://github.com/user-attachments/assets/28532d0e-668d-4104-80c7-f150dcc19e9c)

```
# *指自己创建的.py文件名，笔者这里为test
python *.py
```

![Image](https://github.com/user-attachments/assets/a0026261-8f7b-4c0f-8320-ee7732365a77)

第二种是**直接点击运行**，如下图所示：

![Image](https://github.com/user-attachments/assets/4bac126d-ba85-4118-a6bc-805de986f3e7)

第三种是“右键运行”（任选其一，有不同的效果，在终端中运行的效果和方法二一致），如下图所示：

![Image](https://github.com/user-attachments/assets/48bf9b78-ced3-4779-a930-d999263f5c58)

![Image](https://github.com/user-attachments/assets/abc36577-85ca-4eec-8452-8b35c0f7b2a1)

# 三、Python官方IDLE的下载安装及使用：
`注：其实Anaconda搭建的虚拟环境中也有IDLE的应用程序，但是没法正常启动，所以如果需要使用IDLE，需要本地再下一个Python`
## 1、Python官方IDLE介绍：
IDLE（Integrated Development and Learning Environment）是 Python 官方默认捆绑的轻量级 IDE，适合初学者学习和简单脚本开发。
另外，**NCRE-2的Python以及各编程比赛Python赛道基本都要求使用官方的IDLE进行编程**，所以熟练掌握IDLE的使用也很有必要。

**主要功能**：
- 交互式 Shell：
        类似 Python 命令行，可直接运行代码片段并查看结果。
- 代码编辑器：
        支持语法高亮、自动缩进、基础代码补全。
- 调试功能：
        提供简单的断点调试工具（但功能有限）。
- 跨平台：
        支持 Windows、macOS 和 Linux。

**优点**：
- 轻量、无需额外安装。
- 适合新手快速上手 Python 语法。

**缺点**：
- 功能简陋，缺乏现代 IDE 的智能提示、版本控制集成等。
- 界面较为老旧，扩展性差。
## 2、Python官方IDLE的下载安装：
访问Python官网[Python官网下载——Windows](https://www.python.org/downloads/windows/)

选择稳定版本的**Windows installer (64-bit)**进行下载（笔者这里下载的是3.13.2，一般下载最新的，或者其它稳定大版本如3.7、3.8等的最新版）。

![Image](https://github.com/user-attachments/assets/8de6d1f0-0708-4b87-9e25-934859ddaae1)

**如果觉得浏览器下载得慢可以复制下载链接到迅雷里下载**

下载完成后运行安装程序，安装过程见下图

![Image](https://github.com/user-attachments/assets/5e57c8f5-16fa-455b-85c2-d3aae67fbb37)

![Image](https://github.com/user-attachments/assets/d516a78b-c56f-4d14-a809-27d35cebdea1)

![Image](https://github.com/user-attachments/assets/86566855-09a5-4c4b-9505-39b4da5574d6)

![Image](https://github.com/user-attachments/assets/41ab741e-f933-4462-bbe8-f767e5612c18)

## 3、官方Python命令行的使用：
- 在没安装Anaconda的情况下，按“Win+R”打开命令行窗口，输入“python”（或输入cmd，再在命令行窗口输入python）即可快速启动官方Python的命令行。

![Image](https://github.com/user-attachments/assets/5ab68c30-e03c-4cbd-8f11-f801b8d52160)

- 在按照前述过程安装了Anaconda的情况下，上述过程启动的是Anaconda的base虚拟环境的python的命令行

![Image](https://github.com/user-attachments/assets/1281e9f9-35eb-4ea0-94a0-f07182e17363)

这时如果我们需要使用官方Python的命令行，就只能在应用菜单中启动（或者修改系统变量，但比较麻烦也没必要）

![Image](https://github.com/user-attachments/assets/6e89ab2d-41a5-4d05-9b13-b05fe413672b)

![Image](https://github.com/user-attachments/assets/a8836ce2-08a1-4380-aad3-a36b894faaff)

## 4、IDLE的使用：
### （1）运行：
在桌面没有设置快捷方式的情况下，建议在应用菜单中启动

![Image](https://github.com/user-attachments/assets/944b85c8-525f-4424-9381-42785f9c5ab7)

### （2）IDLE命令行：
IDLE刚启动的界面是主界面，用法和cmd命令行一样，区别在于IDLE有代码高亮

![Image](https://github.com/user-attachments/assets/61ace788-ff95-4ad2-a6c0-206a859927b2)

### （3）IDLE对.py文件的编写和运行：
点击菜单栏的“File”→“New File”，会弹出一个空白界面，用于编写.py文件

![Image](https://github.com/user-attachments/assets/ce95a5e3-d151-419a-96a4-e024bfb57faa)

![Image](https://github.com/user-attachments/assets/80c66712-fc12-4696-a366-9c59a1a22c07)

假如我们要编写一个用户输入n，返回计算1+2+……+n的和的程序，代码如下：
```python
n = int(input("请输入整数n："))
sum = 0
for i in range(1, n + 1):
    sum += i
print("1+2+……+n的和为%d"%sum)
```

![Image](https://github.com/user-attachments/assets/e7e08d45-da68-4cd9-a977-b6d02d07a52b)

编写完之后记得按快捷键“Ctrl+S”保存（或者点击菜单栏的“File”→“Save”）

![Image](https://github.com/user-attachments/assets/f20b89ee-a117-4144-83a7-52410c351816)

首次保存需要选择保存路径并设置文件名

![Image](https://github.com/user-attachments/assets/97a47eec-75ff-4ee4-a0d4-b552d64866f4)

保存之后再运行（**如果没保存就运行，运行的是上一次保存的代码**）
运行需要按快捷键“F5”（或者点击菜单栏的“Run”→“Run Module”）

![Image](https://github.com/user-attachments/assets/be890b6c-783d-4d4a-9a43-8b6465f8243c)

![Image](https://github.com/user-attachments/assets/ce630d95-713d-45c4-9c03-59c71ee7c145)

# 四、PyCharm的下载安装及使用：
## 1、PyCharm介绍：

![Image](https://github.com/user-attachments/assets/91fb92b9-46bd-45ce-aaf4-935337cb3500)

## 2、PyCharm的下载安装：
PyCharm有社区版（Community）和专业版（Professional）两个版本，这里以专业版为例（可以免费试用30天，建议还是申请个学生认证，申请方式可以参考博客：[高校学生免费使用jetbrains产品指南（保姆级教程）](https://blog.csdn.net/m0_63451989/article/details/131743070)）

访问PyCharm官网[PyCharm官网下载](https://www.jetbrains.com/pycharm/download/?section=windows)

选择Windows操作系统进行下载。

![Image](https://github.com/user-attachments/assets/e62513d3-9539-4569-9901-3801e33caf87)

下载完成后运行安装程序，安装过程见下图

![Image](https://github.com/user-attachments/assets/5d7c43a2-2c0b-4eae-861f-0c1b228a469e)

![Image](https://github.com/user-attachments/assets/e5e709b2-137b-4e67-9c3a-27f936ae5a2d)

![Image](https://github.com/user-attachments/assets/7d7596a1-a57d-4191-abaf-63aa7a058790)

![Image](https://github.com/user-attachments/assets/d44c3a7b-93f0-414e-891f-5b4f17e5d633)

![Image](https://github.com/user-attachments/assets/bb38b943-500d-4714-9f81-990b6eb266ed)

## 3、PyCharm的配置：
运行PyCharm，选择语言和地区，默认即可

![Image](https://github.com/user-attachments/assets/2f859f07-20d2-4f3b-ad29-1d09813b0efc)

![Image](https://github.com/user-attachments/assets/623ab83e-0447-469b-9986-94bbcae189a9)

![Image](https://github.com/user-attachments/assets/3fb15bba-68c6-4f5c-b5b7-aa1d6ec61676)

![Image](https://github.com/user-attachments/assets/857b593b-b682-45dc-9776-eebeb57e3f07)

后面选“跳过导入”
## 4、PyCharm的使用：
### （1）新建项目：
![Image](https://github.com/user-attachments/assets/fd8cda8b-576f-4e32-a3d8-d7cb0993404f)

![Image](https://github.com/user-attachments/assets/3b81a4b9-d0a3-4e60-9435-3932f3422e99)

![Image](https://github.com/user-attachments/assets/ab291158-5d79-4d3c-a828-8c89d52dfc36)

![Image](https://github.com/user-attachments/assets/670adb75-eb18-48f4-a283-5fdc3ff343fb)

![Image](https://github.com/user-attachments/assets/99b094c5-3942-4660-a16c-28ed6337ee88)

### （2）运行.py文件：

![Image](https://github.com/user-attachments/assets/bf5657bb-ae64-4999-86d2-21a7ab54be72)