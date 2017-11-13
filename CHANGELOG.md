# Change log

## 0.2.0 (2017-10-30)

* Move to Ansible 2.4
* change default value for `redis_version` to `4.0.2`
* add `redis_download_checksum` role variable. See https://github.com/antirez/redis-hashes
* disable tranparent huge pages. See https://redis.io/topics/latency

## 0.3.0 (2017-11-13)

* Move PID file from `/var/run/redis` to `/var/run`
