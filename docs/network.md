### Network Operations

```bash
# restart
/etc/init.d/network restart
# stop
/etc/init.d/network stop
```

**Network interface**

```bash
# interface configuration
ifconfig
ifconfig eth0

# enable or disable specific interface
ifup eth0
ifdown eth0
```

**netstat**

Print network connections, routings tables, interface statistics, masquerade connections, and multicast memberships

```bash
# show listening sockets
netstat -l -pn -tu
# show all sockets
netstat -a -pn -t

  -a --all       display all sockets
  -l --listening display listening server sockets

  -n --numeric   don't resolve names
  -p --programs  display PID/Program name for sockets

  -t --tcp       tcp
  -u --udp       udp
```

**lsof**

```bash
lsof -i :22

COMMAND  PID USER   FD   TYPE DEVICE SIZE/OFF NODE NAME
sshd    1471 root    3u  IPv4  16316      0t0  TCP *:ssh (LISTEN)
sshd    1471 root    4u  IPv6  16318      0t0  TCP *:ssh (LISTEN)
```

**From A to B**

```bash
# send ICMP ECHO_REQUEST to network hosts
ping 8.8.8.8
ping -c 5 google.com

# print the route package tract to network host
traceroute 4.2.2.2

# show / manipulate the IP routing table
route
```

**DNS**

```bash
# DNS lookup utility
dig google.com

# query Internet name servers interactively
nslookup google.com

# show or set the system's hostname
hostname
hostnamectl status

# change hostname
hostnamectl set-hostname <hostname>
```

*wget, curl*


**Firewall**

```bash
# ubuntu
sudo ufw disable
sudo ufw enable

# centos 7
systemctl status firewalld
systemctl stop firewalld
systemctl start firewalld
systemctl restart firewalld

systemctl status iptables
systemctl stop iptables
systemctl start iptables
systemctl restart iptables
```

**iptables** [^4]
Administration tool for IPv4 package filtering and NAT

```bash
# List rules
iptables -L -v
iptables -L -t nat -n

# Change policy
iptables --policy INPUT ACCEPT

# Blocking
# block all connections from an IP address
iptables -A INPUT -s 10.10.10.10 -j DROP
# block all of the IP addresses in the 10.10.10.0/24 network range
iptables -A INPUT -s 10.10.10.0/24 -j DROP
# block SSH connections from 10.10.10.10
iptables -A INPUT -p tcp --dport ssh -s 10.10.10.10 -j DROP


# Save changes
# ubuntu
sudo /sbin/iptables-save
# redhat/centos
/sbin/service iptables save

# clear all the currently configured rules
iptables -F

# options
  -L --list [chain]   List all rules in a chain or all chains
  -F --flush          Delete rules
  -v --verbose        verbose mode
  -P --policy         Change policy on chain to target
  -n --numeric        numeric output of addresses and ports
  -t --table          table to manipulate (default: filter)
```

**firewalld**

```bash
# Dynamic Firewall Manager
firewalld
```

**SSH**

[How To Set Up SSH Keys](https://www.digitalocean.com/community/tutorials/how-to-set-up-ssh-keys--2)

```bash
# secure copy
scp [[user@]host1:]file1 [[user@]host2:]file2
```
