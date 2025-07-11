# 第六章：设计和管理安全测试过程

现在，你已经很好地理解了可以实施的控制措施，以便你在组织中有一个有效的安全策略，我猜你已经实现了其中的一些控制措施，现在，你可以放心地放松，浏览 LinkedIn，在工作电脑上看 Netflix，直到你退休。恭喜你！你已经赢得了金表。

哦，你刚刚被*pwned*了。哎呀，怎么会这样？好吧，这是因为在你的设计中有一个巨大的漏洞，而你没有让其他人* sanity check*你的架构，也没有让任何内部或外部团队对你的环境进行*渗透测试*。你需要第二双眼睛，通常，你希望那第二双眼睛是一个技术高手——一个与组织没有任何关系的人，不会因为负面的意见而担心得罪同事或上司。

你想要答案。你想要真相！你的安全控制有效吗？有没有绕过控制的方法？你的员工觉得实施这些控制麻烦还是难以使用？

当我谈论信息安全时，它通常会回到采用持续改进的思维方式，这当然包括测试你现有的实施，并改进任何发现的问题，以便运行更顺畅、优化的信息安全程序。哦，当然，不言而喻，你会根据…你知道我要说什么吧？我希望是的：风险。

在本章中，我们将涵盖以下主题：

+   准备安全评估

+   了解不同类型的安全评估

+   执行安全评估的最佳实践

+   解读安全评估结果

到本章结束时，你将能够理解安全控制测试，包括安排外部和内部安全审计、如何分析报告并审查测试结果，以及如何管理每个评估中产生的行动。

让我们开始吧！首先，让我们看看我们需要测试什么，以及我们打算如何进行测试。

# 准备安全评估

我们怎么知道我们的系统可以防御攻击者？我们怎么知道我们的系统是有韧性的？我们怎么知道我们的系统是适当冗余的？

不幸的是，答案不能仅仅是“*因为是我自己设计的*”（戴着墨镜，站在电梯里的 Segway 上）。至少，第二双眼睛是很重要的。为什么我说“至少”？有时，你的第二双眼睛可能是一个同事，他要么没有足够的知识，要么与组织的隔离程度不够，无法提出他们如果没有上司会因为提出意见而冒犯对方的观察。

