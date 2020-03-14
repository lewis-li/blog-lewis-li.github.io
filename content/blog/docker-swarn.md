+++
Title = "Docker Swarm使用"
Date = 2019-12-09T21:33:26+08:00
Categories = ["program"]
# Keywords
Tags = ["docker", "docker swarm"]
Description = "Docker Swarm使用"
Draft = true
+++

## Docker Stack

### 定义
在单文件定义多服务应用，部署并管理完整生命周期（初始化部署 -> 健康检查 -> 扩容 -> 更新 -> 回滚）。

stack配置文件：就是compose配置文件
Stack 不支持构建

包括：
- 网络
- 密钥
- 服务


```
docker stack deploy portainer --prune --compose-file portainer-agent-stack.yml
```

```
docker stack ls
```