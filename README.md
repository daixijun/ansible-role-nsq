# nsq

[![Build Status](https://travis-ci.com/daixijun/ansible-role-nsq.svg?branch=master)](https://travis-ci.com/daixijun/ansible-role-nsq)
[![Ansible Galaxy](https://img.shields.io/badge/galaxy-daixijun.mysql-660198.svg?style=flat)](https://galaxy.ansible.com/daixijun/mysql/)
[![GitHub tag (latest SemVer)](https://img.shields.io/github/v/tag/daixijun/ansible-role-mysql?sort=semver)](https://github.com/daixijun/ansible-role-mysql/tags)

部署 nsq 集群

## 环境要求

- CentOS 7.x/8.x
- Ansible 2.9+
- nsq v1.2+

## 变量

- `nsq_version`: 版本号，默认 1.2.0
- `nsq_download_url`: 二进制包下载地址
- `nsqadmin_log_level`: admin 日志等级, 默认 info
- `nsqadmin_http_address`: admin 监听地址, 黑夜 0.0.0.0:4171
- `nsqadmin_nsqlookupd_http_addresses`: nslookupd 地址，类型为list, 可以有多个
- `nsqadmin_nsqd_http_addresses`: nsqd 地址，类型为list, 可以有多个
- `nsqlookupd_log_level`: nsqlookupd 日志等级，默认 info
- `nsqlookupd_tcp_address`: nsqlookupd TCP 监听地址, 默认 0.0.0.0:4160
- `nsqlookupd_http_address`: nsqlookupd HTTP 监听地址, 默认 0.0.0.0:4161
- `nsqd_log_level`: nsqd 日志等级，默认 info
- `nsqd_data_path`: diskqueue数据存放目录，默认 /data/nsq
- `nsqd_tcp_address`: nsqd TCP 监听地址, 默认 0.0.0.0:4150
- `nsqd_http_address`: nsqd HTTP 监听地址， 默认 0.0.0.0:4151
- `nsqd_https_address`: nsqd HTTPS 监听地址， 默认 0.0.0.0:4152 (暂时不支持)
- `nsqd_nsqlookupd_tcp_addresses`: nsqlookupd 地址，类型为list, 可以有多个
- `nsqd_mem_queue_size`: 每个 topic/channel 在内存中存放的消息数量

## 依赖

无

## 示例

参考 [molecule](./molecule/default/converge.yml)

## License

BSD

## 维护者

- Xijun Dai <daixijun1990@gmail.com>