首先，你需要*获得高层管理的支持*。这是本书中的另一个经典主题，也是信息安全中的经典主题，你将在各种标准中看到这一点。例如，在*ISO 27001*的要求中（[`www.iso.org/standard/54534.html`](https://www.iso.org/standard/54534.html)），*第 5 条*谈到*领导力*，而*第 9.3 条*则涉及*管理评审*。*第 5 条*指出，高层管理层必须参与制定信息安全政策。*第 9.3 条*则要求高层管理层持续参与评估信息安全管理系统，以确保其有效性。

就像我们之前说过的那样，管理层中的某些老古董怎么能做到这一点呢，尤其是他们还没有学会如何在 Excel 中使用公式？其实很简单：他们批准支出，并正式回应调查结果，要么批准所需的修复费用，要么接受风险。当然，作为你组织中的信息安全专业人员，你需要将调查结果转化为管理层能理解的内容，并且要以一种易于理解并突出任何风险的方式进行。

让我们来看一下如何根据组织需求选择合适的评估解决方案。

## 定义你的需求

你有大量的信息、系统、建筑和其他敏感或机密的资产，你已经实施了控制措施来保护它们。为了说它们是安全的（并且确保*CIA 三原则*完整），你需要确保这些控制措施有效地防止未经授权的访问、未经授权的修改，并确保可用性。对吧？对。

这是一件简单的事情，写起来简单，执行起来却不那么简单，尤其是当你的组织做着成千上万种不同的事情时。如果你联系到信息安全咨询公司，你可能会运气不错，遇到一个真正关心你组织的销售人员，然后他会拒绝销售那些不合适或不必要的评估。这对你来说是一个很好的情况，但同时，重要的是在购买之前确保你知道自己需要什么，并且，如何确保你接触到的是那种类型的销售人员呢？

此外，你是否愿意在还没有机会充分内部评估系统之前，就支付咨询公司来评估你的系统？这不仅听起来像是在浪费钱，而且也显得有些不负责任，直接交给别人而没有任何了解。我的意思是，我们是什么？高层管理层吗？！

首先，我们需要参考任何我们需要遵守的标准或法规，并记录是否因此需要进行安全评估。之所以建议这样做，有两个原因：

+   首先，我们可以接受标准和法规是有其存在的理由的，并且它们包含了适用于所有组织（包括我们自己）的最佳实践。

+   其次，如果您没有遵守要求，您可能会在未来的审计中被罚款，或者失去对标准的认证。有时，您的组织有与维持各种标准相关的业务运营和关系，例如**支付卡行业数据安全标准**（**PCD-DSS**），并能够处理卡支付。

有时，例如在 PCI-DSS 的情况下，标准的评估要求会根据您组织的活动不同而有所不同。对于低量处理，您可能只需要填写**自我评估问卷**（**SAQ**），而不是让**合格安全评估员**（**QSA**）评估您的系统。

让我们更仔细地看看 PCI-DSS 的 12 个高层次要求作为例子：

1.  实施并维护有效的防火墙

1.  更改所有默认密码

1.  对持卡人数据进行静态加密

1.  对持卡人数据进行传输中的加密

1.  实施并维护恶意软件防护

1.  更新和修补系统以防止漏洞

1.  对持卡人数据的访问控制

1.  对系统组件的访问控制

1.  对持卡人数据的物理访问控制

1.  监控所有对持卡人数据和网络资源的访问

1.  定期测试系统

1.  为所有员工维护信息安全政策

现在，让我们假设由于您的组织处理的*支付交易*数量较大，因此需要一个 QSA。这些 QSA 将评估您的组织是否符合这 12 个高层次要求（以及总计 220 多个子要求）。如果您无法证明这些要求，您的组织面临罚款的风险，或者可能无法接受某些类型的支付。

当我们考虑为*PCI-DSS 评估*做的准备工作，并确保您的组织在 QSA 到达之前符合标准时，重要的是要安排测试，记录每个要点的发现。我们这样做是为了确保我们的组织能够接受支付并避免被罚款。我们有一份要求清单，其中包括*要求 11*，即*测试所有系统、流程和软件*，以便了解任何可能被恶意行为者利用的漏洞，然后应用适当的控制措施。

组织可能会出于其他原因对其内部系统进行安全评估，即使没有具体的监管要求。可能的原因包括不确定组织的知识产权是否得到了适当保护，或者检查已实施的控制措施是否有效地防范了威胁。也许你认为组织的安全性较差，但没有人听你的。在这种情况下，你可能未能获得高层管理的支持，但通过让专业人士展示如何利用漏洞进行攻击，或许能引起更多关注和/或争取到预算。做出这个决定并不是我所能倡导的，但它可能会有效，也有可能让你陷入困境，因此尽量争取上级的支持。

在我们选择进行哪种评估时，这取决于你的需求和战略。你在做出决策之前可以定义的一些内容包括以下几个方面：

+   为什么要进行评估？

    — **合规性**：有时，组织仅仅需要勾选一个合规性框。对于一些顾问来说，合规性评估可能是他们工作的大部分内容。如果这对你的组织来说是主要驱动力，那么花钱做更高价值的评估可能不太值得。

    — **追求改进**：在这种情况下，组织可能已经符合要求，但希望得到比当前更好的保护。此时，你可能需要更高价值的评估，因此需要一些稍微贵一些的服务，或者选择一家更有名的公司。

    此外，安全评估有助于通过快速发现错误来降低成本，提供一个私密的环境，让团队可以修正任何发现的问题，同时避免因泄露带来的声誉损害。

+   测试的内容是什么？评估的范围是什么？

    — **软件**：你是否想查看你的组织所创建的软件是否能够防止入侵或滥用？你是否想检查你的文件共享软件或操作系统的配置是否得当？针对软件有各种评估方法，比如网络应用渗透测试、安全扫描、内部渗透测试、外部渗透测试等。

    — **硬件**：你的组织是否创建或购买了某些物理设备，如自动取款机、锁系统或加密货币钱包？你将需要一个硬件安全测试人员来评估它是否足够安全，以保护它需要保护的内容。

    — **网络**：前面已经提到过，您可能想要了解，组织内部的低权限用户能够利用自己的凭证做到什么程度。您可能希望查看某人是否能从外部入侵您的网络并提升他们的权限。您是否想在其中加入社交工程的测试？您是否想同时测试您的物理安全性？

    — **员工意识与物理安全**：社交工程评估，例如钓鱼活动，向用户发送伪造的跟踪链接，测试他们识别社交工程攻击的能力。

    — **物理安全**：您是否对“黑队”评估感兴趣，即安全评估人员会实际（并且数字化）渗透到您的场所？员工是否允许陌生人进入限制区域？在这种情况下，某人可以访问多少信息？

+   您会给评估人员多长时间？

    — 有时，一个精心策划的活动可能需要几个月的时间来妥善规划和执行。您试图模拟什么类型的威胁？

+   您需要评估在何时完成？

    — 信息安全行业正在蓬勃发展，但目前人才短缺，这可能导致评估完成的延迟。确保提前规划，并与不同的公司沟通，了解他们的交付周期。

+   您对这个特定评估的预算是多少？

    — 如果您需要一个“红队”评估，其中评估团队需要长期规划并模拟长期的真实威胁，但您只有 5000 美元预算，并且没有监控或“蓝队”，您可能需要重新考虑您期望的目标。

与提供安全评估的第三方交流时，值得询问他们的评估方法，并了解他们是否有适用于您希望进行的具体任务的参考资料。此外，在正式合作之前，可能值得与评估人员交流，并/或查看他们的简历。

另一个重要的要求是您的条款。首先，您不希望评估导致您的*生产系统*停机，并让您的组织因为收入损失而付出代价。这对任何人都不利，您希望与有经验的第三方合作，以防止这种情况发生。此外，您不希望在您有机会修复漏洞之前泄露您的弱点。一种防止未经授权共享的方式是设立各种条款，包括**保密协议**（NDA）。

现在我们已经涵盖了关于在进行安全评估之前，您和您组织成员可能需要问的一些高层次问题，我认为接下来讨论我们可能遇到的安全评估类型是个好主意。

# 了解不同类型的安全评估

有多种安全评估可帮助您了解以下内容：

+   您整个组织的安全态势

+   你的硬件产品的安全控制有效性

+   你的软件产品的安全控制有效性

+   你建筑物的安全性

+   你员工的安全意识

+   你安全团队应对主动威胁的能力

除了这个列表外，执行这些类型评估的方法有很多，包括让你自己的员工进行**内部审查**，或让其他组织进行**第三方审查**。此外，还可以进行自动化测试。

内部审查有助于降低成本，在某些情况下，如果内部团队熟悉其审查的流程，还能节省时间。然而，内部审查缺乏客观性，且可能没有“新鲜眼光”来看待目标。

第三方审查由行业专家进行，这些专家每天都在破解软件、硬件、建筑物和组织的信息系统。他们的发现通常会以标准化报告的形式提供，报告可能还会提供补救措施和战略建议，指导你的组织接下来的行动。此外，第三方能够诚实并公开地向客户说明其缺陷，前提是这不是简单的合规性勾选式评估。

另一方面，*第三方审查*可能会很昂贵、耗时，如果没有经过良好的规划和与组织的合作，它们可能缺乏相关性。

总体而言，安全评估既有积极的一面，也有消极的一面。它们有可能会让组织付出时间、金钱，并减少创造新价值的能力，但它们也提供了揭示安全问题的机会，这些问题如果不处理，可能会通过声誉损害、法规问题或盗窃等带来更大的财务损失。

让我定义一下每项评估可能涉及的内容。

## 自动化评估和扫描

在自动化评估和安全扫描中，你依赖软件根据收集的各种信息，检测*已知的安全漏洞*，并将这些信息与漏洞数据集进行对比。让我简要说明几个可以进行自动扫描的场景。

### Web 应用程序漏洞扫描器

通常，**Web 应用程序漏洞扫描器**可以指向你的组织的 Web 应用程序的 IP 或 URL，并让它“扫描”漏洞，方法是解析*HTTP 响应*来获取有关软件的信息。然后，它可以将这些信息与已知漏洞的数据集进行对比。

除此之外，他们还可能检查暴露的文件，这些文件可能被用来访问机密信息或提升权限，例如在 WordPress 站点中找到`/readme.html`，从而揭示 WordPress 版本信息。

许多扫描工具会包括**模糊测试器**，用于检查**SQL 注入**和**跨站脚本攻击**（**XSS**），以便检测以前未发现的漏洞。模糊测试器自动化了渗透测试者（或恶意攻击者）为确定用户输入是否存在漏洞而进行的初步过程，一旦发现漏洞，测试者会花时间修改并利用该漏洞来获取信息或访问权限。

此外，如果你的网页应用允许登录功能，大多数**网页应用漏洞扫描工具**都会允许你提供凭证进行身份验证，这将模拟来自已经“突破”登录屏障的恶意攻击者的攻击。

许多付费的专有网页应用漏洞扫描工具会内置不同类型应用的“配置文件”，以减少扫描时间或模拟不同程度的攻击。

一旦扫描工具配置正确，你就可以对组织的网页应用进行扫描，完成后，软件通常会将发现结果整理成报告或网页仪表盘，报告中会解释每个发现、基于风险的漏洞评分，以及潜在的修复步骤。

如果你的网页应用面向外部世界，很可能恶意攻击者已经对你的服务器和应用进行过自动扫描，以检查是否存在漏洞，通常使用下面列出的**开源工具**之一。很难通过**IP 黑名单**来阻止这些攻击，因为它们通常来自被攻陷的机器的 IP 地址，或者根本不遵循特定的模式。这类活动时时刻刻在互联网各处发生。这些扫描往往来自那些寻求“低挂果实”的团体，因此，对自己的应用进行扫描并分析结果是否会引发潜在机会是很重要的。**网页应用防火墙**能够检测这些活动，并防止泄露过多信息，但在这方面，最好的防御方式是确保及时实施服务器操作系统和网页应用软件包的安全更新。

以下是一些网页应用漏洞扫描工具的示例，分为专有和开源选项：

+   **专有**：

    a) Tenable.io/Nessus

    b) Rapid7 InsightAppSec

    c) Acunetix

    d) Detectify

    e) WP Scan

