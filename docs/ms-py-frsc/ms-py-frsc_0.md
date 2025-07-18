# 前言

今天，信息技术已成为几乎所有事物的一部分，围绕我们而存在。这些系统是我们穿戴的设备，也是支撑我们建设和运营城市、公司、个人在线购物之旅以及人际关系的系统。这些系统具有吸引力，并且容易被滥用。因此，所有犯罪领域，如盗窃、欺诈、勒索等，都扩展到了信息技术领域。如今，这已经成为一个价值数十亿的、全球性的犯罪阴影产业。

一个人能发现由一个价值数十亿、犯罪、全球性的阴影产业所进行的犯罪或可疑活动的痕迹吗？嗯，有时候你是可以的。要分析现代犯罪，你不需要放大镜或从酒瓶上提取指纹。相反，我们将看到如何运用你的 Python 技能，深入查看文件系统中最有前景的地方，并从黑客留下的痕迹中提取数字指纹。

作为作者，我们相信实际示例的力量，而非陈旧的理论。这就是为什么我们提供法医工具和脚本的示例，这些示例足够简短，普通的 Python 程序员也能理解，但又是可以在实际 IT 法医工作中使用的工具和构建模块。

你准备好将*怀疑*转化为确凿的事实了吗？

# 本书内容概览

第一章，*设置实验室与 Python ctypes 介绍*，介绍了如何设置你的环境，以便跟随本书中的示例进行学习。我们将了解支持法医分析的各种 Python 模块。通过 ctypes，我们提供了一种超越 Python 模块的手段，利用本地系统库的能力。

第二章，*法医算法*，为你提供了数字版的指纹提取方法。就像经典的指纹一样，我们将向你展示如何将数字指纹与已知的好坏样本的大型数据库进行比较。这将帮助你聚焦分析，并提供法医有效性的证据。

第三章，*使用 Python 进行 Windows 和 Linux 法医分析*，是你理解数字证据之旅的第一步。我们将提供示例，帮助你检测 Windows 和 Linux 系统中存在的妥协迹象。最后，我们将通过一个例子展示如何在法医分析中使用机器学习算法。

第四章，*使用 Python 进行网络法医分析*，专注于捕获和分析网络流量。通过提供的工具，你可以搜索和分析网络流量，寻找外泄迹象或恶意软件通信的特征。

第五章，*使用 Python 进行虚拟化取证*，解释了现代虚拟化概念如何被攻击者和取证分析师使用。因此，我们将展示如何在虚拟机管理程序级别找到恶意行为的痕迹，并利用虚拟化层作为可靠的取证数据来源。

第六章，*使用 Python 进行移动取证*，将向你展示如何从移动设备中获取和分析取证数据。示例将包括分析 Android 设备和 Apple iOS 设备。

第七章，*使用 Python 进行内存取证*，展示了如何获取内存快照，并使用 Linux 和 Android 对这些 RAM 镜像进行取证分析。在 LiME 和 Volatility 等工具的帮助下，我们将演示如何从系统内存中提取信息。

# 本书的需求

本书所需的所有设备是一台配置有 Python 2.7 环境并具备正常互联网连接的 Linux 工作站。第一章，*实验室设置及 Python ctypes 简介*，将指导你安装额外的 Python 模块和工具。我们使用的所有工具均可从互联网免费下载。我们的示例源代码可从 Packt Publishing 获取。

若要跟随第五章，*使用 Python 进行虚拟化取证*的示例，你可能需要设置一个 VMware vSphere 虚拟化环境。所需的软件可以从 VMware 获取，作为时间有限的试用版，没有功能限制。

虽然并非严格要求，但我们建议在废弃的移动设备上尝试第六章，*使用 Python 进行移动取证*中的一些示例。作为首次实验，请避免使用正在使用的个人或商务手机。

# 本书适合的读者

本书适合 IT 管理员、IT 运维人员和分析师，他们希望在数字证据的收集和分析方面获得深厚的技能。如果你已经是取证专家，本书将帮助你扩展在虚拟化或移动设备等新领域的知识。

