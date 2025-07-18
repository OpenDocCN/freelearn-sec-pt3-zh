# 前言

本书全面讨论了用于识别、获取和法医分析带有 iOS 操作系统的移动设备的最先进技术，并已扩展和更新至 iOS 8 和 iOS 9。本书是一本实用指南，帮助调查人员在日常工作中有效管理这类移动设备的场景。该领域对实用指南的需求源于 iOS 设备日益普及，以及调查人员可能面临的不同场景，这些场景依据设备类型、操作系统版本以及是否存在安全系统（如密码锁、备份密码等）而不同。本书在概念上分为四个部分。第一部分处理与数字证据处理相关的方法和准则，以及特定 iOS 设备信息的基本概念。第二部分介绍了获取 iOS 设备的基本技术和工具，包括通过备份和 iCloud 的获取方法。第三部分深入探讨了数据分析的方法和技术。最后，第四部分提供了关于 iOS 应用程序和恶意软件分析的概述。对于该领域的新手，我们建议按顺序阅读本书，因为内容按照法医调查的主要阶段（识别、获取、分析）顺序处理。对于经验丰富的读者，以及那些日常处理此类设备的人员，本书可以作为评估不同技术的有用工具，具体取决于你需要处理的案件类型。

# 本书内容

第一章，*数字与移动取证*，是对数字和移动取证领域中最重要概念和定义的介绍，并涉及数字证据的生命周期，包括识别、获取、分析和报告。

第二章，*iOS 设备介绍*，包含了有用的信息和参考资料，帮助你了解如何根据设备型号和 iOS 版本识别各种类型的设备（如 iPhone、iPad 和 iPod Touch）。它还包含了有关特定设备使用的文件系统的基本信息。

第三章，*从 iDevices 获取证据*，解释了如何根据设备型号和 iOS 版本从 iOS 设备中获取数据，这些内容在前一章中有所介绍。讨论了物理、逻辑和高级逻辑获取方法，并介绍了如何破解或绕过用户设置的密码的最有效技巧。本章展示了使用各种工具获取数据的示例，并介绍了针对 iOS 8 和 iOS 9 的最新技术。

第四章，*来自 iTunes 备份的证据获取与分析*，概述了如何处理从 PC 或 Mac 上获取的 iTunes 备份的分析，重点介绍如何读取其内容以及如何尝试攻击用户设置的受保护密码。本章还解释了如何恢复设备中存储的密码，尤其是在备份没有密码保护或分析师能够破解密码的情况下。

第五章，*来自 iCloud 的证据获取与分析*，讲述了设备所有者使用 iCloud 存储设备备份的案例。你将学习如何恢复用于检索存储在 Apple 服务器上的信息的凭证或授权令牌。

第六章，*iOS 设备分析*，提供了关于如何分析已获取设备中存储数据的完整信息。包括预装应用（如通讯录、通话记录、短信、彩信和 Safari）以及第三方应用（如聊天、社交网络和云存储）的分析，特别关注核心证据及其搜索和恢复的方法。

第七章，*应用程序与恶意软件分析*，介绍了从安全角度进行应用程序评估的核心概念和工具。你还将学习如何处理可能存在于越狱设备上的移动恶意软件。

附录 A，*参考文献*，是一本完整的参考文献集，帮助你理解书中解释的一些核心概念，以便深入研究特定主题。

附录 B，*iOS 法医工具*，是一个综合性的工具集，涵盖了用于获取和分析 iOS 设备内容的开源、免费软件和商业工具。

附录 C，*自我测试答案*，包含了书中各章节提问的答案。

# 本书所需内容

本书旨在通过免费软件、开源软件和商业软件，帮助您在不同操作平台（Windows、Mac 和 Linux）之间进行操作。许多示例可以通过作者测试的软件或在附录 B 中提到的等效解决方案来复现，*iOS 法医工具*。某些具体案例需要使用商业平台，对于这些平台，我们更倾向于使用我们在日常工作中作为法医分析师所使用的平台（如 Cellebrite UFED、Oxygen Forensics、Elcomsoft iOS Forensic Toolkit 和 Elcomsoft Phone Breaker）。无论如何，我们受到易用性、提取信息的完整性和软件结果展示正确性的原则启发。本书并非以任何形式为上述软件做广告，我们鼓励您将测试从一个操作平台上的重复应用到其他平台和软件应用中。