+   **开源**：

    a) Nikto

    b) OWASP **Zed Attack Proxy**（**ZAP**）

    c) w3af

    d) OpenVAS

如果你计划设置自己的网页应用漏洞扫描工具，无论是开源的还是供应商提供的，你应该考虑一些常见问题，涉及漏洞扫描活动的实施。

*你有资源维护一个内部系统吗？*

如果你没有专门的员工负责维护内部漏洞扫描器的工作职责，那么将此需求外包给提供托管服务的第三方可能是有用的，第三方将维护和更新扫描器，确保你获得最新和相关的结果。

另一个值得问的问题如下：

*你打算扫描你的生产 Web 应用程序吗？*

如果你的组织依赖于 Web 应用程序赚钱，并且与客户有 SLA 来确保正常运行，那么是否有意义对其进行扫描，这可能会导致它变慢或停机？

另一种解决方案是建立一个*渗透测试*或*扫描环境*，它是你生产环境的*1:1 克隆*，在软件方面与生产环境相同，但使用虚拟数据集，通常运行在完全独立（且便宜得多）的硬件上。这个解决方案有许多优点：

+   你可以**将 IP 列入白名单**，指定扫描器的*IP 范围*，该范围通常由供应商在文档中提供。如果你自己设置了 Web 应用漏洞扫描器，你应该知道这些 IP。这使你能够限制服务器需要做的工作量，从而确保该环境的需求比生产环境低，成本显著低于真正的复制环境。

