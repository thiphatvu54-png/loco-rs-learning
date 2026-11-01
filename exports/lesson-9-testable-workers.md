# 第九课产出：让 Worker 可测试

本课把 `DownloadWorker` 接到受保护的 POST 接口：controller 负责入队并返回 `202 + job_id`，Worker 负责执行。测试环境使用 `ForegroundBlocking`，因此可以稳定断言 Worker 的副作用。

交付物：

- [第九课](../lessons/0009-testable-workers.html)
- [Worker 测试速查](../reference/worker-testing.html)

依据：工作区的 `config/test.yaml`、`tests/requests/admin.rs`，以及 Loco 官方 worker 文档。

验证：课程文件、速查页与状态 JSON 均可读取；`cargo fmt --check` 通过；现有项目 `cargo test` 为 36 passed / 0 failed。
