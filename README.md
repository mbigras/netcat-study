# Netcat study

> Hack session to learn more about netcat

## Alice and Bob example

```
root@alice:/home/vagrant# while true; do echo hello world | nc -l 8001; done
GET / HTTP/1.1
Host: 192.168.0.2:8001
User-Agent: curl/7.47.0
Accept: */*

GET / HTTP/1.1
Host: 192.168.0.2:8001
User-Agent: curl/7.47.0
Accept: */*
```

```
root@bob:/home/vagrant# nmap 192.168.0.2

Starting Nmap 7.01 ( https://nmap.org ) at 2018-05-25 00:00 UTC
Nmap scan report for 192.168.0.2
Host is up (0.000088s latency).
Not shown: 998 closed ports
PORT     STATE SERVICE
22/tcp   open  ssh
8001/tcp open  vcom-tunnel
MAC Address: 08:00:27:9E:77:69 (Oracle VirtualBox virtual NIC)

Nmap done: 1 IP address (1 host up) scanned in 1.66 seconds
root@bob:/home/vagrant# curl 192.168.0.2:8001
hello world
root@bob:/home/vagrant# curl 192.168.0.2:8001
hello world
```

## Cool commands

```
while true; do echo hello | nc -l 8001; done
while true; do echo hello | nc -vvl 8001; done
tcpdump -A -i lo 'port 8001'
```