+   你避免了因扫描而导致生产系统停机的风险，因为测试环境与产生收入的系统不共享任何资源。

+   你可能在生产环境中有一个**Web 应用防火墙**（**WAF**），但在渗透测试环境中，你可以专门测试你的应用程序，而不是测试 WAF 本身。在这种情况下，你可以通过 WAF 将扫描器 IP 列入白名单，从而使请求可以不经过检查地通过。

在测试环境中使用不同的凭据和帐户，并使用虚拟数据集而非生产数据集，以确保隐私和保密性，通常也是个好主意。此外，拥有一个“渗透测试”数据集，它占用的存储空间比生产数据集少，也可以节省资金。

### 网络漏洞扫描器

**网络漏洞扫描器**在功能和操作上与**Web 应用漏洞扫描器**非常相似，但它们专注于你组织的网络环境，包括员工使用的设备和服务。

许多漏洞扫描器供应商将 Web 应用程序和网络扫描合并到他们的解决方案中，提供一种“一体化”或“单一视窗”的统一自动漏洞评估方法。

通常，你希望网络漏洞扫描器执行以下任务：

+   发现网络中的设备和软件资产。

+   确定设备的软件版本和操作系统版本。

+   检查从收集的信息中获取的已知漏洞。

+   根据风险/漏洞分数报告并优先排序修复步骤。

许多解决方案提供额外的功能，包括以下内容：

