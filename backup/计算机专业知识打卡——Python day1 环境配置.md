`注1：带*为必做，其余为选做`
`注2：由于笔者在物理机上已经安装过这些，所有操作都是在win10虚拟机上进行的，但并不影响各位在Windows系统的物理机上执行相同操作`
# *一、下载安装Anaconda：
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

![Image](https://github.com/user-attachments/assets/1af9f5d9-8dcb-4188-92c0-7cbc8183f52a)

## 4、Anaconda默认环境保存路径更改：
**没有修改的conda的pkgs和envs均保存在C盘，为了不占用系统盘的空间，我们需要修改保存的位置**
## 5、Anaconda换源：
## 6、Anaconda基础命令：
# *二、下载安装Visual Studio Code：