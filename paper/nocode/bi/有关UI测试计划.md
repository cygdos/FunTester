# 有关UI测试计划



[UI测试](https://mp.weixin.qq.com/s/wDvUy_BhQZCSCqrlC2j1qA)是用户在网站或者APP上进行的。良好的用户界面和交互可以吸引用户使用，这就是为什么测试用户界面至关重要的原因，[UI测试](https://mp.weixin.qq.com/s/wDvUy_BhQZCSCqrlC2j1qA)是软件周期的一个非常重要的阶段。

本文中将介绍不同UI测试过程。测试中的主要组件：**测试计划**，**测试方案**，**测试用例**。将分享如何制定良好的UI测试计划以及如何创建它们以测试应用程序。

# 如何制定好的UI测试计划

UI测试计划是与应用程序测试相关的**正式文档**。这包括应用程序的**范围**，**测试方法**，**测试相关活**动等。这非常重要，也是应用程序测试的第一步。

# UI测试计划的先决条件

一个好的UI测试计划总是从确定可用于测试的不同资源开始，需要的资源包括具有所需技能，工具和文档的质量检查专业人员。

创建良好的UI测试计划的第一步是文档。此后，至关重要的是，测试团队准备描述应用程序的不同要求和基本信息的正式文档。

在确定可用于UI测试的资源之后，还需要确定需要测试的不同关键区域的优先级，要遵循的测试方法所需的资源以及它们各自的文档。

另外，每个好的测试计划都应包括响应测试和跨浏览器测试，以便为用户提供最佳的`UI/UX`体验。

# 为什么要制定UI测试计划

在开始UI测试之前，有一个测试计划很重要。一个好的UI测试计划可以帮助测试团队创建整个过程的结构图，更好地管理测试的时间成本，并提供参考指南以确保每个人都按计划进行。

UI测试计划的重要性如下：

* 创建结构图：测试计划创建如何进行UI测试的结构图。创建UI测试计划将突出显示将需要的测试类型（例如[探索性测试](https://mp.weixin.qq.com/s/nebHPfKbCO0f-G24qCh9wA)，[自动化测试](https://mp.weixin.qq.com/s/qHmcblN4cD4JK6jT7oU4fQ)，[可用性测试](https://mp.weixin.qq.com/s/aUIg40scOWzbRR89ojJWLg)，[如跨浏览器测试](https://mp.weixin.qq.com/s/MB_Wv7yQ6i9BztAZtL4grA)等），并最终帮助您在团队中分配任务。
* 估计总时间： UI测试计划有助于估计测试所需的总时间。有了它的帮助，可以为测试团队提供精确截止日期，并为生产团队或用户提供估计日期。
* 测试详细指南： UI测试计划是测试过程的详细指南。因此，它可以帮助测试区域以外的人员（例如开发人员，用户，业务经理，业务分析师等）了解正在详细遵循的流程。
* 识别资源： UI测试计划强调了测试阶段所需资源的大小和数量。这些资源会根据项目而有所不同，例如硬件，基于云的服务器，测试所需的Web应用程序等。
* 降低风险： UI测试计划突出了项目测试中涉及的风险。揭示不同的风险可以帮助提供风险管理解决方案以应对这些风险。这样可以提高测试效率。
* [自动化测试解决了什么问题](https://mp.weixin.qq.com/s/96k2I_OBHayliYGs2xo6OA)： UI测试计划应包括哪些测试方案或测试需要自动化。一些测试是重复性的，可以自动进行[Selenium自动化测试](https://mp.weixin.qq.com/mp/appmsgalbum?action=getalbum&album_id=1319034944479510528&__biz=MzU4MTE2NDEyMQ==#wechat_redirect)测试。使某些测试自动化将提高这些测试的准确性和速度。
* 创建浏览器矩阵：在创建测试策略时，您需要确保您的网站在所有浏览器上都能无缝运行。创建浏览器矩阵后，您需要对网站执行[跨浏览器测试](https://mp.weixin.qq.com/s/MB_Wv7yQ6i9BztAZtL4grA)。


# 如何编写UI测试计划

由于测试计划更多是包含描述，因此了解UI测试计划中应包含的内容非常重要。因此，在创建测试计划时应记住的一些关键点包括：

* 需要专业人员（具有各自的技能）。
* 测试Web应用程序所需的总时间。
* 团队将遵循不同的测试技术。
* 测试所需的资源，例如工具，硬件，文档等。
* 用于跨浏览器测试的目标测试环境，例如OS，设备，浏览器等。
* 测试的最终目标。

记录完上述要点后，就可以使用冒烟测试或[可用性测试](https://mp.weixin.qq.com/s/aUIg40scOWzbRR89ojJWLg)来创建UI测试计划。

冒烟测试将帮助识别应用程序中的简单BUG，但不要太深入。冒烟测试可以说是测试应用程序的第一步。如果应用程序未通过基本功能测试，则需要进行深度响应测试或兼容性测试。

健全性测试与冒烟性测试相反，在冒烟性测试中，它确定应用程序的新代码和修改后的代码，并检查其是否符合要求。与冒烟测试不同，健全性测试非常严格，并且对功能进行了更深入的测试。在应用程序通过冒烟测试之后，执行完整性测试。

记录完UI测试计划后，就可以继续为项目创建测试方案。

# 为UI测试编写良好的测试方案

测试方案是需要测试什么的整体概念。这将包含一组测试用例，这些用例将作为场景的正面或负面结果。由于测试方案说明了用户将在网站上使用的功能，因此测试人员考虑最终用户的想法并据此创建测试方案非常重要。

UI测试计划中的测试方案尤其重要，其优势在于：

* 测试方案可帮助其他与业务相关的团队了解测试人员将在应用程序中进行哪些测试的概述。通过测试方案，他们可以根据自己的要求修改或更改任何方案。
* 测试场景涵盖了完整的测试用例，因为它们属于一个整体。这有助于为应用程序创建广泛的测试范围，并确保更好的测试。
* 测试方案有助于确定应用程序不同区域的优先级，从而帮助测试人员专门关注这些区域。
* 测试方案对于研究应用程序的端到端流程非常重要。

# 如何编写用于UI测试的测试方案

编写测试方案是一个逐步的过程，有助于实现更大的测试范围并满足要求。

* 浏览要测试的应用程序的文档，测试计划，手册等。这将帮助您了解完整的应用程序。
* 弄清楚应用程序的不同功能被最终用户的使用场景。由于测试场景是基于用户创建的，因此最好在此过程中更加真实地模拟用户行为。
* 完成以上两个步骤后，列出想出的测试方案。
* 创建刚刚列出的测试方案的可追溯性矩阵，以验证是否满足所有要求。
* 请其他管理人员或相关人员评审测试方案。
* 在计划中包括跨浏览器测试和响应式测试方案，以确保良好的用户体验。
* 到目前为止，已经完成了为项目创建UI测试计划和测试方案的工作。下一步是编写测试方案所涵盖的具体测试用例。

# 为UI测试编写好的测试用例

UI测试计划和测试方案是编写系统功能测试的方法论，而测试用例提供了针对这些功能要进行的测试内容。测试的结果决定了该功能是否正常工作（通过了测试用例）或否（测试用例失败了）。测试用例涉及要在项目上执行的条件、数据以及结果。这些信息通常在测试用例内部。因此可以将测试场景视为更大范围的测试用例。

测试用例是整个UI测试过程不可或缺的一部分。编写测试用例的重要性在于：

* 测试用例可以更好地控制项目的逻辑和流程。
* 测试用例有助于揭示用户操作时可能出现的错误。由于测试用例模仿最终用户，因此很容易发现一些隐藏的错误。
* 测试用例为测试提供了更好的流程。测试人员知道先要测试什么，然后再进行测试等等。
* 如果以适当且有条理的方式编写测试用例，它们将使软件质量得到很好的保证。


# 如何编写好的测试用例？

如果以正确的方式编写测试用例，则它们可以提供更大更准确的测试范围和更有效的测试。因此，这应该是一个深思熟虑的过程。这里有一些技巧可以编写更好的测试用例。

* 请在测试场景下编写测试用例。测试场景就像文章的标题一样，如果在测试场景下编写测试案例。
* 包括执行测试所需的条件和最终的预期结果。这有助于其他测试人员快速了解测试的预期目的。
* 不要只关注正面的用例，更要记下负面的测试用例。
* 始终执行遗落角落的测试用例或异常测试用例。
* 不要创建关联性较强的测试用例。
* 记录在测试案例中包括以下内容：测试用例ID、测试案例的标题、风险等级（高/低）、使用的测试类型、预期内容等等。

测试用例所测功能非常确定，而测试用例则会很庞大。在测试方案部分中，如何[简化测试用例](https://mp.weixin.qq.com/s/BhwfDqhN9yoa3Iul_Eu5TA)显得非常重要。

---
* **郑重声明**：“FunTester”首发，欢迎关注交流，禁止第三方转载。更多原创文章：**[FunTester十八张原创专辑](https://mp.weixin.qq.com/s/Le-tpC79pIpacHXGOkkYWw)**，合作请联系`Fhaohaizi@163.com`。

### 热文精选

- [接口功能测试专辑](https://mp.weixin.qq.com/mp/appmsgalbum?action=getalbum&album_id=1321895538945638401&__biz=MzU4MTE2NDEyMQ==#wechat_redirect)
- [性能测试专题](https://mp.weixin.qq.com/mp/appmsgalbum?action=getalbum&album_id=1319027448301961218&__biz=MzU4MTE2NDEyMQ==#wechat_redirect)
- [Linux性能监控软件netdata中文汉化版](https://mp.weixin.qq.com/s/fdXtK-5WwKnxjLZdyg6-nA)
- [图解HTTP脑图](https://mp.weixin.qq.com/s/100Vm8FVEuXs0x6rDGTipw)
- [接口测试代码覆盖率（jacoco）方案分享](https://mp.weixin.qq.com/s/D73Sq6NLjeRKN8aCpGLOjQ)
- [写给所有人的编程思维](https://mp.weixin.qq.com/s/Oj33UCnYfbUgzsBzEm2GPQ)
- [好书推荐《Java性能权威指南》](https://mp.weixin.qq.com/s/YWd5Yx6n7887g1lMLTcsWQ)
- [Selenium并行测试最佳实践](https://mp.weixin.qq.com/s/-RsQZaT5pH8DHPvm0L8Hjw)
- [性能测试、压力测试和负载测试](https://mp.weixin.qq.com/s/g26lpd7d7EtpN7pkiqkkjg)
- [如何维护自动化测试](https://mp.weixin.qq.com/s/4eh4AN_MiatMSkoCMtY3UA)
- [负载测试最佳实践](https://mp.weixin.qq.com/s/hNj7UsCCvv9TdexAcNFUvg)

![](https://mmbiz.qpic.cn/mmbiz_jpg/13eN86FKXzCxr0Sa2MXpNKicZE024zJm73r4hrjticMMYViagtaSXxwsyhmRmOrdXPXfS5zB2ILHtaqNSoWGRwa8Q/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)