为了最大限度地利用本书，你应该具备一定的 Python 技能，并至少了解一些你取证目标的内部工作原理。例如，一些文件系统的细节。

# 术语约定

本书中你会看到多种文本样式，以区分不同类型的信息。以下是这些样式的一些示例及其含义的解释。

文本中的代码字、数据库表名、文件夹名称、文件名、文件扩展名、路径名、虚拟网址、用户输入和 Twitter 账号会这样显示：“请注意，在 Windows 中，`msvcrt` 是 MS 标准 C 库，包含大多数标准 C 函数，并使用 `cdecl` 调用约定（在 Linux 系统中，相似的库是 `libc.so.6`）。”

代码块设置如下：

```
def multi_hash(filename):
    """Calculates the md5 and sha256 hashes
       of the specified file and returns a list
       containing the hash sums as hex strings."""
```

当我们希望引起您对代码块中特定部分的注意时，相关行或项目会以粗体显示：

```
<Event ><System><Provider Name="Microsoft-Windows-Security-Auditing" Guid="54849625-5478-4994-a5ba-3e3b0328c30d"></Provider>
<EventID Qualifiers="">4724</EventID>
<Version>0</Version>
<Level>0</Level>
<Task>13824</Task>
```

任何命令行输入或输出如下所示：

```
user@lab:~$ virtualenv labenv
New python executable in labenv/bin/python
Installing setuptools, pip...done.

```

**新术语**和**重要词汇**以粗体显示。您在屏幕上看到的词汇，例如在菜单或对话框中，文本中会这样显示：“当要求**选择系统日志**时，确保选择了所有日志类型。”

### 注意

警告或重要提示会以类似这样的框显示。

### 提示

提示和技巧以这样的形式出现。

# 读者反馈

我们始终欢迎读者的反馈。告诉我们您对这本书的看法——您喜欢或不喜欢的地方。读者反馈对我们非常重要，它帮助我们开发出您真正能从中获益的书籍。

要向我们发送一般反馈，只需发送电子邮件至`<feedback@packtpub.com>`，并在邮件主题中提及书名。

如果您在某个话题上有专长，并且有兴趣编写或参与编写书籍，请查看我们的作者指南：[www.packtpub.com/authors](http://www.packtpub.com/authors)。

# 客户支持

现在，您是 Packt 书籍的骄傲拥有者，我们有一些方法可以帮助您充分利用您的购买。

## 下载示例代码

您可以从您的帐户下载所有已购买的 Packt 出版书籍的示例代码文件，网址是[`www.packtpub.com`](http://www.packtpub.com)。如果您在其他地方购买了这本书，您可以访问[`www.packtpub.com/support`](http://www.packtpub.com/support)并注册，以便将文件直接通过电子邮件发送给您。

## 勘误

虽然我们已尽最大努力确保内容的准确性，但错误仍然会发生。如果您在我们的一本书中发现错误——无论是文本还是代码中的错误——我们将非常感激您能向我们报告。通过这样做，您可以避免其他读者的困扰，并帮助我们改进后续版本的书籍。如果您发现任何勘误，请访问[`www.packtpub.com/submit-errata`](http://www.packtpub.com/submit-errata)报告，选择您的书籍，点击**勘误提交表单**链接，并输入勘误的详细信息。一旦您的勘误被验证，您的提交将被接受，勘误将被上传到我们的网站或添加到该书籍的勘误列表中。

要查看之前提交的勘误，请访问[`www.packtpub.com/books/content/support`](https://www.packtpub.com/books/content/support)，并在搜索框中输入书名。相关信息将在**勘误**部分显示。

## 盗版

互联网版权材料的盗版问题在各类媒体中普遍存在。在 Packt，我们非常重视保护我们的版权和许可证。如果您在互联网上发现任何形式的非法复制作品，请立即向我们提供网址或网站名称，以便我们采取措施。

请通过`<copyright@packtpub.com>`与我们联系，并附上涉嫌盗版材料的链接。

感谢您的帮助，保护我们的作者以及让我们能为您提供有价值的内容。

## 问题

如果您在本书的任何方面遇到问题，可以通过`<questions@packtpub.com>`联系我们，我们将尽力解决问题。
