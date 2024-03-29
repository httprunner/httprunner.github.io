---
title: 开源项目-扬帆测试平台
weight: 6
description: 基于 HttpRunner v4 搭建自动化测试平台
---

## 项目介绍

<img src="/image/logo/yangfan.png" title="扬帆自动化测试平台" width="120">

扬帆测试平台是一款基于 gin-vue-admin 为框架，以 HttpRunner v4 go 模块（以下简称hrp）为测试引擎搭建的自动化测试平台，致力于打造最易使用的开源测试平台。与大多数测试平台不同，扬帆测试平台采用了 go 语言进行开发，具有良好的性能和稳定性，同时在部署方式和复杂度方面也更加简单，减轻了用户的部署负担。

在设计理念上，扬帆测试平台注重实用性和易用性，平台界面简洁明了，用户可以通过简单的操作完成测试任务的创建、执行、查看和管理。平台提供了完整的测试流程支持，包括测试用例管理、测试计划管理、测试报告生成等，让测试工作更加规范和高效。

作为一款自动化测试平台，扬帆测试平台自然也支持接口自动化测试。平台已经实现了接口自动化测试中最关键的部分，包括测试用例的编写、执行、性能测试和结果分析等。同时，平台还提供了丰富的接口测试功能，包括参数化测试、前置后置处理、断言验证、函数驱动、hooks等，满足用户在接口测试中的不同需求。

除此之外，扬帆测试平台后续将支持多种测试类型，包括 UI 自动化测试、k8s 部署、分布式压测、消息通知等，满足不同场景下的测试需求。平台提供了灵活的扩展机制，用户可以根据实际需求开发自己的测试插件，实现更多的测试类型和功能。

总的来说，扬帆测试平台是一款易用且功能丰富的自动化测试平台，适用于各类软件测试工作，为用户提供高效的测试支持，助力测试工作的顺利进行。

案例提供人：[扬帆](https://gitee.com/test-instructor/yangfan)

## 平台功能

1. 项目管理：项目创建后会初始化函数驱动，可根据实际需要对项目进行划分，各项目数据相互独立，无法查看、引用其他项目的数据
2. 环境变量：用于不同环境中相同变量的设置，所有模块都必须有环境变量
3. 配置管理：公共数据配置，可以配置域名、请求头、变量和前置套件等
4. 树形菜单：接口管理、测试套件、测试用例都包含了树形菜单，可以根据树形菜单对接口按功能模块、服务等进行划分，方便用例管理
5. 接口管理：接口测试最基础模块，测试用例、测试套件、定时任务等都依赖与接口管理
6. 测试套件：数据从接口管理的数据复制过来，数据相互独立，互不影响；运行配置只在调试时生效，测试用例、定时任务执行时无效
7. 测试用例：引用测试套件，执行时以测试用例的配置为主；测试套件的修改，会导致测试用例运行报错、无法运行等
8. 定时任务：引用多个定时任务，执行时各用例项目独立，没有依赖
9. 性能任务：引用测试套件，增加性能测试相关特性（如：事务、集合点等）
10. 测试报告：展示除压测任务的报告外的所有接口调试、运行报告
11. 性能测试报告：展示性能测试报告
12. 环境变量(`开发中`)：自行设置`开发环境`、`测试环境`、`预发布环境`等多个环境，相对固定的变量进行设置，如：域名、账号等

## 为什么选择 HttpRunner？

在选择自动化测试平台的技术时，我们经过了一番思考和比较，最终决定采用 go 语言作为开发语言，并选择了基于 go 语言的 HttpRunner v4 框架作为我们的核心测试执行框架。当时我们发现，还没有特别合适的测试执行框架，并且我们也无法忍受将测试用例转换成文件后再运行的低效率。在了解到 HttpRunner 即将用 go 语言重写后，我们迫不及待地开始了尝试。

HttpRunner 是一个功能丰富的自动化测试框架，它支持多种协议、包括 HTTP、WebSocket、RPC 等。同时，它还具备 UI 自动化和性能测试的能力，并且易于扩展。我们深深地被它的特点所吸引，这也是我们选择 HttpRunner 作为我们的核心测试执行框架的重要原因之一。

在我们的实际应用中，我们已经验证了在项目中接入 HttpRunner 的方案，并且得到了比较好的效果。相较于 v3 版本，我们可以避免将测试用例转换成文件后再运行的低效率，从而大大提升了测试执行的效率。同时，我们还在不断地拓展测试平台的功能，例如我们目前已经支持 grpc 协议的接口测试，并且我们也将继续增加 UI 自动化、SQL 等功能，以满足不同场景下的测试需求。

我们认为，选择一个合适的自动化测试平台是非常重要的。我们选择了 HttpRunner 作为我们的核心测试执行框架，这不仅因为它支持多种协议、易于扩展、并且有很好的性能，同时也因为我们相信它将能够满足我们未来的测试需求。

## HttpRunner 使用情况

我们正在一个项目中使用 HttpRunner 进行接口自动化测试，并且尝试解决加解密问题。在这个项目中，所有的接口都进行了加解密处理，如果使用传统的测试框架，我们需要对每个接口的数据进行单独处理，这样就会导致冗余代码的数量大大增加，并且后期维护也比较困难。

但是，我们发现使用 HttpRunner 可以轻松解决这个问题。虽然 HttpRunner 支持 hook 功能，但是无法直接修改请求和返回的数据。因此，我们对这部分内容进行了二次开发，仅花费了不到 2 小时的时间，就成功地解决了这个问题，并验证了 HttpRunner 的高度拓展性。

总的来说，我们非常满意使用 HttpRunner 进行接口自动化测试的效果，并且通过这个项目的实践，我们深刻认识到了 HttpRunner 的优点，例如易于使用、高拓展性、以及支持多种协议等等。在未来的测试工作中，我们将继续使用 HttpRunner，以提高测试效率和减少测试代码的冗余。

- [开源项目源码](https://gitee.com/test-instructor/yangfan)
- [项目官网](http://www.yangfan.gd.cn/)
- [demo](http://82.157.150.119:8080/)【账号：admin，密码：123456】
- [使用文档](https://blog.csdn.net/weixin_46616730/article/details/128473359)

## 后续展望

目前我们在自动化测试平台中已经完成了接口测试和性能测试部分，并且在项目中进行了初步验证。我们发现，使用自动化测试平台可以大大节省时间并减少冗余代码，这让我们感到非常满意。

虽然我们目前只实现了接口测试和性能测试，但是在未来我们将继续对平台进行优化和迭代，以便更好地服务于项目的需求。我们将会考虑加入UI测试、数据库测试等功能，以满足更多的测试需求。我们相信，这个自动化测试平台将会成为我们项目中不可或缺的一部分，为项目的稳定运行和高质量交付提供坚实的保障。
