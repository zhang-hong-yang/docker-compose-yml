# docker-compose-yml

Docker Compose 配置文件集合，包含常用服务的配置。

## 服务列表

- **MySQL** - MySQL 8.0 数据库
- **PostgreSQL** - PostgreSQL
- **Redis** - Redis 7 缓存数据库
- **Portainer** - Docker 容器管理界面

## 启动命令

### MySQL

```bash
cd mysql
docker-compose up -d
```

- 端口：`3306`
- 默认 root 密码：`rootpassword`
- 默认数据库：`mydb`
- 默认用户：`user` / 密码：`password`

### PostgreSQL

```bash
cd postgresql
docker-compose up -d
```

- 端口：`5432`
- 默认用户：`postgres` / 密码：`postgres`
- 默认数据库：`mydb`

### Redis

```bash
cd redis
docker-compose up -d
```

- 端口：`6379`
- 已启用 AOF 持久化

### Portainer

```bash
cd portainer
docker-compose up -d
```

- 端口：`9000`
- 访问地址：http://localhost:9000

## 常用命令

### 启动服务
```bash
docker-compose up -d
```

### 停止服务
```bash
docker-compose down
```

### 查看日志
```bash
docker-compose logs -f
```

### 查看运行状态
```bash
docker-compose ps
```

### 重启服务
```bash
docker-compose restart
```

## 注意事项

1. 所有服务的数据都持久化到各自的 `./data` 目录
2. 请根据实际需求修改环境变量中的密码和数据库名称
3. 确保端口未被占用，否则需要修改 `ports` 配置