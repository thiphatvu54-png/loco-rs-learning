# 第十课产出：Scheduler + Task

本课把定时触发和业务逻辑拆开：`Task` 负责可手动执行的工作，`Scheduler` 只负责按时间调用 Task。课程覆盖专用 `config/scheduler.yaml`、英文 schedule、`--list` 与 `--name`。

交付物：

- [第十课](../lessons/0010-scheduler-task.html)
- [Scheduler + Task 速查](../reference/scheduler-task.html)

依据：工作区现有 `user:create` / `user:delete` Task，以及 Loco 官方 Scheduler 文档。
