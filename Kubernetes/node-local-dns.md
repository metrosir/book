## ip-100-66-35-217.ec2.internal

[ERROR] plugin/errors: 2 4284805962838622348.4964286968892133078.ip6.arpa. HINFO: dial tcp 172.20.245.160:53: i/o timeout
[INFO] Added back nodelocaldns rule - {raw PREROUTING [-p tcp -d 169.254.20.10 --dport 53 -j NOTRACK]}
[INFO] Added back nodelocaldns rule - {raw PREROUTING [-p udp -d 169.254.20.10 --dport 53 -j NOTRACK]}
[INFO] Added back nodelocaldns rule - {filter INPUT [-p tcp -d 169.254.20.10 --dport 53 -j ACCEPT]}
[INFO] Added back nodelocaldns rule - {filter INPUT [-p udp -d 169.254.20.10 --dport 53 -j ACCEPT]}
[INFO] Added back nodelocaldns rule - {raw OUTPUT [-p tcp -s 169.254.20.10 --sport 53 -j NOTRACK]}
[INFO] Added back nodelocaldns rule - {raw OUTPUT [-p udp -s 169.254.20.10 --sport 53 -j NOTRACK]}


## 