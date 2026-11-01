# 已分清 Worker 的入队边界和执行边界

用户能说明 controller 调用 `perform_later`、worker 在 `perform` 中查询 Model。随后明确：`perform_later` 负责入队并返回 job id，`perform` 才执行任务；这个边界是下一课测试 HTTP `202` 和 worker mode 的基础。

Evidence: 第八课练习对话中，用户正确描述了 controller 与 worker 的职责；教师纠正了“入队”和“执行”的区别。
