只是将from 改为nvidia/cuda:9.0-cudnn7-runtime

# 使用方法：
```
docker build ./ -t $IMAGE_NAME
docker run -it --runtime=nvidia --name flashback -e GEOMETRY=1366x768 -p 5901:5901 $IMAGE_NAME
```
需要加上`--runtime=nvidia`才能在docker进程里访问宿主机显卡
