# 第十三课产出：请求测试的数据边界

本课解释 `init_user_login` 为什么同时调用 HTTP 和 `ctx.db`：HTTP 验证接口行为，测试数据库提供 pid/token 并验证副作用。测试使用独立的 test 配置，不连接 production 数据库。

交付物：

- [第十三课](../lessons/0013-request-test-data.html)
- [请求测试数据速查](../reference/request-test-data.html)

依据：工作区 `tests/requests/prepare_data.rs`、`config/test.yaml` 和 Loco 官方 request-test 文档。
