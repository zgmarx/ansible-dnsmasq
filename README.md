ansible-dnsmasq
=========

This role install dnsmasq for CentOS/Ubuntu.

By using this role dnsmasq will listen on 127.0.0.1:53,

It will use 127.0.0.1 as nameserver by setting the first line of /etc/resolv.conf.

Set dns resolve server as you want like the example below.

Usage
-----



```
---
- hosts: localhost

  connection: local

  roles:

    - role: ansible-dnsmasq
      dnsmasq_resolv_dnsmasq_conf: [
        "nameserver 8.8.8.8  # google dns",
        "nameserver 8.8.4.4  # google dns"
      ]
```
