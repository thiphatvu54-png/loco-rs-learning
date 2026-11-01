# Resources

只认三个官方来源。文档和源码不一致时，以源码 / 当前发布版为准。

## Knowledge
- [loco.rs](https://loco.rs/) — 官网首页，版本与整体介绍。
- [loco.rs/docs](https://loco.rs/docs/) — 官方文档入口（教程 / How-to / Reference / Explanation 四类）。
- [github.com/loco-rs/loco](https://github.com/loco-rs/loco) — 源码。版本看根 `Cargo.toml`，改动看 `CHANGELOG.md`；`loco` CLI 在 `loco-new/`。
  - [Cargo.toml](https://github.com/loco-rs/loco/blob/master/Cargo.toml) — `loco-rs` 当前版本和 feature 列表。
  - [CHANGELOG.md](https://github.com/loco-rs/loco/blob/master/CHANGELOG.md) — 每版改了什么、怎么升级；注意顶部 `Unreleased` 段还没发布。
- [Your First App](https://loco.rs/docs/tutorials/your-first-app/) — 安装、`loco new`、`cargo loco start`、第一个 scaffold。第 1 课主读。
- [CLI reference](https://loco.rs/docs/reference/cli/) — `loco new` 全部参数和 `cargo loco` 全部子命令。查命令时用。
- [Coming from Axum](https://loco.rs/docs/explanation/coming-from-axum/) — axum 概念到 Loco 的对照。你有 axum 底子，这页最省力。
- [Architecture: the request lifecycle](https://loco.rs/docs/explanation/architecture/) — 启动流程、AppContext、请求怎么走、中间件为什么是 LIFO。
- [Add a controller](https://loco.rs/docs/how-to/add-controller/) — 写路由和 handler。
- [Configuration](https://loco.rs/docs/reference/configuration/) — `config/*.yaml` 每个键。
- [Generators & field types](https://loco.rs/docs/reference/generators/) — `cargo loco generate` 全部生成器和字段类型写法。
- [Protect a Route with JWT](https://loco.rs/docs/how-to/jwt-auth/) — 后台登录鉴权。
- [Paginate query results](https://loco.rs/docs/how-to/paginate/) — 列表分页。
- [Validate requests](https://loco.rs/docs/how-to/validate-requests/) — 参数校验。
- [Handle errors](https://loco.rs/docs/how-to/handle-errors/) — 错误和 HTTP 状态码。
- [Write request (controller) tests](https://loco.rs/docs/how-to/request-tests/) — 接口测试。

## Wisdom (Communities)

- [Paginate query results](https://loco.rs/docs/how-to/paginate/) — `PaginationQuery`、过滤和分页元数据。

- [Protect a Route with an API Key](https://loco.rs/docs/how-to/api-key-auth/) — `ApiToken<T>`、`find_by_api_key` 和 Bearer API key。

- [Protect a Route with JWT](https://loco.rs/docs/how-to/jwt-auth/) — `JWTWithUser` 加载用户并保护业务路由。

- [Protect a Route with JWT](https://loco.rs/docs/how-to/jwt-auth/) — `JWT`、`JWTWithUser` 和受保护路由。

- [Write request tests](https://loco.rs/docs/how-to/request-tests/) — 测试启动、TestServer、请求断言和测试数据库。

- [Configure logging](https://loco.rs/docs/how-to/configure-logging/) — 日志级别、格式和生产 JSON 输出。

- [Configuration](https://loco.rs/docs/reference/configuration/) — 环境选择、`get_env`、配置覆盖和环境变量。

- [Schedule recurring jobs](https://loco.rs/docs/how-to/schedule-jobs/) — Scheduler 配置、英文时间表达式、Cron、`--list` 与 `--name`。

- [Add a background worker](https://loco.rs/docs/how-to/add-worker/) — 生成、注册和调用 `BackgroundWorker`，包含 job id 与 batch enqueue。
- [The background-processing model](https://loco.rs/docs/explanation/background-processing-model/) — 解释 `BackgroundAsync` / `ForegroundBlocking` / `BackgroundQueue` 的统一接口。
- [GitHub Discussions](https://github.com/loco-rs/loco/discussions) — 官方仓库的讨论区。适合问“这样设计对不对”、DDD 分层怎么放这类判断题，回答可被搜索。
- [官方 Discord](https://discord.gg/fTvyBzwKS8) — 链接来自官方 README。适合快速问答、卡住时求助。

## Gaps
- [Configuration](https://loco.rs/docs/reference/configuration/) — `settings:` 与 `Config::settings::<T>()` 的应用自定义配置。
- 官方文档没有专门讲 DDD 分层的页面。DDD 部分只能从 Loco 的默认结构（controllers / models / dtos / workers）出发自己推，需要判断时去 Discussions 问。

- [Add middleware](https://loco.rs/docs/how-to/add-middleware/) — `Routes::layer` 的路由组作用域。
- [Protect a Route with JWT](https://loco.rs/docs/how-to/jwt-auth/) — `JWT` 与 `JWTWithUser` 的 handler 边界。
- [Write request (controller) tests](https://loco.rs/docs/how-to/request-tests/) — `request::<App, _, _>`、TestServer 与状态断言。

- [Handle errors](https://loco.rs/docs/how-to/handle-errors/) — Loco 错误到 HTTP 状态和 JSON 的映射。

- [Middleware catalog](https://loco.rs/docs/reference/middleware/) — MiddlewareLayer、默认栈顺序和 MiddlewareStackExt。
- [Hooks trait](https://loco.rs/docs/reference/hooks/) — Hooks::middlewares 的全局扩展点。

- [Add middleware — custom middleware](https://loco.rs/docs/how-to/add-middleware/) — 自定义 MiddlewareLayer、map_response 和注册方式。
