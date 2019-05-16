### 以busybox制作镜像镜像
- docker run busybox ls
mkdir -p /data/html
vi /data/html/index.html
<h1>Busybox httpd server</h1>

- 不用退出该容器（可以再开一个终端登录）
- docker image ls
- 打标签: docker tag IMAGEID pantsli/busybox:v0.2
- 删除标签：docker image rm TAGNAME
- ps: 标签名组成必须为：USERNAME/TAG

- 在docker hub上创建一个仓库：busybox
- 登录docker hub:docker login -u pantsli -p panlt827
- docker push pantsli/busybox

- docker save
docker save -o shareimages.gz ts/busybox:v0.1 pantsli/busybox:v0.2
- docker load 
docker load -i shareimages.gz




docker exec -it simpleweb sh

docker run --rm -p 3000:3000 -v /app/node_modules -v $(pwd):/app IMAGEID