# 本书适用对象

本书主要面向技术读者，特别是那些需要从运行 iOS 的移动设备中获取和分析信息的法医分析师（或数字调查员）。本书对于计算机安全专家和渗透测试员也非常有用，因为它涉及在商业环境中部署此类移动设备之前必须考虑的一些问题，尤其是在数据安全至关重要的情况下。最后，本书也可能对移动应用开发者感兴趣，他们可以了解在使用应用程序的设备中存储了哪些数据，从而提高安全性。

# 约定

本书中，您将看到几种文本样式，用于区分不同类型的信息。以下是这些样式的一些示例，以及它们的含义解释。文本中的代码字、数据库表名、文件夹名称、文件名、文件扩展名、路径名、虚拟网址、用户输入和 Twitter 用户名的显示方式如下：

“只需输入`make`命令即可编译源文件。”

URL 的写法如下：[`theiphonewiki.com/wiki/UDID`](http://theiphonewiki.com/wiki/UDID)

路径名写法如下：`/private/var/root/Library/Lockdown/data_ark.plist`

任何命令行输入或输出如下所示：

```
$ iproxy 2222 22
 $ ssh usb

```

新术语和重要单词会用粗体显示。在屏幕上看到的词语，例如菜单或对话框中的内容，出现在文本中时如下所示：“点击**下一步**按钮会将您带到下一个屏幕。”

### 注意

警告或重要提示会以框的形式显示，如下所示。

### 提示

提示和技巧如下所示。

# 读者反馈

我们非常欢迎读者的反馈。告诉我们你对这本书的看法——你喜欢或不喜欢的地方。读者的反馈对我们很重要，因为它帮助我们开发出真正能让你受益的标题。

要向我们发送一般反馈，只需发送电子邮件到 feedback@packtpub.com，并在邮件主题中提及书名。如果你在某个专题上有专业知识，并且有兴趣撰写或贡献一本书，请查看我们的作者指南，网址为 [www.packtpub.com/authors](https://www.packtpub.com/books/info/packt/authors)。

# 客户支持

现在你是 Packt 书籍的自豪所有者，我们有很多事情可以帮助你充分利用你的购买。

# 下载本书的彩色图像

我们还为你提供了一个 PDF 文件，其中包含本书中使用的截图/图表的彩色图像。彩色图像将帮助你更好地理解输出的变化。你可以从 [`www.packtpub.com/sites/default/files/downloads/LearningiOSForensicsSecondEdition_ColorImages.pdf`](http://www.packtpub.com/sites/default/files/downloads/LearningiOSForensicsSecondEdition_ColorImages.pdf) 下载此文件。

# 勘误

尽管我们已经尽一切努力确保内容的准确性，但错误是难免的。如果你在我们的书中发现错误——可能是文本或代码中的错误——我们将不胜感激地接受你的报告。通过这样做，你可以帮助其他读者避免沮丧，并帮助我们改进本书的后续版本。如果你发现任何勘误，请访问 [`www.packtpub.com/submit-errata`](http://www.packtpub.com/submit-errata)，选择你的书，点击勘误提交表单链接，并输入你的勘误详情。一旦验证你的勘误，你的提交将被接受，并且勘误将被上传到我们的网站或添加到该书籍的现有勘误列表中的勘误部分。要查看先前提交的勘误，请转到 [`www.packtpub.com/books/content/support`](https://www.packtpub.com/books/content/support)，在搜索框中输入书名。所需信息将显示在勘误部分下方。

# 盗版

互联网上对版权材料的盗版是各种媒体的持续问题。在 Packt，我们非常重视版权和许可的保护。如果你在互联网上发现我们作品的任何形式的非法副本，请立即向我们提供位置地址或网站名称，以便我们采取措施。请通过 copyright@packtpub.com 发送含有 suspected pirated material 链接的邮件给我们。感谢你帮助保护我们的作者和我们带给你有价值的内容的能力。

# 问题

如果你对本书的任何方面有问题，可以通过 questions@packtpub.com 联系我们，我们会尽力解决问题。
