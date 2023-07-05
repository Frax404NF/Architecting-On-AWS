### Membuat VPC A dan B, Subnet untuk setiap VPC, mengonfigurasi security group dan route table, memasang internet gateway, membuat koneksi dengan VPC Peering, dan mengujinya langsung dengan melakukan SSH dan Ping.


## Hasil CMD :

Microsoft Windows [Version 10.0.22621.1848]
(c) Microsoft Corporation. All rights reserved.

C:\Users\acer\Downloads>ssh -i "dicoding-demo.pem" ec2-user@13.229.109.242

       __|  __|_  )
       _|  (     /   Amazon Linux 2 AMI
      ___|\___|___|

https://aws.amazon.com/amazon-linux-2/


[ec2-user@ip-10-100-0-234 ~]$ ssh ec2-user@10.100.1.119
The authenticity of host '10.100.1.119 (10.100.1.119)' can't be established.ECDSA key fingerprint is SHA256:yjsEJDk/TdGmQKkAEIAPGUR3bOQoGRJ+CStbhVJ2y2A.ECDSA key fingerprint is MD5:61:d3:67:18:d6:d3:45:ba:8c:73:ea:e9:d1:1a:34:88.
Are you sure you want to continue connecting (yes/no)? yes
Warning: Permanently added '10.100.1.119' (ECDSA) to the list of known hosts.
Permission denied (publickey,gssapi-keyex,gssapi-with-mic).


[ec2-user@ip-10-100-0-234 ~]$ nano dicoding-demo.pem

[ec2-user@ip-10-100-0-234 ~]$ chmod 400 dicoding-demo.pem

[ec2-user@ip-10-100-0-234 ~]$ ssh -i dicoding-demo.pem ec2-user@10.100.1.119
       __|  __|_  )
       _|  (     /   Amazon Linux 2 AMI
      ___|\___|___|

https://aws.amazon.com/amazon-linux-2/

[ec2-user@ip-10-100-1-119 ~]$ ssh ec2-user@10.200.1.23
^C

[ec2-user@ip-10-100-1-119 ~]$ ping 10.200.1.23
PING 10.200.1.23 (10.200.1.23) 56(84) bytes of data.
^C
--- 10.200.1.23 ping statistics ---
12 packets transmitted, 0 received, 100% packet loss, time 11245ms

[ec2-user@ip-10-100-1-119 ~]$ ping 10.200.1.23
PING 10.200.1.23 (10.200.1.23) 56(84) bytes of data.
64 bytes from 10.200.1.23: icmp_seq=1 ttl=255 time=1.48 ms
64 bytes from 10.200.1.23: icmp_seq=2 ttl=255 time=1.08 ms
64 bytes from 10.200.1.23: icmp_seq=3 ttl=255 time=1.03 ms
64 bytes from 10.200.1.23: icmp_seq=4 ttl=255 time=1.08 ms
64 bytes from 10.200.1.23: icmp_seq=5 ttl=255 time=3.36 ms
64 bytes from 10.200.1.23: icmp_seq=6 ttl=255 time=1.09 ms
^C
--- 10.200.1.23 ping statistics ---
6 packets transmitted, 6 received, 0% packet loss, time 5006ms
rtt min/avg/max/mdev = 1.035/1.524/3.364/0.836 ms

[ec2-user@ip-10-100-1-119 ~]$ ssh ec2-user@10.200.1.23
The authenticity of host '10.200.1.23 (10.200.1.23)' can't be established.
ECDSA key fingerprint is SHA256:DAPHMjMt/Co6TDEAML84jjlj264tdPdeaSEClXRjVZA.ECDSA key fingerprint is MD5:b4:8d:6c:78:98:aa:25:f3:f1:c5:14:da:ed:01:1a:00.
Are you sure you want to continue connecting (yes/no)? yes
Warning: Permanently added '10.200.1.23' (ECDSA) to the list of known hosts.Permission denied (publickey,gssapi-keyex,gssapi-with-mic).

[ec2-user@ip-10-100-1-119 ~]$ nano dicoding-demo.pem

[ec2-user@ip-10-100-1-119 ~]$ chmod 400 dicoding-demo.pem

[ec2-user@ip-10-100-1-119 ~]$ ssh -i dicoding-demo.pem ec2-user@10.200.1.23

       __|  __|_  )
       _|  (     /   Amazon Linux 2 AMI
      ___|\___|___|

https://aws.amazon.com/amazon-linux-2/

[ec2-user@ip-10-200-1-23 ~]$ ping 10.200.1.23
PING 10.200.1.23 (10.200.1.23) 56(84) bytes of data.
64 bytes from 10.200.1.23: icmp_seq=1 ttl=255 time=0.023 ms
64 bytes from 10.200.1.23: icmp_seq=2 ttl=255 time=0.025 ms
64 bytes from 10.200.1.23: icmp_seq=3 ttl=255 time=0.030 ms
64 bytes from 10.200.1.23: icmp_seq=4 ttl=255 time=0.030 ms
64 bytes from 10.200.1.23: icmp_seq=5 ttl=255 time=0.030 ms
^C
--- 10.200.1.23 ping statistics ---
5 packets transmitted, 5 received, 0% packet loss, time 4085ms
rtt min/avg/max/mdev = 0.023/0.027/0.030/0.006 ms

[ec2-user@ip-10-200-1-23 ~]$ ping 10.100.1.119
PING 10.100.1.119 (10.100.1.119) 56(84) bytes of data.
^C
--- 10.100.1.119 ping statistics ---
10 packets transmitted, 0 received, 100% packet loss, time 9195ms

[ec2-user@ip-10-200-1-23 ~]$ ping 10.100.1.119
PING 10.100.1.119 (10.100.1.119) 56(84) bytes of data.
64 bytes from 10.100.1.119: icmp_seq=1 ttl=255 time=1.01 ms
64 bytes from 10.100.1.119: icmp_seq=2 ttl=255 time=1.03 ms
64 bytes from 10.100.1.119: icmp_seq=3 ttl=255 time=1.04 ms
64 bytes from 10.100.1.119: icmp_seq=4 ttl=255 time=1.14 ms
64 bytes from 10.100.1.119: icmp_seq=5 ttl=255 time=1.02 ms
64 bytes from 10.100.1.119: icmp_seq=6 ttl=255 time=1.10 ms
64 bytes from 10.100.1.119: icmp_seq=7 ttl=255 time=1.08 ms
^C
--- 10.100.1.119 ping statistics ---
7 packets transmitted, 7 received, 0% packet loss, time 6007ms
rtt min/avg/max/mdev = 1.012/1.064/1.142/0.051 ms