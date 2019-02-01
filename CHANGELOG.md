# Change log

## 0.2.0 (2017-10-30)

* Move to Ansible 2.4
* change default value for `redis_version` to `4.0.2`
* add `redis_download_checksum` role variable. See https://github.com/antirez/redis-hashes
* disable tranparent huge pages. See https://redis.io/topics/latency

## 0.3.0 (2017-11-13)

* Move PID file from `/var/run/redis` to `/var/run`

## 0.4.0 (2017-11-13)

* Rollback to previous setup for PID file
* Add `ExecStartPre` directive to create `/var/run/redis` and set ownership.

## 0.5.0 (2017-11-13)

* Absolute path to `mkdir` and `chown`

## 0.6.0 (2017-11-13)

* Use two `ExecStartPre` directive instances to execute `mkdir` and `chown`

## 0.7.0 (2019-02-01)

* Do not default redis_maxmemory_percentage to 70
* add `LimitNOFILE` to systemd script