+   深网监控，检查你的组织的凭证是否已在市场上被检测到

+   记录网络事件，如用户活动，并与警报进行关联

+   一个用于**网络**（**NIDS**）、**主机**（**HIDS**）和云的**入侵检测系统**（**IDS**）

+   端点检测，可能来自网络事件启发式分析

本质上，这意味着**网络漏洞扫描器**软件能够收集有关你内部网络环境的信息，然后判断是否存在恶意行为者可能利用的漏洞，从而进入你的网络并在网络内部“转移”以提升其特权，最终导致网络被攻陷。

如果你的组织使用过时的操作系统，如*Windows 2008 或 2012 服务器*或*Windows 7 桌面*，那么你的网络漏洞扫描器将像圣诞树一样亮起，你将不得不完成大量的工作来修复这些问题。也就是说，运行这个扫描要比支付数千美元给安全公司，然后让*渗透测试员*在几个小时内攻陷你的网络要便宜得多。通过修复网络漏洞扫描器中发现的问题，你在*去除低悬果实*，并增加了入侵你组织网络所需的技术水平。

一些网络漏洞扫描器的例子，分为*专有*和*开源*选项，可能包括以下内容：

+   **专有**：

    a) Microsoft Security Suite

    b) Tenable.io/Nessus

    c) Rapid7 InsightVM

    d) AT&T Cybersecurity USM Anywhere

    e) Acunetix

    f) Detectify

    g) WP Scan

+   **开源**：

    a) Nikto

    b) OWASP **Zed Attack Proxy**（**ZAP**）

    c) w3af

    d) OpenVAS

除了在环境中进行漏洞扫描之外，还需要考虑你组织开发的任何软件中的漏洞，因此让我们更详细地看一下这个场景。

### 软件开发生命周期（SDLC）或 DevSecOps 扫描

如果你的组织开发软件，无论是供内部使用、客户使用，还是供公众使用（包括网站），那么在**软件开发生命周期**（**SDLC**）中实施安全实践是至关重要的。

在整个过程中有许多机会和阶段可能会引入漏洞，在 *第八章*  *提高软件的安全性*中，我们将深入探讨如何提高软件的安全性并加强安全的软件开发生命周期。直到那时，还是值得关注可以在过程中实施的扫描器，用来检查漏洞代码或软件包，包括以下内容：

+   **静态应用程序安全测试**（**SAST**）工具会扫描你的软件源代码。它们通常会集成在开发人员的**集成开发环境（IDE）**中，或者被设置为自动扫描你代码库中的新条目或提交，例如 GitHub、BitBucket 或 GitLab。通过扫描源代码，软件可以找到常见的陷阱和错误，这些错误可能导致应用程序漏洞，例如 *XSS* 和 *SQL 注入*，即使在应用程序上线后。常见的 SAST 工具示例包括 GitLab 集成的 SAST 工具和 *SonarQube / SonarCloud*。

+   **动态应用程序安全测试**（**DAST**）工具本质上与之前讨论的 Web 应用程序漏洞扫描器相同。它们允许你在软件编译并运行后，通过信息收集和模糊测试对软件进行扫描。通常，DAST 与软件开发生命周期相关，理念是你可以自动触发对每个由开发人员修改的应用程序源代码的临时测试环境的扫描，并根据扫描结果，如果该更改不符合安全基线要求，则拒绝该更改*合并*到生产代码库中。基本上，我的意思是，Web 应用程序漏洞扫描器通常能够配置为软件的*CI/CD 管道*中的 DAST 工具，或者定期进行扫描。

    DAST 工具的示例包括 **Acunetix**、**Rapid7 InsightAppSec/AppSpider**、**Tenable.io/Nessus** 以及 OWASP 的 **Zed 攻击代理**（**ZAP**）。

+   **依赖扫描**工具允许你扫描软件导入的依赖项。开发人员通常会利用其他方已创建的软件，这避免了耗时的开发过程并减少了实现的复杂性，但也增加了将*已知漏洞*引入软件的可能性。依赖扫描器会将导入的模块及其版本与已知漏洞的数据库进行比对，以确保你的软件不会使用到存在漏洞的第三方代码版本。

    *依赖扫描器*的示例包括以下内容：

    a) **Snyk.io** 评估多个语言的导入，包括 JavaScript、Java、.NET、Python、GoLang、PHP 等。

    b) **Node 包管理器**（**NPM**）为 JavaScript 提供了一些内置的依赖扫描器。

    c) **OWASP 依赖项检查项目**。

