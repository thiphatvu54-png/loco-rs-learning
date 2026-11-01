# 第八课产出：后台任务三分法

## 目标

围绕 `playground/admin_api` 学会区分 `Task`、`BackgroundWorker`、`Scheduler`，并补完已有 `DownloadWorker` 的最小执行逻辑。

## 证据

- `src/workers/downloader.rs` 已有 `BackgroundWorker<DownloadWorkerArgs>` 骨架，`perform` 当前是 TODO。
- `src/app.rs` 的 `Hooks::connect_workers` 已注册 `DownloadWorker`。
- `config/development.yaml` 使用 `BackgroundAsync`。
- `config/test.yaml` 使用 `ForegroundBlocking`。
- 官方文档说明 `perform_later` 返回 `Result<String>` job id，参数应可序列化并优先传标识符。

## 交付物

- [第八课](../lessons/0008-background-workers.html)
- [后台任务速查](../reference/background-workers.html)

学习记录暂不写入“已掌握”：需要用户完成练习并说明结果后再记录。

## 验证

- `cargo fmt --check`：通过。
- `cargo test`：36 passed，0 failed。
- `cases/lesson-8/state.json`：可解析，`next_steps` 已写入练习步骤。
