# Jarkom_Modul4_Lapres_D14

Menentukan jumlah subnet yang ada dalam topologi menggunakan metode VLSM
<img src="https://github.com/hrswcksono/Jarkom_Modul4_Lapres_D14/blob/main/img/VLSM.png" >

Jumlah IP pada tiap-tiap subnet
<img src="https://github.com/hrswcksono/Jarkom_Modul4_Lapres_D14/blob/main/img/VLSMIP.png" >


Pembagian IP dalam pohon seperti gambar dengan NID 192.168.0.0 dengan netmask /19
<img src="https://github.com/hrswcksono/Jarkom_Modul4_Lapres_D14/blob/main/img/VLSMtree.jpg" >

Penyetingan Routing pada Cisco Packet Tracer
```
SURABAYA
192.168.0.12/30 mask 255.255.255.252 via 192.168.0.10
192.168.12.0/22 mask 255.255.252.0 via 192.168.0.10
192.168.16.0/21 mask 255.255.248.0 via 192.168.0.10
192.168.0.128/25 mask 255.255.255.128 via 192.168.0.10
192.168.0.0/30 mask 255.255.255.252 via 192.168.0.6
192.168.2.0/23 mask 255.255.254.0 via 192.168.0.6
192.168.0.16/28 mask 255.255.255.248 via 192.168.0.6
192.168.8.0/22 mask 255.255.252.0 via 192.168.0.6
10.151.79.125/30 mask 255.255.255.248 via 192.168.0.6
192.168.1.0/24 mask 255.255.255.0 via 192.168.0.6
192.168.4.0/22 mask 255.255.252.0 via 192.168.0.6
```
```
BATU
0.0.0.0/0 mask 0.0.0.0 via 192.168.0.5
192.168.0.16/28 mask 255.255.255.248 via 192.168.2.2
10.151.79.124/30 mask 255.255.255.248 via 192.168.0.2
192.168.1.0/24 mask 255.255.255.0 via 192.168.0.2
192.168.4.0/22 mask 255.255.252.0 via 192.168.0.2
```
```
KEDIRI
0.0.0.0/0 mask 0.0.0.0 via 192.168.0.1
192.168.4.0/22 mask 255.255.252.0 via 192.168.1.2
```
```
MADIUN
0.0.0.0/0 mask 0.0.0.0 via 192.168.2.1
```
```
BLITAR
0.0.0.0/0 mask 0.0.0.0 via 192.168.1.1
```
```
PASURUAN
0.0.0.0/0 mask 0.0.0.0 via 192.168.0.9
192.168.16.0/21 mask 255.255.248.0 via 192.168.0.14
192.168.0.128/25 mask 255.255.255.128 via 192.168.0.14
```
```
PROBOLINGGO
0.0.0.0/0 mask 0.0.0.0 via 192.168.0.13
```