现在我们已经讨论了如何对你组织的数字资产进行自动化扫描，我认为有必要进一步探讨可以由你组织内部员工执行的其他*内部评估*。

## 内部评估

内部评估是指那些无需外部（第三方）专家帮助就能执行的评估。我们来看一下你可以进行的几种不同类型的内部评估。

### 员工安全意识评估

我们已经讨论过，在我们的组织中给予员工**安全意识测试**，以确保他们已经吸收了提供的信息，并作为对您的*合规性审计*的*尽职*和*持续改进*的证据。一种方法是让员工需要以问答形式回答标准化测试题，以展示他们的知识水平。

另一种方法是利用工具，例如对员工进行**钓鱼训练**，例如发送他们已经接受培训以识别的电子邮件，并记录他们的响应指标。如果维护内部软件和创建新的电子邮件模板的开销在内部无法承受，则第三方也可以作为*托管服务*来执行此项工作。

### 合规性审计

如果您的组织受到诸如**通用数据保护条例**（**GDPR**）或**加州消费者隐私法**（**CCPA**）之类的法规，或者诸如*ISO27001*或 PCI-DSS 之类的标准约束以执行其核心业务目标并为客户提供服务，那么理解您的控制措施的有效性，并找出合规要求与实际情况之间的差距就非常关键。

为此，可以进行**内部合规审计**，作为对将来由监管机构或代表其进行检查的第三方审计的准备。模拟第三方，并调查证据是否存在，以评估控制实施对要求的有效性，是在您真正支付昂贵的审计员前来对您的组织进行评估时，减少时间和精力消耗的绝佳方式。

您必须确保做好记录，并确保所有要求被适当的员工了解，以便实施适当的控制并保持合规性。像*Microsoft Compliance Manager*这样的软件解决方案可以跟踪、分配、安排和记录对超过 300 个全球法规的合规性观察，并提供关于实施方法的解释和指导，这些方法在您的组织中可能非常有效。

### 红队和蓝队

如果您拥有一个合格的内部安全团队，您可以将团队分为**红队（攻击团队）**和**蓝队（防御团队）**，以模拟恶意行为者的攻击方法来攻击您的组织，测试防御团队应对这些攻击的能力，并减少可能造成的损害。

较小的组织在这项工作中将比拥有非常庞大安全团队和大预算的大型企业更加困难，但即使是大型组织也可能发现他们的团队更适合执行防御措施，而不是渗透测试人员已经掌握的攻击性措施，所有这些措施都可以通过第三方参与利用。

有了这些，我们来看一下可以由你的组织进行的第三方评估。

## 第三方评估

当你想评估你的控制措施在风险评估或内部评估中所估算的有效性时，你会想引入**第三方评估员**。当你想测试你的*蓝队*的有效性时，你会想引入第三方评估员。如果你想向潜在和现有客户展示你的安全效果时，你会想引入第三方评估员。当你想遵守标准和法规时，你需要引入第三方评估员。

你可能有很多原因想要或需要引入第三方。归根结底，这涉及到两种特定的理念：*客观性*和*技能*。

在安全公司工作的渗透测试员每天都获得报酬，去“攻占”客户系统，这些系统可能非常先进，也可能是“普通”的。它们使用恶意行为者可能使用的工具，并且在攻防安全方面高效且熟练。此外，由于没有受到办公室政治或既得利益的影响，他们无需讨好你们公司的人；他们是客观的，他们的报告通常清晰、标准化，并且具有可操作性。

第三方可以进行多种评估，且新的“类型”不断涌现。我将提供几个例子。

考虑到我们可能（潜在地）将以下任何安全评估作为内部审查进行，而不是让第三方组织执行测试。

### 技术评估和渗透测试

**技术评估**和**渗透测试**有多种形式，但通常，评估的重点是查看是否可以利用漏洞来获取访问权限，并在此基础上提升权限，直到能够访问机密或敏感数据为止：

+   **Web 应用渗透测试**是由*渗透测试员*或多个*渗透测试人员*针对*Web 应用程序*进行的测试。它模拟了一个恶意行为者试图通过 Web 应用中的功能和/或漏洞来获取访问权限并提升权限。

