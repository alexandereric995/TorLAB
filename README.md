# TorLAB
This repository contains the scripts and disk image files of a private network of TOR nodes.

## Private network

The network of TOR nodes are connected to the same local network via one or more routers.

Each node's /etc/hosts are hardcoded with fixed IPs as:
```
127.0.0.1       localhost

192.168.1.130   a
192.168.1.131   b
192.168.1.132   c
192.168.1.133   d
192.168.1.134   e
192.168.1.135   f
192.168.1.136   g  
192.168.1.137   h
192.168.1.138   i
192.168.1.139   j
192.168.1.140   k
192.168.1.141   l
192.168.1.142   m
192.168.1.143   n
192.168.1.144   o
192.168.1.145   p
192.168.1.146   q
192.168.1.147   r
192.168.1.148   s
192.168.1.149   t
192.168.1.149   u
```

Therefore, the respective /etc/hostname in each node has to set accordingly, e.g. "a" for node a, "b" for node b and so on. 

## The Nodes
There are 21 TOR nodes and a Linux machine.<br/>
This Linux machine is connected to the same network router and is used to start and stop all the TOR nodes' services via a shell script.<br/>
The TOR nodes run on Raspberry Pi.<br/>

The logins for the 21 TOR nodes are user: Pi, password: Slowdown<br/>

### Nodes and their Roles
The Roles played by the nodes are:<br/>

Directories Nodes: node a, b, c
Exit Nodes: nodes d, e, f, o, p, h
Proxy Nodes: nodes g, n, u
Relay Nodes: nodes i, j, k, l, m, q, r, s, t

| Roles  | Nodes |
| ------ |:-----:|
| Directories  | a, b, c                   |
| Exit         | d, e, f, o, p, h          |
| Proxy        | g, n, u                   |
| Relay        | i, j, k, l, m, q, r, s, t |


## Image Files
Based on the Roles played by the nodes mentioned above, you can make copies of the 21 SD cards from the provided image files. <br/>
These image files are direct image copies of the Raspberry Pi SD cards from the nodes a, d, g, n, u, and i. <br/>
These image files were created using [win32diskimager](https://sourceforge.net/projects/win32diskimager/). <br/>
You can refer to the [instructions](https://raspberry-projects.com/pi/pi-operating-systems/win32diskimager) provided by win32diskimager.

Each image is compressed to zip files using [Winrar](https://www.win-rar.com/).<br/>
Where the zip file exceeds GitHub LFS limit of 2GB, it is split to multiple z files:<br/>
Node a's SD card image: a_image.zip, a_image.z01, a_image.z02, a_image.z03 <br/>
Node d's SD card image: d_image.zip, d_image.z01, d_image.z02, d_image.z03, d_image,z04 <br/>
Node g's SD card image: g_image.zip, g_image.z01, g_image.z02, g_image.z03 <br/>
Node i's SD card image: i_image.zip, i_image.z01, i_image.z02, i_image.z03 <br/>
Node n's SD card image: n_image.zip <br/>
Node u's SD card image: u_image.zip <br/>







## Linux Machine Shell Script
