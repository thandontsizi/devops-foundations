# Networking Verification:
This file documents the actual outputs and results from running networking commands.

1. IP Address:
- Command: ip addr
- Output: 
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.-.-.-/8 scope host lo
       valid_lft forever preferred_lft forever
    inet 10.255.255.-/32 brd 10.255.255.- scope global lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host
       valid_lft forever preferred_lft forever
2: eth0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc mq state UP group default qlen 1000
    link/ether 00:15:5d:b5:df:d5 brd ff:ff:ff:ff:ff:ff
    inet 172.-.-.-/20 brd 172.-.-.255 scope global eth0
       valid_lft forever preferred_lft forever
    inet6 fe80::215:5dff:feb5:dfd5/64 scope link
       valid_lft forever preferred_lft forever

2. Routing Table:
- Command: ip route
- Output: 
default via 172.-.64.1 dev eth0 proto kernel
172.-.64.0/20 dev eth0 proto kernel scope link src 172.20.-.61

3. Connectivity Test:
- Command: ping -c 4 8.8.8.8
- Output: 
--- 8.8.8.8 ping statistics ---
4 packets transmitted, 4 received, 0% packet loss, time 2999ms
rtt min/avg/max/mdev = 47.221/56.200/67.094/7.100 ms

4. Listening Ports:
- Command: ss or ss -tuln
- Output: 

5. Application Connectivity:
- Command: curl https://github.com
- Output: 
