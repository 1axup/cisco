# ASA Configuration

## Set IP Address

```
interface e0
 ip address 12.12.12.1
 no shutdown
 nameif LOREM
 security level 100
```

## Set Hostname

```
hostname DEFAULT
```

## Set enable secret

```
enable password LoremIpsum
```

## Local authentication

```
username admin password Pa$$worD
aaa authentication serial console LOCAL
```

## Routing

same as csr1000v
