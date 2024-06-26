# 配置PM2

- [阅读官方文档](https://github.com/Unitech/pm2)

PM2参数说明:

- apps：json结构，apps是一个数组，每一个数组成员就是对应一个pm2中运行的应用
- name：应用程序的名称
- cwd：应用程序所在的目录
- script：应用程序的脚本路径
- exec_interpreter：应用程序的脚本类型，这里使用的shell，默认是nodejs
- min_uptime：最小运行时间，这里设置的是60s即如果应用程序在60s内退出，pm2会认为程序异常退出，此时触发重启max_restarts设置数量
- max_restarts：设置应用程序异常退出重启的次数，默认15次（从0开始计数）
- exec_mode：应用程序启动模式，这里设置的是cluster_mode（集群），默认是fork
- error_file：自定义应用程序的错误日志文件
- out_file：自定义应用程序日志文件
- pid_file：自定义应用程序的pid文件
- watch：是否启用监控模式，默认是false。如果设置成true，当应用程序变动时，pm2会自动重载。这里也可以设置你要监控的文件。
