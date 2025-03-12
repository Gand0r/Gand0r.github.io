---
permalink: /catatanku/
title: "Catatanku"
---

* * *

> Mungkin semua orang bisa copy dan paste, tapi tidak semua orang bisa menganalisa.


* * *

<details><summary>Cara Mengganti Dns dengan menggunakan wmic via command line</summary><br>
   <li><data value="1">wmic nicconfig where (IPEnabled=TRUE) call SetDNSServerSearchOrder ()</data></li>
   <li><data value="2">wmic nicconfig where (IPEnabled=TRUE) call SetDNSServerSearchOrder ("8.8.8.8", "8.8.4.4")</data></li>
</details>

* * *

<details><summary>Install Nodejs dari Binary di Ubuntu 20.04</summary><br>
   Node 18.x
   <li>curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash - </li>
   <li>sudo apt-get install -y nodejs </li>
   <br>
   Node 17.x
   <li>curl -fsSL https://deb.nodesource.com/setup_17.x | sudo -E bash - </li>
   <li>sudo apt-get install -y nodejs </li>
   <br>
   Node 16.x
   <li>curl -fsSL https://deb.nodesource.com/setup_16.x | sudo -E bash - </li>
   <li>sudo apt-get install -y nodejs </li>
   <br>
   versi LTS
   <li>curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo -E bash - </li>
   <li>sudo apt-get install -y nodejs </li>
   <br>
   versi Terbaru
   <li>curl -fsSL https://deb.nodesource.com/setup_current.x | sudo -E bash - </li>
   <li>sudo apt-get install -y nodejs </li>
</details>

* * *

<details><summary>Setting IP pada Ubuntu Server 22.04</summary><br>
   <li>ip link</li>
   <li>cd /etc/netplan</li>
   <li>sudo nano /etc/netplan/installer-config.yaml</li>
   <li>edit file yaml seperti contoh di bawah ini, untuk addresss dan gateway sesuaikan dengan jaringan anda</li>
   
   ```
   network:
   version: 2
   renderer: networkd
   ethernets:
    enp5s0:
       dhcp4: no
       addresses:
         - "172.11.11.15/24"
       gateway4: "192.168.75.254"
       nameservers:
           addresses: [1.1.1.1,8.8.8.8]
   ```
   
   <li>sudo netplan apply</li>
   <li>selesai, setelah itu cek ping ke gateway atau ip Lokal</li>
</details>

* * *

<a href='https://ko-fi.com/M4M3AGKQC' target='_blank'><img height='36' style='border:0px;height:36px;' src='https://cdn.ko-fi.com/cdn/kofi1.png?v=3' border='0' alt='Buy Me a Coffee at ko-fi.com' /></a>
