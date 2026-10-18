# 黑马点评

项目包含 Spring Boot 后端与前端静态页面及 Nginx 配置。

- `backend/`：后端源码，数据库初始化脚本位于 `backend/src/main/resources/db/hmdp.sql`。
- `frontend/html/hmdp/`：前端页面和静态资源。
- `frontend/conf/nginx.conf`：Nginx 配置。

## 本地配置

首次拉取后，复制后端配置示例：

```sh
cp backend/src/main/resources/application-example.yaml backend/src/main/resources/application.yaml
```

根据本机环境调整数据库和 Redis 连接信息，通过环境变量 `DB_PASSWORD` 设置数据库密码。Redis 需要密码时，取消配置文件中对应密码项的注释，并设置 `REDIS_PASSWORD` 环境变量。

本机 `application.yaml`、日志、缓存和 IDE 文件已被 Git 忽略，避免将密码及运行产物提交到仓库。
