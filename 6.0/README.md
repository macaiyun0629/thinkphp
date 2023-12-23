## 安装ThinkPHP

### 启动composer
```bash
sudo docker-compose -f docker-compose-composer.yml up
```
### 进入composer容器
```bash
sudo docker exec -it 60-composer-1 bash
```
### 安装ThinkPHP 6.0.x
```bash
composer create-project topthink/think tp 6.0.*
```

## 制作ThinkPHP镜像

```bash
sudo DOCKER_BUILDKIT=1 docker build . -f ./Dockerfile -t registry.cn-hangzhou.aliyuncs.com/macaiyun0629/thinkphp --no-cache 
```