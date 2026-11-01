# 已分清环境选择、数据库地址和秘密注入

用户能识别 development/test/production 的 worker mode，并能写出 PowerShell 的 `LOCO_ENV` 切换命令；已澄清 production 的 `DATABASE_URL` 由环境变量提供，数据库类型不固定，不等于 SQLite。

Evidence: 第十一课回答中正确指出测试使用 `ForegroundBlocking`、生产秘密不应有默认值。
