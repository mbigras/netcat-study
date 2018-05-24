# Netcat study

> Hack session to learn more about netcat

## Cool commands

```
while true; do echo hello | nc -l 8001; done
while true; do echo hello | nc -vvl 8001; done
tcpdump -A -i lo 'port 8001'
```
