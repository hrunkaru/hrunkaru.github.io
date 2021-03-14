# Basics
- Read from pcap file
```
tshark -r example.pcap
```

- Permanently add colored output to shark
```
echo -e "alias tshark='tshark --color'" >> ~/.bashrc
source ~/.bashrc
```

# Filtering output 

| direction | eth | ip | tcp | udp |
|---|---|---|---|---|
| source | src | src | srcport | srcport |
| destination | dst | dst | dstport | dstport |
| either | addr | addr | port | port |

Source MAC address is 00:11:22:33:44:55
```
eth.src == 00:11:22:33:44:55
```

Find all traffic that has IP of 10.0.0.1
```
ip.addr == 10.0.0.1
```

Destination tcp port is NOT 80
```
tcp.dstport != 80
```

Add protocol filter
```
ip.addr == 8.8.8.8 and !(icmp or dns)
```


## Links
- https://tshark.dev/packetcraft/add_context/tshark_colorized/
- https://tshark.dev/analyze/packet_hunting/packet_hunting/ 
- https://tshark.dev/analyze/ 