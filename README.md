# ansible-role-rclone [![Build Status](https://travis-ci.org/shengyou/ansible-role-rclone.svg?branch=master)](https://travis-ci.org/shengyou/ansible-role-rclone)
=========

安裝 [rclone](https://rclone.org/)。

適用於 Ubuntu 與 CentOS

Requirements
------------

* ansible >= 2.4
* python >= 2.6

Role Variables
--------------

```
rclone_version: (default: 1.41)
rclone_os:      (default: "linux-amd64")
rclone_update:  (default: false)
# 如欲強制更新或重新安裝 rclone 則設置 rclone_update: true
```

rclone_os 可用的選項如下
* linux-386, linux-amd64, linux-arm, linux-arm64, linux-mips, linux-mipsle


Dependencies
------------

none.

Example Playbook
----------------

```
- hosts: your_host
  gather_facts: yes
  become: yes

  vars:
    rclone_version: 1.41
    rclone_os: "linux-amd64"

  roles:
    - ansible-role-rclone
```

License
-------

MIT
