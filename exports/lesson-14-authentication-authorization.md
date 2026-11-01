# 第十四课产出：认证与授权

本课区分 `auth::JWT`（验证 token、只给 claims）与 `auth::JWTWithUser<users::Model>`（验证后加载用户），并建立 401/403 的业务边界。

交付物：

- [第十四课](../lessons/0014-authentication-authorization.html)
- [认证与授权速查](../reference/auth-authorization.html)

依据：工作区现有 categories/auth controller 与 Loco 官方 JWT 文档。
