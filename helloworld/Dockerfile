# java 环境
FROM coding-public-docker.pkg.coding.net/public/docker/openjdk:8

# 定义工作目录
WORKDIR /app
# 把项目中的所有东西复制到工作目录(app)下面
COPY . .
# 把打包好的文件 赋值到app下面 方便操作
ADD target/*.jar /app/helloworld-0.0.1-SNAPSHOT.jar
# 改变容器的时区
RUN ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime
RUN echo 'Asia/Shanghai' >/etc/timezone
#端口号
EXPOSE 8090
ENTRYPOINT ["java","-jar","/app/helloworld-0.0.1-SNAPSHOT.jar"]






