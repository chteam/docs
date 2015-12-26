# redis

## CentOS

1. Install wget `yum -y install wget`
2. Download redis `wget http://download.redis.io/releases/redis-stable.tar.gz`
3. `tar zxvf redis-stable.tar.gz`
4. `cd redis-stable`
5. `yum install gcc`
6. `yum install tcl`
7. `make MALLOC=libc`
8. `make test`

### 启动redis
src/redis-server &

### 关闭redis
src/redis-cli shutdown

### 测试
$ src/redis-cli
127.0.0.1:6379> set foo bar
OK
127.0.0.1:6379> get foo
"bar"
$ 

### 建立redis运行目录

mkdir -p redis-server/7000/

### 复制默认的配置文档

cp redis-3.0.0/redis.conf redis-server/redis.default.conf

#把编译好的server复制到运行目录

cp redis-3.0.0/src/redis-server redis-server/7000/
