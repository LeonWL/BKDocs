## 蓝盾软件升级

版本升级一般伴随着 env 模板及 sql 变更。
主要注意如下前置步骤：
1. 需要先使用 `./bin/prepare-bk-ci.sh` 自动放置新的 env 模板到指定路径。
2. 需要检查是否需要进行 env 修改，一般模板会提供默认 可用 / 兼容 的值。如果安装包没有随附 env 变更说明，一般无需变动。
3. 重新导入 `*.sql`及 `*iam.json`等文件。虽然`./bin/sql_migrate.sh`创建了 flag 文件避免重复导入，但蓝盾的 sql 默认支持重复导入，故`./bin/prepare-bk-ci.sh`里有检测 MySQL flag 文件并删除的逻辑。
4. 停止全部蓝盾服务。如果使用了高可用方案，需要自行编写脚本实现 精确停止特定服务并更新特定的服务，然后启动，依此类推，实现平滑滚动升级。

完成上述检查后，即可直接执行安装脚本。
