# docker-miner

用docker部署挖矿软件

# Features
 - 支持docker灵活部署
 - 支持多款挖矿软件

# 安装安装前准备

- 必须预先安装 [NVIDIA 驱动](https://www.nvidia.cn/Download/index.aspx?lang=cn)
- 安装docker [Get Docker](https://docs.docker.com/get-docker/)
- 安装 [nvidia-docker 2.0](https://github.com/NVIDIA/nvidia-docker)

# 使用

首先pull镜像

```bash
docker run -it levizebulon/ethminer /bin/bash
```

ethminer是一款命令行工具，进入交互式终端之后可以使用

```bash
ethminer --help
```

## 样例

比如gpu卡，[鱼池](https://www.f2pool.com/)账户为linuzb

```
ethminer  -U -P stratum://linuzb.w@eth.f2pool.com:6688
```
