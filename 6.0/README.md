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

## 启动容器

### docker直接启动

```bash
sudo docker run -d --name thinkphp -p 80:80 registry.cn-hangzhou.aliyuncs.com/macaiyun0629/thinkphp
```

## 访问容器

```bash
curl http://localhost
```

## 停止容器

```bash
sudo docker stop thinkphp
```

### docker-compose 启动

```bash
sudo docker-compose -f docker-compose.yml up -d
```