+   **网络渗透测试**是由*渗透测试员*或多个*渗透测试人员*对组织的网络环境进行的测试。它模拟了一个恶意行为者试图通过安全漏洞远程获取访问权限并提升权限，或者模拟一个内部威胁，假设其初始访问权限有限，然后通过安全漏洞提升权限并访问机密或敏感信息。

+   **红队和黑队** 是模拟**威胁**的活动，复制恶意行为者尝试通过任何必要手段渗透进入您的组织的情景。**红队** 通常专注于信息安全，而**黑队** 则通常专注于物理安全。

    红队和黑队都比传统的渗透测试需要更多的计划和*侦察*工作，但它们总体上代表了更高质量的测试。这对于那些已经建立良好信息安全实践和程序，并在其员工中具有被证明的控制有效性和高级别安全意识的组织非常有价值。通常，**蓝队** 将意识到这一参与，并准备好保护其资产，这需要您的组织进行计划和准备。

继续从*渗透测试*出发，接下来我们将关注风险管理和治理评估。

### 风险管理和治理评估

远离技术评估，我们转向“无聊”的合规审计和认证审查世界。在这里，业务流程和政策将被审查和测试其有效性，需要证据来满足审计员的要求。我之前提到过这些审计; 例如，它们可以包括*PCI-DSS 合规评估*或*ISO27001 认证评估*。

只要审计员技术娴熟，您与评估人员诚实开放，这些评估可能具有巨大的价值。这些评估人员可以发现您流程和程序中的漏洞，并识别您可能没有考虑到的风险，以便轻松地由您组织内的业务利益相关者理解。

不幸的是，如果评估人员没有足够的时间参与，或者没有足够的权限从头到尾对公司进行全面评估，他们可能会错过漏洞和间隙。这就是为什么与评估人员保持诚实和开放，确保您的组织从评估中得到物有所值的重要性所在。

考虑到第三方安全评估可以分为这两种“风格”，我们可以理解以下内容：

+   涵盖整个组织安全姿态的评估通常会是技术和风险管理评估的混合。

+   对您的硬件产品安全控制效果的评估通常会归入技术评估。

+   对您的软件产品安全控制效果的评估也是如此。

+   评估建筑物安全可以通过技术或风险管理评估来完成，但通常我们会考虑“黑队”。

+   你的员工安全意识的第三方评估可以包括钓鱼演习或红队/黑队参与。

+   您的安全团队应通过红队评估来应对主动威胁，在此过程中，您的团队充当蓝队，保护组织的资产。

让我们继续讨论执行安全评估时的最佳实践。

# 执行安全评估的最佳实践

无论您的组织是在进行内部评估，还是聘请第三方评估其信息安全状况，都有一些最佳实践可以有效确保评估的价值最大化。

关键要点如下：

+   确保评估有足够的时间进行彻底完成。匆忙进行评估没有意义，但同样重要的是确保测试不会拖延，确保您宝贵的 IT 和安全人员能够专注于评估，而不是日常工作需求。

+   确保测试范围已定义，以避免进行不相关的评估。

+   确保测试人员和协助测试人员的内部员工都经过良好的培训，准备充分，并且具备相关知识，以提高评估的价值。

还有一些过程可以在不依赖于纯粹出于合规性要求的测试和审计的情况下，用于有效选择合适的评估。

这些过程可以包括以下内容：

+   定义业务需求。

+   定义信息安全目标和策略。

+   从内部角度审查感知的优势和劣势。

+   对资产进行风险评估，包括已知的威胁和漏洞。

+   执行并记录来自网络和 Web 应用程序漏洞扫描的结果。

+   审查并记录系统的安全控制有效性，包括防火墙、VPN、客户端、访问控制机制和其他信息系统。

+   审查并记录来自访问控制列表和访问日志的发现。

+   审查并记录员工的安全意识。

一旦您收集了尽可能多的关于组织的信息（其中许多内容在我们之前多次讨论的风险管理阶段已经完成），您将能够基于风险做出决定，选择需要评估的资产，这样可以比仅仅对所有事物进行完全测试更有效地利用您的预算。

关于最佳实践的另一个简短说明是我之前提到过的：我认为为自动化扫描和（一些）渗透测试设置一个虚拟环境是值得的。这减少了使生产系统停机的风险，并且通过使用虚拟数据，避免暴露真实的客户数据或机密商业信息。这是一种成本效益高的解决方案，用来降低由于安全评估而导致的停机风险。权衡之下，一些认证机构、监管机构和客户可能不会像测试生产环境一样看待对克隆环境的测试，但这些情况可以在出现时进行处理。

