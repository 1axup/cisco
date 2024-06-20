# VPN Configurations

```
crypto ikev2 keyring <keyr_name>
 peer <peer_name>
  address [other's_public_ip]
  hostname [peer's_hostname]
  identity address [other's_public_ip]
  pre-shared-key local <pass phrase>

crypto ikev2 profile <prof_name>
 match address local [own_ip_address]
 match identity remote address [peer's_public_ip]
 identity local address [own_public_ip]
 authentication remote pre-share key <passphrase>
 authentication local pre-share key <passphrase>
 lifetime 3600

crypto ipsec transform-set <tfs-name> esp-gcm 256
 mode tunnel

crypto ipsec profile <ipsec_prof_name>
 set transform-set <tfs-name>
 set ikev2-profile <prof_name>

interface Tunnel 1
 tunnel source [my_ip_for_tunnel_ipsec]
 tunnel destination [other_side_ip_ipsec]
 ip address 10.0.0.1
 tunnel protection ipsec profile <ipsec_prof_name>
``` 
