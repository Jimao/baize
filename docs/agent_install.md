# 客户端安装

## 该部分包含baize系统客户端安装方法


### 安装前须知

```
1. 白泽客户端程序默认安装到/usr/local/baize目录
2. 为保证白泽客户端正常运行/usr/local/baize目录至少10G空间(空间不足可ln -s自行创建软连接)
3. 白泽系统客户端与proxy双向通信需正常，才可以正常工作
4. 安装过程依赖本地yum环境,需要保证可用
5. 安装过程中需要使用pip安装python环境依赖,请确保服务器可以连通公网(或者可以使用代理连通公网pip 代理可以在files/scripts/bash_lib_baize中配置)
```

### 下载客户端

```
cd /tmp
git clone https://github.com/zutianbiao/baize.git
```

### 手工指定proxy

```
vim /tmp/baize/APP/APP_agent/config.py
##################################################################
# 仅修改下面配置指定管理该agent的proxy server即可
#
# PROXY_SERVER = '172.16.211.77:8101'
#
##################################################################
```


### 安装客户端

```
cd /tmp/baize
sh manage.sh install agent
```

### 测试客户端联通性

```
1. 客户端安装完毕3分钟后登录web页面
2. 系统中资产管理部分是否已经可以查找到新的客户端
3. 点击该客户端详情，选择任意远程控制命令执行，观察执行是否正常
```
