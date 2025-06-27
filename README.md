# remote-serial
Simple server and client scripts to route a Serial port through LAN. Needed a simple, free script to have a remote workstation accessing the COM ports from an on-field laptop.
Works for me with a VPN.

Server usage example:

```
remote-serial-server --serial-port COM4 --baud-rate 115200 --data-bits 8 --parity None --stop_bits One --tcp-port 12345
```
Or keep it simple with some common parameters (default to baud = 115200, data bits = 8, parity = None, stop bits = One):
```
remote-serial-server --serial-port COM4 --tcp-port 12345
```

Client usage example:
```
remote-serial-client --serial-port COM5 --baud-rate 115200 --data-bits 8 --parity None --stop_bits One --remote-ip 192.168.2.15 --remote-port 12345
```
Or keep it simple with the same common parameters from server:
```
remote-serial-client --serial-port COM5 --remote-ip 192.168.2.15 --remote-port 12345
```
