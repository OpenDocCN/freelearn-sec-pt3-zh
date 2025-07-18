# 第七章：掌控安全操作

你已经实施了自己心中对卓越且持续改进的信息安全战略的愿景，并且采取了适当的控制措施，以确保你的组织安全且合规。做得很好！接下来，你打算如何保持对事情的掌控？在发生安全事件或事故时，你将如何调查？我们需要做什么才能确保在线运作，保持组织资产的可用性，并使员工能够不受干扰地进行日常工作？本章专注于安全操作这一永无止境的任务，以及它如何与组织的商业愿景对齐。

本章将讨论以下主题：

+   配置资源和维护资产的有效策略

+   聚焦于可用性、灾难恢复和业务连续性活动

+   管理升级、打补丁及应用安全控制

+   事件调查与事故响应

+   实施和利用侦测控制

+   使用安全监控提高可见性

+   安全监控最佳实践

让我们开始吧！首先，我们来看看配置资源和维护资产的一些有效策略。

# 配置资源和维护资产的有效策略

Automox 在 500 至 25,000 名员工的公司中进行了一项调查，超过 500 名 IT 和信息安全专业人士回答了相关问题（[`www.darkreading.com/vulnerabilities---threats/missing-patches-misconfiguration-top-technical-breach-causes/d/d-id/1337410`](https://www.darkreading.com/vulnerabilities---threats/missing-patches-misconfiguration-top-technical-breach-causes/d/d-id/1337410)）。Automox 发现，过去两年内，超过 80%的公司曾遭遇过安全 breaches，以下数字显示了在这些攻击中被利用的漏洞类型：

+   操作系统补丁缺失（30%）

+   应用程序补丁缺失（28%）

+   操作系统配置错误（27%）

在成功的网络钓鱼攻击或凭证收集后，通常会发生一连串事件，这些事件往往会利用前面提到的某个漏洞。关键是，我们可以通过提供经过批准的配置并确保资产得到维护（包括操作系统和应用程序补丁与更新）来防止这种情况发生。

本节将讲解我们如何确保在整个生命周期内，资产始终得到维护并保持最新。这个过程是持续的，但它能节省时间和精力，并确保组织能够创新其产品，而不是单纯地应对信息安全威胁并急于更新遗留软件。

## 资源配置

在数字资产中，信息系统不断地被添加、移除和修改。不幸的是，这通常是没有任何监督或缺乏最佳实践指导的情况下进行的。

当我们将新资产添加到我们的资产池时，涉及什么样的流程？我们是否“只是做了”，没有定义更广泛的策略？我们对资产版本或操作系统有何种可视化？

此外，在云计算时代，部署只需要在浏览器中点击几下按钮，我们如何避免**影子 IT**（在没有 IT 部门批准的情况下使用系统、设备、软件或其他 IT 解决方案），并确保当组织中的员工“启动一个新服务器”时，遵循我们的流程，并考虑到我们的信息安全策略？

### 政策

随着你在本书中的阅读进展，你已经习惯了我对政策的看法：在信息安全政策文档中定义你的方法的力量是至关重要的。信息系统的配置和维护也同样如此。我们需要具体指导用户找到正确的答案。你不一定需要在政策文档中直接定义“批准”的操作系统版本或应该禁用哪些功能；事实上，我建议不要这样做，因为这将需要不断更新以保持相关性。

你可以指向一个不断更新的资源，类似于“批准的操作系统版本和配置可以在这里找到：<link>。” 然后，在链接的文档中，可以更新并根据你的策略调整信息，无需维护文档，同时确保每个人都能获取到正确的信息安全政策版本。

### 配置管理

当我们查看上述包含“批准”配置的链接时，应该如何处理？我们从哪里获取“良好”的配置？如何定义我们组织需要什么，以确保操作的持续性？

幸运的是，市场上有**软件配置管理**（**SCM**）工具。常见的选择包括以下几种：

+   Microsoft **系统中心配置管理器** (**SCCM**)，或**配置管理器**

+   **SolarWinds 服务器配置监控器**

+   **Ansible**/**Ansible Tower**

+   **Puppet**

+   **Chef**

这些工具提供各种功能，包括以下内容：

+   远程管理

+   补丁管理

+   软件分发

+   操作系统部署

+   配置管理

+   维护每个资产的软件和硬件清单

作为信息安全专业人员，这可以从多个方面帮助你。考虑到你现在拥有一份资产清单，以及每个资产使用的软件。这可以帮助你完善资产和风险登记表，并提供每个资产的实时准确信息，同时简化如审计等特定时间点的评估。通过配置管理，我们还确保记录所有更改，以便于轻松排查配置错误、停机、性能下降和不符合标准的来源，并提高系统的可审计性。

此外，我们有可用的治理结构，以便设置基准配置并实施变更控制流程，确保对生产系统的任何更改都是以系统化、计划好的方式进行的。通过实施这些治理控制措施，例如要求管理员在进行系统或网络配置更改之前验证所做的更改（*职务分离*），你可以降低配置错误导致停机或安全漏洞的风险。

运营员工可能会对建立治理结构提出反对意见，抱怨例如“这与我们以前的工作方式相悖”或“这会让我们变慢”。请记住，从组织的角度来看，节省的时间（无需恢复系统）、节省的费用（避免违反**服务水平协议**）、防止声誉损害以及在确保系统得到适当维护并设置了检查和制衡的情况下放心前行的心态，将弥补在变更时可能出现的轻微速度损失（如果真有速度损失的话）。流程的自动化可以帮助消除障碍，防止许多员工预测的那种麻烦。

当我们考虑有效使用配置管理工具时，应考虑以下实践：

+   确保将系统分类并分组到对组织有意义的分类法中。这些类别和子类别可以批量更改，因此请确保你和你的同行架构师在设计时考虑到这一点。

+   我们需要定义“已批准”的基础配置，并记录每个配置的理由和标签。像**互联网安全中心**（**CIS**）这样的组织提供“加固镜像”。这些操作系统和应用镜像很可能已经符合安全配置指南，比如 CIS 基准，能够快速、轻松地在云环境和本地环境中部署安全系统，而无需自行定义要求。更多信息可以参考[`www.cisecurity.org/cis-hardened-images/`](https://www.cisecurity.org/cis-hardened-images/)。

+   在更改系统时，所有关于更改的信息（用户、时间、所做更改、受影响的系统）应当被记录和追踪，并且过程应当遵循有效的*职责分离*原则，以确保没有个人能够做出破坏性更改。

+   确保测试环境和生产环境之间的一致性，包括操作系统、软件版本、网络配置等。环境越对齐，当变更推向生产时，出现停机或未发现漏洞的可能性就越小。

+   在出现故障的情况下，还可以自动化回滚或修复的过程。

话虽如此，许多组织正在向一种名为**基础设施即代码**（**IaC**）的理念转变，这与**DevOps**和**持续集成/持续部署**（**CI/CD**）的 IT 管理和软件开发方法密切相关。让我们来看一下 IaC 的优势。

#### 基础设施即代码

有一个叫做 IaC 的概念，从安全角度和 IT 运维角度来看，它都是一种非常有益的方法。IaC 的基本思想是，您的基础设施不再仅仅是特定位置的物理服务器，而是越来越趋向于完全虚拟化、分布式的云环境。因此，您不再需要配置、管理、扩展和停用物理硬件，或者使用传统的、专为这些硬件设计的交互式配置管理工具，而是可以在*机器可读文件*中定义您的基础设施和所有信息处理设施，这些文件像软件代码一样*版本化*并更新，供自动化软件在无需人工干预的配置/扩展/停用过程中引用。

这个想法与**DevOps**和**CI/CD**实践紧密相关，而不是传统的 IT 运维与软件开发人员之间的分离。*IaC*的目标，以及大多数*DevOps*和*CI/CD*实践的目标，都是通过减少错误频发的手动流程，提升改进的速度，加快部署并提高效率，从而部署更高质量的软件。

在我们讨论 IaC 工具和格式之前，我想提到的是，IaC 范式通常涉及利用容器和编排软件，如**Docker**和**Kubernetes**。

**Docker** 根据**Dockerfile** 中定义的指令构建*容器镜像*，Dockerfile 是一个文本文件，包含构建系统镜像所需的所有命令（例如应用程序及其依赖项），这些镜像被称为**容器**。容器是虚拟机的轻量级替代品，它们已经与运行它的服务器底层基础设施解耦。因此，一个服务器可以运行基于数千种不同配置的容器，每个容器可能包含不同的操作系统和软件包。关于 Docker 工作原理的进一步阅读可以在这里找到：[`docs.docker.com/get-started/overview/`](https://docs.docker.com/get-started/overview/)。

关于如何定义和编写*Dockerfiles*的进一步阅读可以在这里找到：[`docs.docker.com/develop/develop-images/dockerfile_best-practices/`](https://docs.docker.com/develop/develop-images/dockerfile_best-practices/)

**编排软件**，如**Kubernetes**，有助于自动化在分布式环境中部署这些*容器*，并帮助管理、部署和扩展容器的操作方面。编排软件行为的基础配置通常定义在**YAML**文本文件中，并且可以通过前端 Web 应用界面或命令行工具进一步修改。有关 Kubernetes 的进一步阅读可以在这里找到：[`kubernetes.io/docs/concepts/overview/what-is-kubernetes/`](https://kubernetes.io/docs/concepts/overview/what-is-kubernetes/)。

你可能会问：“我为什么要简要探讨这些内容？”我想从信息安全的角度突出一个要求，那就是紧跟你组织运作方式的变化。IT 变化极快，理解新技术背后的概念非常重要，以确保流程和解决方案的安全性。在这个例子中，应考虑如何确保这些工具和文本文件进行安全性检查并进行版本控制。这些新的软件打包和部署方式正在逐渐成为你组织基础设施建设的方式，如果没有你组织定义的适当治理和流程，它们可能为恶意行为者提供了利用漏洞的机会。

在基础设施即代码（IaC）方面，在创建了用于包装和部署你组织中的应用程序所需的 Dockerfiles/YAML 后，你需要确保部署软件的基础设施被正确配置。接下来就是**持续配置自动化**（**CCA**）工具的作用。CCA 利用 IaC 的原则，并参考 IaC 定义文件，以自动化我们之前提到的 IT 配置管理方面。

你可能会问：“好吧，如果你只是想告诉我们那是旧的方法，且现在有了更好、更新的方法，那你为什么还要提到配置管理工具呢？！”

最棒的是，你通常还是在使用之前相同的工具组！一些流行的 CCA 工具包括以下几个：

+   **Ansible**/**Ansible Tower**

+   **Chef**

+   **Puppet**

+   **SaltStack**

与之前的列表相比，我们可以看到传统的配置管理工具与 CCA 工具之间存在重叠，例如 Ansible、Chef 和 Puppet 等。这些工具提供了传统的“前端”配置仪表盘，可以通过浏览器访问，并提供我们期望并要求的图形化库存管理和报告功能，这些是我们从传统配置管理工具中所期待的。

这些*DevOps 导向*的理念、工具和解决方案为开发人员和系统管理员提供了一个机会，可以简单地在他们的代码中“声明”要部署的基础设施，自动化工具接收该声明，然后参考预定义的“批准”蓝图，这些蓝图可以配置以确保符合安全性和合规性要求，（通常称为**政策即代码**）。

因此，就像我们能够为人类阅读创建政策一样，我们也能够将这些政策定义为*机器可读格式*，确保每次都以自动化、无错误的方式部署适当的配置。我们现在拥有一个可审计的、可测量的、预定义的“批准”基础设施和部署场景，并且这些场景会不断监控是否有未经授权的更改，任何绕过或不合规的行为都会被拆除，同时用符合规范的版本替换掉。考虑到你的风险，这是绝对完美的。此外，我们在过程中解决了许多*完整性和可用性*的问题，前提是工具可靠，解决方案为你的组织精心设计。

从*保密性*的角度来看，我们能够通过利用**密钥管理**自动化工具（如**HashiCorp Vault**）来自动创建和声明超级强大的密钥、令牌、密码和密钥，这些内容永远不会由个人处理。

通过*密钥管理*，你可以以编程方式动态地创建、撤销和轮换组织的密钥，响应根据政策定义或检测到的活动所设定的变化或需求。这样，你可以实现对静态或传输数据的高效加密，且对密钥没有任何知识，并能记录所有交互的审计日志。此外，密钥管理过程的自动化可以为授权提供高效的*即时*解决方案。

当然，IaC CCA 方法也存在一些缺点。像**Docker Hub**这样的社区仓库，包含了数十万已经被“弃置”或“腐烂”的容器配置文件。这些文件包含过时的定义、不良的安全实践，或者有意写入的后门和恶意软件，等待那些匆忙（或无法正确阅读和理解文件）的人将漏洞部署到他们的系统中。

记住，这并不是一个极端案例。Palo Alto Networks 的威胁情报团队曾发现，2019 年 65%的公开披露的云安全事件是由于组织员工的错误配置所致。当他们调查为何这个数字如此之高时，他们发现那些采用 DevOps 方法的公司内部有一种文化，强调创建新功能的速度，而非治理和安全。再加上对速度的推动，数十万个高风险模板在受信任供应商（如 Docker Hub）开放源代码、可搜索的仓库库中免费提供。有关此主题的进一步阅读可以在这里找到：[`www.paloaltonetworks.com/company/press/2020/palo-alto-networks-report-finds-poor-security-hygiene-leads-to-escalating-cloud-vulnerabilities`](https://www.paloaltonetworks.com/company/press/2020/palo-alto-networks-report-finds-poor-security-hygiene-leads-to-escalating-cloud-vulnerabilities)。

考虑到这一点，我们可以达成共识：即使在事物的核心是高度自动化和加速的情况下，IaC 也无法消除实施和遵循变更控制和审批流程的必要性。我们必须记住，省略这些治理步骤会增加实施变更时引入未知风险的可能性。

一些适用于 IaC 部署管道的过程和程序的合适理念可能包括以下内容：

+   确保你为用户实施了*最小权限*原则。你不希望给他们“城堡的钥匙”或让他们有机会关闭流水线中的某些功能，从而绕过某些保护和检查。此外，应该没有任何方法让用户能够访问他们已部署代码的生产服务器。

+   在开发和部署过程的多个阶段，可以对定义基础设施的机器可读文本文件进行安全检查和扫描：

    – DevOps 工程师或开发人员可以在他们编写代码的 IDE 中扫描文本文件，检查是否存在已知的错误配置和镜像。

    – Git 仓库，如 GitHub、GitLab 或 Bitbucket，可以与安全扫描器集成，以检查文件中是否存在已知的配置错误或恶意项。像**Snyk.io**这样的解决方案可以参与 CI/CD 流程，确保正在使用的 IaC 定义是安全的。

    – 像 Snyk 这样的工具能够扫描 IaC 配置文件，报告容器是否以特权模式/特权用户身份运行，或者是否未设置内存和 CPU 限制等漏洞。

    – 这些扫描还可以检查基础设施是否运行在最新且安全的操作系统和应用版本上。

+   IaC 工具本身应该得到维护，我们需要确保我们正在运行最新、最安全的版本。

总结来说，使用 IaC，我们能够实施自动化方法，以减少配置错误和过时基础设施的风险，包括通过变更控制阶段发生的管道安全扫描。

通过自动化和适当的测试，你可以通过去除部署、更新和变更过程中的人为因素来减少错误的风险。一份好的脚本在每次执行时都能有效运行，并且需要员工的参与时间和精力更少。

这些自动化解决方案应该防止在检测到不可接受的风险水平时部署基础设施，你的工作是确定适合你组织的风险水平，并将其传达给相关人员。

此外，通过适当的监控和变更检测，我们可以确保系统在停机或类似事件后可预测地恢复。例如，如果只有一台服务器出现故障，我们可以创建规则自动部署该服务器的镜像来替代它，而不是等待员工注意到故障、诊断故障原因并修复问题。

关于停机的问题，我认为现在是时候转向讨论专注于可用性、灾难恢复和业务连续性了。

# 专注于可用性、灾难恢复和业务连续性

我们在谈论信息安全时需要诚实；它并不总是为了防御那些试图窃取我们组织珍贵知识产权的恶意黑客。实际上，在你的职业生涯中，你会面临的许多场合都涉及由于停电或软件更新失败等原因导致生产系统宕机的情况。

仅仅因为这些威胁不是敌对性质的，并不意味着它们不真实。事实上，情况可能恰恰相反：我们可能会比面对恶意攻击者更频繁地遭遇非敌对事件导致的停机。因此，我们需要确保拥有有效的变更控制政策，并严格遵循这些政策，我们还需要定义和演练灾难恢复和业务连续性流程，以确保最大限度地减少停机时间。

## 定义、实施和测试灾难恢复流程

灾难恢复是建立适当文档、规划和实践的过程，确保我们能够从自然灾害或人为灾难中恢复，并恢复关键的业务功能。它与业务连续性不同，业务连续性专注于确保所有关键的业务功能在任何破坏性事件或灾难发生时仍然保持在线并正常运作，而灾难恢复则是关于恢复。

例如，正如我在前面的章节中所讨论的，您的组织可能面临自然灾害，如洪水、地震和龙卷风。在我写这本书时，全球范围内正在发生大流行和战争活动。您可能会面临危险废物事件、爆炸，甚至是导致您的业务下线或人员不得不离开常规工作空间的网络攻击。

对于所有这些灾难，我们面临着潜在的损失。2015 年，IT **灾难恢复准备**（**DRP**）委员会报告称，小型企业在每小时停机的情况下可能面临最高 8,000 美元的损失。同一报告中，中型企业每小时可能面临最高 74,000 美元的损失，而大型企业在灾难发生时每小时的损失可能高达 70 万美元。更多阅读内容可以在这里找到：[`www.researchgate.net/publication/343063858_PLANNING_FOR_DISASTER_RECOVERY_CAN_LEAD_TO_AVOIDING_DISASTER`](https://www.researchgate.net/publication/343063858_PLANNING_FOR_DISASTER_RECOVERY_CAN_LEAD_TO_AVOIDING_DISASTER)。

为了准备适当的灾难恢复计划，我们需要一些文档，这些文档看起来非常熟悉，因为我们在本书中反复提到了相同的内容：

+   清晰、直白的操作手册，任何人都可以在没有干扰的情况下跟随。这意味着清晰的标签和确保可用性（即使在停机或外部场景下）。

+   政策文件，清楚地说明您组织的角色和职责，以及从业务角度的需求，这些可能包括来自监管机构的合规要求或服务级别协议（SLA）。

一旦这些文档创建完成，优先级*第一*的任务是审查这些计划——不仅要进行桌面演练，还要进行实际的场景演练，进行实际的疏散以及基础设施和系统恢复操作，以发现从理论到现实的任何逻辑或技术上的漏洞。如果发现任何漏洞，必须进行补救计划并实施，然后重新创建测试场景，以验证更改的有效性。

当然，这一切都围绕风险展开。你专注于最关键的资产和系统，并根据哪些对业务运营至关重要来优先恢复活动。

与灾难恢复密切相关，以至于我不知道应该先谈哪个，我想简要谈谈业务连续性，尽管我在前面的章节中已经提到过它。

## 管理业务连续性设计、规划和测试

与灾难恢复紧密相关的功能是业务连续性。业务连续性专注于确保所有关键的业务功能在受到干扰事件或灾难的情况下仍能保持在线并正常运行。从某种意义上说，灾难恢复可以看作是业务连续性的一个子部分。通过建立所有必要的文档、规划、培训和测试，我们能够确保在面对困境或发生干扰事件时，我们的组织具备韧性。

对于灾难恢复和业务连续性来说，值得考虑的是关于热备站、温备站和冷备站的相关理念。

**热备站**指的是作为公司生产系统的可用且完全冗余的镜像的活跃基础设施，与原始基础设施解耦，以减少两者同时被摧毁的可能性。如果你有一个热备站准备好，那么只需要将操作转移过去。这是最昂贵的选项，但也是在发生干扰时最能够迅速投入使用的选项。

**温备站**是与生产系统同步的版本，能够随时部署，尽管在提供过程中会有一些延迟。温备站的优点在于其准备成本远低于热备站。

**冷备站**可用于非关键的业务操作，或当组织面临的风险水平不足以要求热备站或温备站，或没有预算来维持这两者时。冷备站需要从头开始进行配置，但仍然能够在故障或灾难发生后提供迅速恢复的机会。

## 实施和管理物理安全

一如既往，我想简要提到，作为信息安全专业人员，您应该将物理安全纳入自己的责任范围。从本书开始以来，我们已经讨论了组织在物理领域面临的风险，从因恶劣天气或电力中断导致的可用性损失，到恶意攻击者突破外围防线并获得机密信息。

对于各种物理安全事件，必须定义、研讨和实践相关的计划和程序，以确保您的团队能够做出适当的反应。文档必须存放在任何可能承担责任的人可以轻松访问的位置，且指令必须简明清晰，因为高度紧张的情况下可能导致误解和混淆。

由于我们在本书中已讨论过物理安全的各个方面，我将简要总结本节内容并进入本节的总结部分。

在本节中，我们讨论了通过定义、实施和测试灾难恢复流程，以及管理业务连续性设计、规划和测试，来提高系统可用性的方法。现在我们已经讨论了可用性问题，我将继续讲解如何管理升级、打补丁和应用安全控制。

# 管理升级、打补丁和应用安全控制

您的系统需要不断更新和打补丁。在前面的一节中，我们讨论了 IaC 如何帮助我们自动化这些过程，这非常有益，但并不总是可行的。

有时，我们需要采取实践操作的方式来配置、审计、更新和撤销系统，例如，当我们过渡到更新的技术或在第三方进行渗透测试时得到了相关发现。

此外，在*第六章*《设计和管理安全测试流程》中，我们讨论了*网页应用程序漏洞扫描器*、*网络漏洞扫描器*、*SAST/DAST*、*依赖性扫描*以及类似的自动化扫描，这些可以提供需要采取的行动和必须执行的升级内容。

问题是，如何确保 IT 团队理解组织面临的风险，并执行需要实施的变更列表，以确保更加安全的环境？

## 教育

作为组织的信息安全专家，我们有责任确保相关人员了解并掌握他们可以采取行动应对的风险。这可能包括安排安全培训，但也可能意味着定期安排与 IT 团队的会议，可以是每周、每两周或每月一次，会议中你将展示特定风险或陷阱的信息，或者讨论组织面临的整体风险态势。花时间解释并帮助他们理解这些问题为何重要。这是你知识体系中的一个关键部分，否则你只会成为办公室里那个让人浪费时间、没有实质性贡献且不让同事们在公司笔记本电脑上插入 USB 驱动器的脾气暴躁的人。

此外，这些会议有助于你更好地理解资产管理。你可以参与对话，从中获得关于为什么某个变更可能在另一个变更之前实施的有用信息。你可以从管理日常运营的团队那里获得丰富的信息，而这种对话在持续改进的过程中极具价值。这不仅是积极主动管理你数字资产健康的有效方法，也是大多数标准和义务要求的内容，你的组织将受到这些要求的约束。

这种知识共享和开放性可能是决定变更是否成功的关键，或者它可能导致失败，从而引发安全漏洞或停机。基于此，让我们来看看实施变更的最佳实践。

## 变更控制

正如我们之前提到的，遵循已定义的治理结构和**变更控制**流程至关重要，这有助于减少停机时间，并提升你组织的员工诊断故障或错误的能力。

我们可以在这个话题上深入讨论成千上万的页面，但我认为更相关的是聚焦于 IT 领域的安全特定内容，并让你进一步研究作为更广泛 IT 或组织控制的变更控制流程。当我们从信息安全的角度看待*变更控制*时，我们的目标是避免错误配置，最大化正常运行时间和可用性，并记录所有变更及相关信息。

在进行补丁、升级或应用安全控制时，变更控制流程中有价值的步骤包括以下内容：

+   在文档中识别并描述所需的变更

+   从商业角度证明变更的必要性以及为何需要进行变更

+   评估变更可能对组织造成的影响，并记录减轻负面影响的方式

+   描述在失败时的回退计划

+   记录任何需要批准的内容并保存相关批准记录

+   与员工、合作伙伴、客户或类似方进行沟通的规划

+   有效沟通计划中的变更，包括时间窗口和任何预期的停机时间

+   变更的实施和评估

一个出色的变更控制过程不需要慢或限制性强。关键在于确保我们有一个计划，以减少停机、配置错误或类似的信息安全事故的可能性。通过确保我们有适当的文档和规划，我们也在确保拥有所有必要的资源。

大型项目将从定义明确的变更控制过程中受益，例如安全改进计划，我将在此简要介绍。

## 安全改进计划

除了在差距分析或第三方/内部渗透测试后的持续改进努力外，可能会揭示出你们的信息安全计划中某些方面缺乏在风险管理方面所需的成熟度或有效性。**安全改进计划**是一个定义明确的信息安全改进项目，在一段时间内进行排定、实施并测试其有效性，朝着成为一个更加安全、运营更加有韧性的组织迈进。

安全改进计划可以涵盖本书中所讨论的所有主题以及更多内容，它是一个全组织范围的努力，旨在实施和加强控制措施并降低风险。

安全改进计划的理念在于，我们不仅仅是把一些基于安全的任务“撒入”我们每天、每周和每月关注的任务中。这是一个主动的决定，*降低新特性的优先级*，而是专注于提高保护水平和风险缓解。当然，像这样的决定需要高层管理的支持，这将需要一个明确的计划，其中包括时间、成本、风险和回报的估算。

在规划和估算这一点时请花些时间，因为这往往是一个领导层难以做出的决定。然而，一旦你获得了支持，你将能够向团队呈现计划，这将帮助你在每个步骤中推进安全改进计划，且让团队知道这一指令是“来自高层”是一种非常有效的方法，可以优先处理这些任务并获得一线员工的支持。

既然我们简要讨论了资源配置、专注于可用性和业务连续性、以及管理升级、补丁和应用安全控制的内容，我认为我们应该进入下一部分，讨论如何调查信息安全事件并响应信息安全事故。

# 调查事件与响应事故

我相信大家都会同意，当我说“没有准备就是在准备失败”时，尤其是在事件响应和调查方面。如果没有足够的响应计划、操作手册和文档，当我们面临数据泄露、停机或其他信息安全事件时，我们注定会无所适从，缺乏有效的方向。

我们可以有出色的软件解决方案来帮助识别我们环境中的恶意和高风险活动，但如果没有足够的应对计划来决定响应什么以及如何响应，那这一切都是徒劳的。

我们应该通过定义什么构成响应的启动来开始制定我们的事件响应计划。哪些类型的信息安全事件会导致贵组织的成员进行调查或响应？

并非所有信息安全事故都是信息安全漏洞，但所有信息安全漏洞都是信息安全事故和信息安全事件。让我引用一些来自 ISO 27001 的定义：

+   **信息安全事件**是指在一个环境或系统内，任何表明安全政策被违反、控制措施失效或出现未预测到的可能影响安全的情况。

+   **信息安全事故**是指一项或多项**信息安全事件**，其中信息安全或业务操作受到损害。

+   **信息安全不合规**是指未能履行政策、标准或法规中的要求。

所以，**信息安全事件**即使是短暂的，也有可能影响风险。**信息安全事件**是指我们已知对运营或安全产生负面影响的情况，如停机或确认的安全漏洞，**信息安全不合规**则是发现控制措施未正确实施或政策在实践中被忽视。

让我举个例子，说明信息安全事件是如何引发信息安全事故的：

+   **事件**：贵组织的一名用户联系说他们无法打开任何文件，且屏幕上显示有警告信息。

+   **事故**：经过调查后，你的团队发现该用户的笔记本电脑感染了勒索病毒。因此，启动了勒索病毒的事件响应手册，并启用了相关团队进行响应。

+   **不合规**：经过调查和修复后，事件响应团队发现员工打开了来自未知方的电子邮件附件，并且由于 IT 团队的疏忽，某些计算机上未禁用过时的 SMB 服务。

+   **行动**：已优先为员工提供钓鱼攻击和信息安全培训，IT 部门已将实施工作站安全配置（包括禁用过时的 SMB 版本）列入路线图项目。

如你所见，如果我们使用这些事件和事故的定义，并考虑到我们的风险，我们就能够为调查特定类型的事件和响应事故制定统一且有效的程序。做到这一点就是定义你的事件响应计划，接下来我将进一步探讨。

## 定义你的事件响应计划

为了理解工作流程和需求，制定适合你组织的事件响应计划是至关重要的。例如，如果你没有为你的组织的**安全信息与事件管理**（**SIEM**）解决方案生成的警报制定可行的响应，那么你实际上就是在浪费这项工具的投资，无法从中获得价值。

我想借此机会讨论一些在开始安全监控活动之前需要回答的关键问题。

我们希望回答的一些问题可能包括以下内容：

+   *与信息安全事件相关的角色有哪些？*

    一些角色示例可能包括首席执行官（CEO）、首席信息安全官（CISO）、首席技术官（CTO）、董事总经理（MD）、系统管理员（SysAdmin）、人力资源经理等。

+   *每个角色在每种类型的事件中的职责是什么？*

    一些成员可能需要与客户沟通，其他成员可能需要与执法机构、客户或业务利益相关者沟通。可能会有负责调查事件的角色；也可能会有负责恢复流程的角色。将角色与特定的技能相匹配是一个有益的解决方案，将这些角色与特定的职位名称和职位描述挂钩，则能够使个人在进入新角色时意识到自己的职责。

+   *如何对安全事件进行优先级排序？*

    优先级应该基于风险，但你需要以一种便于任何可能成为“首位响应者”的人遵循的方式正式定义这些优先级。教育员工如何应对安全事件，以及文档可能存放的位置，是事件响应的一部分，我们在其他章节中曾提到过。

+   *记录安全事件的方法是什么？*

    我们如何从发现到关闭记录安全事件，这是事件响应的另一个方面，我们需要有效地定义并培训员工。

+   *如何通知事件响应团队的适当成员有关事件的信息？*

    一些示例可能包括电子邮件、电话、短信或 WhatsApp。

当我们定义一个流程时，我们需要考虑以下步骤的指导：

+   调查一个事件，包括需要观察和记录哪些信息

+   确认事件，包括沟通和后续适当响应的步骤

+   响应事件，包括隔离或遏制威胁并减少对组织的损害

+   恢复操作，确保事件的影响降到最低。

+   调查和报告，可能使用取证能力，并采取措施保护免受罪犯侵害或采取法律行动（如适用）

如果我们想要一套简明的指南来应对信息安全事件，我们可能会看到由各政府机构提供的以下几条指南：

+   英国**国家网络安全中心**（**NCSC**）的*中小型企业指南：响应与恢复*（[`www.ncsc.gov.uk/collection/small-business-guidance--response-and-recovery`](https://www.ncsc.gov.uk/collection/small-business-guidance--response-and-recovery)）

+   欧洲网络与信息安全局的*事件管理良好实践指南*（[`www.enisa.europa.eu/publications/good-practice-guide-for-incident-management`](https://www.enisa.europa.eu/publications/good-practice-guide-for-incident-management)）

+   美国国家标准与技术研究院的*800-61 Rev. 2*（[`csrc.nist.gov/publications/detail/sp/800-61/rev-2/final`](https://csrc.nist.gov/publications/detail/sp/800-61/rev-2/final)）

您还可以寻求提供事件响应服务的信息安全咨询公司帮助。通常情况下，您需要提前支付费用，以便这些组织在发生事件时能够随时响应，并且每次事件所消耗的时间将从您的“余额”中扣除。

此外，值得注意的是，根据您所在国家/地区的不同，政府的各个部门提供的支持是不同的。

其他组织可能更倾向于自己进行调查和应对，而无需外部帮助。接下来让我们看看关于执行安全调查的几个要点。

## 执行安全调查

我将在本节中讨论如何管理和进行事件的安全调查，以及如何报告事件。通过使用一致的、结构化的方法，我们可以确保在大多数情况下采取系统且有效的方式。

首先，让我们提醒自己，并非所有安全事件都足够重大，值得进行调查。记录单个事件或多次事件的组合是很重要的，但我们不一定需要将每个记录的事件上报并让更广泛的组织介入或联系执法部门。有关应该报告哪些内容的指导可以在当地法规或来自警方、国防部、网络安全部门（如英国的 NCSC）以及其他类似机构提供的资源中找到。

作为一名信息安全专业人员，您的责任包括以下内容：

+   确定什么构成**轻微事件**和**重大事件**。

+   确定对轻微事件和重大事件的响应。

+   确保遵守所有国家或地区的法律法规，包括确保事件报告给相关执法部门。

一些*重大事件*的例子可能包括以下内容：

+   诸如入室盗窃或损坏组织财产等犯罪行为

+   洪水、风暴以及其他天气灾害导致的安全或运营受损

+   未经授权访问被分类为机密或受保护的信息

通常，一个重大事件需要联系保险提供商、执法机构、政府机构、客户和其他团体。为这些情况定义并保持一套程序并确保其易于访问是非常重要的，通常这些内容会被记录在你的应急响应和灾难响应的操作手册和政策中。

随着流程的推进，定义与安全调查相关的角色也非常重要。以下是一些角色及其职责的示例：

+   **CEO** 和 **C-suite** 高层管理人员，最终负责响应安全事件。通常这包括确保为员工和承包商提供足够的流程来报告和响应此类事件，并确保有关于过去表现和要求的记录。这通常通过任命适当的员工来专注于这些工作。

+   **CISO**，由 **C-suite** 任命负责处理前述工作的人员，负责以下事项：

    – 处理与信息安全事件相关的流程

    – 管理与安全事件相关的信息，包括来自内部调查和执法机构调查的结果

    – 向 **C-suite** 和高级管理团队报告该信息

+   **高级管理** 团队成员将在事件响应过程中发挥作用，并会利用其团队在发生安全事件时执行相关职责。这可能包括法务负责人准备与诉讼相关的信息、人力资源负责人回应内部风险、传播负责人准备公众声明等。他们通常也会负责与其部门相关的报告领域，并定期向 **CISO** 汇报这些信息。

+   **经理** 更接近业务活动的运营层面，确保安全事件得到适当报告，并确保员工在发生需要响应的安全事件时，做好应对其职责的准备。

+   **员工** 是最有可能注意到信息安全事件或事故的群体。他们应该理解自己的职责以及在发现安全事件时可用的流程。这可以通过教育和培训来实现。

我建议你阅读国际非营利组织 CREST 发布的一份文档。这是一个关于事件响应流程的指导，名为 *网络安全事件响应指南* ([`www.crest-approved.org/wp-content/uploads/2014/11/CSIR-Procurement-Guide.pdf`](https://www.crest-approved.org/wp-content/uploads/2014/11/CSIR-Procurement-Guide.pdf))。

在链接的 PDF 指南中，你将找到以下内容的指导：

+   理解信息安全事件，包括以下内容：

    – 如何定义一个事件

    – 各种事件之间的对比

    – 我们从攻击中预期的各个阶段

+   为信息安全事件做准备，包括在应急响应过程中可能遇到的各种挑战、应对方式、如何利用专家进行响应以及如何建立内部响应能力。此外，文档讨论了为你的组织做好准备的五个步骤：

    – 对你的组织进行关键性评估

    – 进行威胁分析

    – 考虑对组织的影响，包括所需的人力、流程和技术

    – 创建一个安全的环境，包括实施基本的控制措施，以防止最常见的事件发生

    – 审查你的防护姿态并测试应急响应准备情况

+   对信息安全事件的响应，包括以下内容：

    – 识别事件

    – 确定目标

    – 采取行动来遏制事件

    – 恢复系统

+   下面是信息安全事件相关内容，包括以下方面：

    – 进一步调查事件

    – 向利益相关者报告事件

    – 进行事件后的调查复盘

    – 传达发现并基于发现进一步扩展

    – 根据调查结果更新信息和控制措施

    – 执行分析以发现趋势

+   最后，选择供应商来帮助处理信息安全事件。

这份文档将在未来成为你和你组织的宝贵资源，我希望你能采纳我的建议并阅读它。

现在我们已经讨论了事件调查和应对事件，我想深入讲解如何在你的组织中实施和利用侦测控制。

# 实施和利用侦测控制

如 IT 的性质所示，我们面临着不断变化的技术、威胁和应对技巧，包括勒索软件、分布式拒绝服务（DDoS）攻击和渗透攻击。我们需要了解我们网络中的情况，并实施自动化的控制措施，在攻击发生时进行通知，并积极防止这些威胁被利用。

为了实现这种可见性，我们需要一套围绕**安全监控**和**安全调查**的流程和结构，并且我们需要与负责保护我们网络的员工和第三方一起测试这些流程。

最终，高级管理层负责向内部**安全运营中心**（**SOC**）或第三方提供的**SOC 即服务**分配适当资源，并准备好**事件响应团队**。一旦高级管理层认识到信息安全的这些方面的重要性，实施和维护这些控制的责任可能会被委托给您，您的组织的信息安全专业人员。

在承担这一责任的同时，我们需要确保采取基于风险的策略，包括以下内容：

+   资产优先级排序

+   威胁建模

+   一个检测预算

+   一个响应预算

除此之外，我们需要为未来制定策略，并确定应采取哪些教育和改进措施，以确保组织即使在不断变化的情况下也能保持受保护状态。

就目前而言，信息安全专业人员在实现这些更高水平的可见性方面最有效的措施之一是通过安全监控。让我们讨论接下来可能涉及的内容。

# 使用安全监控来提高可见性

增加对数字资产运行情况的可见性的一种特别受欢迎的控制是实施日志记录并将这些日志聚合到 SIEM 系统中。

SIEM 不仅为专家提供了调查组织内资产日志的能力，而且最近还能利用 IPS/IDS 功能以及机器学习算法来丰富日志数据并积极防范威胁。这将 SIEM 从仅仅是*侦查控制*转变为既是*预防性又是侦查性控制*，为网络以前黑暗的角落提供上下文和可见性，以及减轻威胁行为者的有效性。

这可能包括识别以下模式和行为：

+   通过认证日志进行**账户被篡改检测**。

+   通过系统活动、防火墙、IDS/IPS 和**CASB**（***云应用安全代理***）日志进行**恶意软件检测**。

+   通过上下文参考，如比较 IDS/IPS 和漏洞数据库，进行**入侵检测**。

+   通过防火墙和 CASB 的出站连接日志进行**恶意软件主机检测**。

+   通过管理活动、用户活动和变更日志进行**策略违规检测**。

+   通过 Web 应用防火墙日志、Web 或云服务器日志，或应用程序和数据库服务器日志，检测对外部应用程序的攻击。

为了了解这些检测是否有效且可信的威胁，准备一些信息以使您的*事件响应团队*和*SOC*进行比较和参考将是重要的。

这些信息可能包括以下内容：

+   预期在您环境中出现的*主机列表*。这有助于团队成员或自动化系统检测您环境中不需要的主机或端点。

+   在特定时间段内的网络活动的*基线日志*，可能被视为“正常”。收集这些信息的问题在于回答“如果我们已经遭受入侵怎么办？”的问题。假设“已遭受入侵”的原则在零信任网络理念中变得流行，但许多组织并没有准备好像我们希望的那样迅速采取这些步骤。

+   每台主机上运行服务的*列表*作为基线。它可以建立在先前提到的主机列表上，并应包括预期在特定主机上进行通信的端口号和协议。

+   与 OSI 参考模型对齐的网络功能的*交互式图表或可视化表示*。如前所述，在这个过程中提供有污染的数据的风险，实际上证明了您网络中存在的威胁是“正常”的，因为它们被认为是“正常”的。

为了避免提供掩盖已存在于您资产中的威胁的垃圾信息的陷阱，您应该考虑一个项目，解决以下问题：

+   确定*所有服务器上存在的所有过程和服务*，并指定它们的功能

+   确定*这些过程和服务产生和/或接收的通信类型*

+   确定*这些服务的关键性*，以及它们的脆弱性和相关风险水平

+   确定是否有*冗余服务*（即，它们是不必要的）

+   确定是否有*关键服务缺乏冗余*（即，它们是关键的，但没有任何备用措施）

“啊，我们又来了！”，你现在可能在想。“又让我们做不可能的事情！”

对于一些人来说，尝试准确表示资产中的所有网络活动似乎是不可能的... 这就是为什么自动化系统开始提供解决方案，而不是要求团队放下日常任务，投入时间和精力去处理像之前看到的那样困难的任务。

相反，这些自动化系统能够“扫描”和“检测”在您资产中发现的活动类型，并丰富该数据与全球其他资产中发生的恶意活动周围的情报，然后利用该信息通知您的 SOC 并应对任何活动威胁。

这些解决方案可能是您组织的更可行的解决方案，并可以帮助您导航您的资产的复杂性，过滤掉所有噪音，突出只有最有价值的见解和基于风险的检测。这些见解甚至可以转化为基于关键点摘要的报告或“管理风格”的报告。

这些软件的一些示例可以包括以下内容：

+   Microsoft Azure Sentinel

+   Splunk Enterprise Security

+   IBM QRadar Security

+   LogRhythm NextGen SIEM 平台

+   AT&T 网络安全 AlienVault USM

+   Graylog

无论你为组织选择哪种 SIEM 和情报解决方案，都有一些最佳实践值得注意，并可以在将解决方案引入组织并创建最佳流程的早期阶段应用。

# 安全监控最佳实践

*安全监控和 SIEM* *工具* 在检测和预防试图利用你组织资源的重大威胁方面非常有用，帮助确保你的组织遵守相关法规和要求，同时提供可衡量的洞察，指出安全态势可以改进的地方。

对于这类系统，我们希望从技术、法律或监管的角度收集尽可能多的信息，以确保最高水平的可见性和数据聚合，并从我们组织的活动中获取有意义的洞察。这可能包括*网络设备和服务器日志*、*Active Directory/IAM 日志*、*漏洞扫描仪和配置管理工具指标*等等。

此外，在聚合数据时，实施冗余非常重要，并且要像对待任何关键数据一样处理这些数据，其中的风险通过备份和恢复策略得到缓解，以确保符合你的信息安全政策。

在*SIEM 和安全监控*中也存在一些局限性。有时候，收集某些信息是不可行的，或者网络和计算吞吐量无法处理你组织中的数据量。做出决定之前，了解你期望系统处理的数据量非常重要，这对于选择合适的解决方案和供应商至关重要。

我想介绍一些在深入进行安全监控之前需要采取的特别重要的步骤，这些步骤可以帮助你和你的组织避免常见的错误和失误。

## 建立需求并定义工作流

让我问你一个问题：如果你不知道从 SIEM 中需要什么，怎么能评估可用解决方案的功能呢？

首先，像做任何决定一样，在选择解决方案之前，以下几个步骤非常重要：

+   确定你的需求。

+   确定你的时间线目标。

+   定义理想的工作流，并根据你和你组织的需求进行规划。

有时候，供应商会尝试突出一些对你没有价值的功能，这些功能的存在只是为了让那些没有准备好的人眼花缭乱。另一方面，有时候，供应商会为你提供一个更好的解决方案，它能够解决更多你未曾预料到的问题，或者以巧妙的方式解决你的问题，这是一个很好的情况。

在我们制定需求时，不妨再次考虑*KISS 原理*（保持简单）。定义一个合理的范围来试点你的解决方案。在实施 SIEM 的第一天，你不需要一次性覆盖所有需求，系统可以逐步推出，允许进行故障排除和已定义流程的测试。通过这样做，你不仅提供了概念验证，减少了边缘案例的可能性，还能向关键决策者展示 SIEM 系统的好处。

鉴于此，确保始终牢记你的最终目标，确保解决方案能够扩展到你希望覆盖的数据量级。这可能以**每秒事件数**（**EPS**）来衡量，或者可能是**每日千兆字节**（**GB/day**）。

在考虑需求、目标和工作流程时，你还需要考虑合规性和法规要求。*SIEM*能够帮助向监管机构和审计员展示其他安全控制的有效性。在之前的章节中，我们讨论了制定法规和标准清单，以及你的组织必须遵守的每项法规和标准的具体要求，所以你应该已经准备好这些了，对吧？没错吧？！

有了这份清单，你已经准备好在演示和展示过程中向供应商提及你的合规性要求，确保你能收集、保留和删除为了保持合规所需的信息。它还可以帮助估算为存储保留所需的存储量，帮助简化定价讨论。

## 定义具体规则并确保其有效性

在确定你的需求和定义*SIEM*与*事件响应*流程之后，你可以定义对组织有用的数据类型及其可能的指示意义。许多解决方案有各种“内建”的指标，例如以下内容：

+   授权失败的尝试

+   授权成功

+   用户权限变更

+   应用服务器错误

+   应用服务器性能问题

+   管理员活动

此外，定义你不想存储或执行 SIEM 活动的信息，或者可能希望限制某些活动类型也是非常重要的，例如以下内容：

+   个人身份信息（PII）

+   违法收集的信息

+   信用卡和银行信息

+   密码

+   加密密钥

从这些定义以及从这些定义中制定的规则来看，定期测试解决方案的有效性非常重要，以确保预期的结果确实发生。这包括*精确数据匹配*或*近似匹配*，或需要通过的*阈值*（例如，某事件需要在 1 分钟内发生超过三次，才会触发警报），等等。这还包括解决方案生成的通信和通知，以及是否如预期一样通知了相关人员。

我相当确定，在为*事件响应和安全监控*制定需求和计划的过程中，你会发现一些你曾认为可行的理论并不奏效。这是你开始采取下一个最佳实践的机会，那就是…你猜对了，持续改进你的政策和配置。

## 持续改进你的 SIEM 配置和事件响应策略

信息技术领域正在以前所未有的速度变化，且这一速度正在不断加快。这意味着解决方案会变得过时，曾经被认为是高质量的解决方案或资产的信息要么变得难以使用，要么变得毫无用处，同时，新的威胁会出现，利用或规避曾经被视为“防弹”的配置。

因此，我们需要在日历中设定一个定期的日期，专注于完善 SIEM 配置和事件响应策略（当然也包括其他方面，但我们现在只讨论 SIEM 和事件响应）。我们不能让它停滞不前，即使我们正在使用一个*软件即服务（SaaS）*解决方案，且该解决方案会自动从供应商处更新，我们仍然需要确保系统中反映的是当前我们环境的实际状况。

现在我们已经结束了关于安全监控的这一部分内容，我想以本章的总结来作结。

# 总结

那么，现在就结束了*第七章*，*安全运营管理*。我相信我们已经涵盖了信息安全专业人员处理安全运营所需的高层次要求。正如本书的每一章节一样，我们涵盖了许多话题，但每个话题都只是非常简略地提及。任何本章的内容，甚至是其中某一段，都是可以专门写成整本书的。我希望这能激发大家未来深入了解每个领域的兴趣！

在本章中，我们涵盖了信息安全运营团队日常需求的各个重要方面。

首先，我们探讨了资产配置和维护的有效策略，包括所需的政策和配置管理步骤，并且简单介绍了基础设施即代码（IaC）这一概念，以简化和自动化这些过程。

接着，我们关注了可用性、灾难恢复和业务连续性活动，包括定义、实施和测试灾难恢复与业务连续性计划的流程。

从这里，我们进一步探讨了在组织中管理升级、打补丁和应用安全控制的相关话题，其中包括关于教育要求、变更控制流程以及安全改进项目的信息。

然后，我们深入探讨了事件调查和应急响应，包括定义事件响应计划和进行安全调查。

然后，为了结束本章，我们探讨了实施和利用侦探控制措施，包括如何利用监控来提高对你系统内部的可见性，利用增加的日志记录级别，将这些日志聚合到 SIEM 中，应用自动化逻辑和机器学习洞察分析数据，并让 SOC 成员审核这些数据。

最后，我们讨论了安全监控的最佳实践，包括建立需求并定义工作流程，定义具体的规则并确保其有效性，以及持续改进你的 SIEM 配置。

现在，接下来我们要进入最后一章，*第八章*，*提高软件安全性*，这是我个人最喜欢的话题。
