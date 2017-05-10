Flink用户案例

为了展示如何使用Flink处理无限数据集（unbounded dataset），下面列举了一些真实场景中的Flink用户，以及他们正在使用Flink解决的问题。

更多示例，请参考[Powered by Flink](http://flink.apache.org/poweredby.html)页面。

- 实时优化电商系统中的搜索结果：Alibaba搜索基础设施团队使用Flink实时更新商品详情页和库存信息，提高用户的相关性。
- 为数据科学团队提供流式处理服务：King（糖果粉碎传奇游戏的作者）通过Flink支撑的内部平台，为它的数据科学家们实现了实时分析服务，极大缩短了理解游戏数据的时间。
- 网络／传感器监控和错误检测：Bouygues Telecom，法国最大的电信提供商之一，用Flink监控它的有线和无线网络，获得了快速地响应全国范围内故障的能力。
- 服务商业智能基础设施的ETL：Zalando使用Flink处理数据，以便更简单地将数据导入数据仓库，能将复杂的数据转化为相对简单的数据，同时让分析师们能更快的访问数据。

从这些用户案例中我们能梳理出一些共性。基于上述案例，我们能看出Flink非常适合用于：

1. 种类繁多的（有时候不稳定的）数据源：当数据在上百万不同用户或设备上产生，基本确定会有部分数据到达服务器端的顺序会和真实顺序不同，当发生更严重的上游错误时，一些事件可能比实际预期时间晚数小时达到。需要处理好这些晚到的数据，以保证结果的准确性。

2. 应用有状态： 当应用变的越来越复杂，不再只是简单地过滤或者增强数据记录，管理这些应用（例如，统计计数，已处理数据的窗口，状态机，嵌入式数据库等）的状态将会变得很困难起来。Flink提供了工具，让状态管理从外部看来变得高效、容错和可管理，你不需要自己构建这些能力。

3. 数据需要被快速处理：在这些实时或准实时场景中，需要在数据产生的瞬间，就能得到数据的相关分析结果。Flink能够满足这些实时性要求。

4. 数据体量大：为支持这样的数据规模，应用需要被部署到上千个节点多的分布式环境中。Flink能跑在大型集群上，和跑在小规模集群上一样顺滑。

如果想查看更多用户案例，我们推荐年度Flink用户大会[Flink Forward 2016](http://flink-forward.org/program/sessions/)上的主题演讲。