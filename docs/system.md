# System Information

## OS

```bash
> uname -r
2.6.32-504.3.3.el6.x86_64

> cat /etc/os-release
NAME="Ubuntu"
VERSION="14.04.4 LTS, Trusty Tahr"
ID=ubuntu
ID_LIKE=debian
PRETTY_NAME="Ubuntu 14.04.4 LTS"
VERSION_ID="14.04"
HOME_URL="http://www.ubuntu.com/"
SUPPORT_URL="http://help.ubuntu.com/"
BUG_REPORT_URL="http://bugs.launchpad.net/ubuntu/"

> cat /etc/redhat-release
CentOS release 7 (Final)
```

## RAM

```bash
> free -g

             total       used       free     shared    buffers     cached
Mem:         64394       1407      62987          4         49        359
-/+ buffers/cache:        997      63397
Swap:       102399          0     102399
```

## CPU

```bash
> lscpu

Architecture:          x86_64
CPU op-mode(s):        32-bit, 64-bit
Byte Order:            Little Endian
CPU(s):                12
On-line CPU(s) list:   0-11
Thread(s) per core:    2
Core(s) per socket:    6
Socket(s):             1
NUMA node(s):          1
Vendor ID:             GenuineIntel
CPU family:            6
Model:                 62
Stepping:              4
CPU MHz:               1200.000
BogoMIPS:              5199.93
Virtualization:        VT-x
L1d cache:             32K
L1i cache:             32K
L2 cache:              256K
L3 cache:              15360K
NUMA node0 CPU(s):     0-11
```

## Hardisk

```bash
> df -h

Filesystem      Size  Used Avail Use% Mounted on
/dev/sda1       197G  143G   44G  77% /
tmpfs            32G   80K   32G   1% /dev/shm
/dev/sda3       2.4T   17G  2.3T   1% /grid/0
/dev/sdb1       2.7T   66G  2.5T   3% /grid/1
/dev/sdc1       2.7T   68G  2.5T   3% /grid/2
/dev/sdd1       2.7T   66G  2.5T   3% /grid/3
```

<small>similar: fdisk, sfdisk, cfdisk, parted, df, pydf, lsblk, blkid, hwinfo</small> <sup id="fnref-1217-1"><a href="#fn-1217-1" rel="footnote">2</a></sup>