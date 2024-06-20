# Router stuff

## FHRP

```
HQ-RTR1(config)# interface vlan 10
HQ-RTR1(config)glbp 10 ip ????192.168.99.254
HQ-RTR1(config)glbp 10 priority 150
HQ-RTR1(config)glbp 10 preempt
HQ-RTR1(config)glbp 10 authentication md5 key-string Pa$$worD
```

## Auto priv exec mode

```
line console 0
login local
autocommand enable
```

## Portfast BPDU Guard

```
spanning-tree portfast bpdu
```