在第三方测试结束时，评估人员会花时间撰写报告并提供结果。这些结果是为你的组织带来价值的，而不是支付费用仅仅为了勾选一个框并继续在不必要的风险下工作。这就是为什么诚实能够带来更好的、可操作的改进。你支付专业人士的费用是为了告诉你你的弱点，所以要诚实，获取真实的结果，而不是支付第三方费用后误导他们远离你流程和实践的实际情况，这样你的组织就能继续重复犯同样的错误。

让我们来看一下这些结果是如何呈现的。

# 解释安全评估结果

当我们查看安全评估的结果时，有两种类型，类似于我们在上一节中对第三方评估的划分。这两种类型分别是技术评估和风险管理与治理评估。

这两种类型的报告通常会尝试通过给每个发现的漏洞分配一个分数（可能是 1-5、1-10，或其他量表）来量化漏洞带来的风险水平。重要的是，你需要在风险评估过程中考虑资产的价值，因为有时一个漏洞可能被认为具有较高的可利用性，但可能不值得去缓解，因为它不会保护任何有价值的东西。换句话说，所呈现的风险水平低于风险接受水平。

通常，技术报告会包括渗透测试如何逐步进行的叙述，并附有截图、命令和其他信息，以帮助客户复制发现的结果并测试他们的修复措施。这些对于信息安全专业人士来说是无价的贡献，因为它们不仅作为你组织 IT 员工的教程，还帮助你将威胁呈现给非技术人员和高层管理人员。它为恶意行为者的思维提供了一个很好的第一人称视角，并有助于让威胁变得更真实。

在涉及第三方审查时，无论报告是技术性的还是非技术性的，通常都会包含由第三方交付的图表、图形和展示材料，并以“发现展示”的形式呈现。将公司相关利益方纳入会议非常重要，因为许多人不会阅读 PDF 报告。说实话：大多数人邮箱里有成千上万封未读邮件，那为什么他们会关注你那份枯燥的 PDF，里面写的是他们的业务是如何被*轻松攻破*的呢？

除了这些发现外，还会有修复步骤的建议。这些页面的价值不可估量。你基本上是在“坏人”告诉你如何防止他们（或具备相同技能的其他人）下次进入！因此，我的建议是按照他们的指导进行操作。你将需要计划如何更新和重构系统、修改密码以及招聘员工，所以第一步是确保你有必要的资源和批准。记住：发现展示将会唤醒高层管理人员，并成为一个很好的机会，让你在问题尚在他们脑海中的时候请求批准这些资源。

同样适用于*内部审查*，包括*自动化评估和扫描*的结果。你有度量标准以及可以采取的措施来控制风险，这些内容已经被量化，并以引人注目的方式展示，以帮助你向高层管理人员展示你的发现。不要错过向老板展示你*信息安全计划*价值的机会——这就是他们支付你薪水的原因。

在修复阶段，进行内部验证是非常重要的。这可以成为一个有益的机会，帮助 IT 和开发人员了解安全漏洞的危险，同时也提高了你组织的整体安全意识。此外，内部验证修复措施可以避免尴尬，因为你最不希望发生的情况是安排第三方进行后续测试，结果他们又做了完全相同的事情，浪费了时间、金钱和资源。

这让我进入最后一个要点：持续改进。你需要安排后续检查，以验证你的修复措施是否有效，然后你还需要为未来安排另一个测试，看看评估人员能否发现其他弱点。

# 总结

现在我们已经到了这一章的结尾，我知道你已经能够理解安全控制测试，包括如何安排外部和内部的安全审计，如何分析报告和审查测试结果，以及如何管理每次评估中产生的行动。

现在你已经了解了，可以进行各种不同的安全评估，以帮助你了解如何保护和改善整个组织的安全态势，以及你的网络和数字资产，从组织所创建的硬件和软件到物理安全和员工意识。

此外，你现在也知道了进行这些类型评估的不同方式，例如让你自己的员工进行*内部审查*，或是让其他组织进行*第三方审查*。此外，还可以进行自动化评估，你也了解了几种不同的自动化安全测试方法。

在我们讨论了安全评估如何帮助你的组织改善安全性并简化操作之后，我认为接下来讨论*第七章*，*拥有安全运营*，是有意义的。
