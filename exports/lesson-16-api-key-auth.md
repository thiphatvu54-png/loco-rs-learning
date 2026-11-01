# 第十六课产出：API Key 认证

本课介绍 `auth::ApiToken<users::Model>`：从 Bearer header 读取长期 API key，调用 `find_by_api_key` 加载用户，适合 CLI 和机器对机器调用。

交付物：

- [第十六课](../lessons/0016-api-key-auth.html)
- [API Key 认证速查](../reference/api-key-auth.html)

依据：工作区 users 模型的 `api_key` / `Authenticable` 实现与 Loco 官方 API key 文档。
