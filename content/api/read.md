---
title: "读取监控数据"
weight: 9
---

首页有个架构图，大家可以看到，夜莺把接收到的监控数据都直接写入了后端时序数据库，所以，读取监控数据，无需经由夜莺的接口，直接读取后端的时序库的接口就可以了。即：如果使用了 Prometheus，就通过 Prometheus 的接口读取监控数据，如果用了 VictoriaMetrics，就通过 VictoriaMetrics 的接口读取监控数据。

比如 Prometheus，就是那些`/api/v1/query` `/api/v1/query_range`之类的接口。相关接口文档请参考：[Prometheus官网](https://prometheus.io/docs/prometheus/latest/querying/api/)
