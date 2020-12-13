# Jarkom_Modul4_Lapres_D14
 
### KELOMPOK        : D14
ANGGOTA         :

* Muhammad Haris W.     (05111840000029)
* Vieri Fath Ayuba      (05111840000153)


## Soal
<img src="https://github.com/hrswcksono/Jarkom_Modul4_Lapres_D14/blob/main/img/Soal.png" >
Kerjakan pada Cisco Packet Tracer dan UML menggunakan metode
perhitungan CLASSLESS yang berbeda.

Keterangan: Bila di CPT menggunakan VLSM, maka di UML menggunakan CIDR
atau Sebaliknya

## Menggunakan Cisco Packet Tracer
Menentukan jumlah subnet yang ada dalam topologi menggunakan metode VLSM
<img src="https://github.com/hrswcksono/Jarkom_Modul4_Lapres_D14/blob/main/img/VLSM.png" >

Jumlah IP pada tiap-tiap subnet yang ada pada topologi
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



## CIDR (Classless Inter Domain Routing) - UML


- Pertama, tentukan subnet yang ada dalam topologi dan lakukan labelling netmask terhadap masing-masing subnet


<img src="https://github.com/hrswcksono/Jarkom_Modul4_Lapres_D14/blob/main/image/1.JPG" >



- Kedua, gabungkan subnet paling bawah di dalam topologi yang mana paling jauh dari cloud. Subnet yang digabung tersebut akan membentuk sebuah subnet lebih besar dari subnet-subnet kecil yang ada di dalamnya. Lalu ulangi langkah tersebut sampai menjadi sebuah subnet besar yang mencakup 1 topologi yang kita miliki.


<img src="https://github.com/hrswcksono/Jarkom_Modul4_Lapres_D14/blob/main/image/2.JPG" >
<img src="https://github.com/hrswcksono/Jarkom_Modul4_Lapres_D14/blob/main/image/3.JPG" >
<img src="https://github.com/hrswcksono/Jarkom_Modul4_Lapres_D14/blob/main/image/4.JPG" >
<img src="https://github.com/hrswcksono/Jarkom_Modul4_Lapres_D14/blob/main/image/5.JPG" >
<img src="https://github.com/hrswcksono/Jarkom_Modul4_Lapres_D14/blob/main/image/6.JPG" >
<img src="https://github.com/hrswcksono/Jarkom_Modul4_Lapres_D14/blob/main/image/7.JPG" >
<img src="https://github.com/hrswcksono/Jarkom_Modul4_Lapres_D14/blob/main/image/8.JPG" >



- Ketiga, hitung pembagian IP dengan pohon berdasarkan penggabungan subnet yang telah dilakukan.

<img src="https://github.com/hrswcksono/Jarkom_Modul4_Lapres_D14/blob/main/image/tree.JPG" >



### Konfigurasi topologi.sh


```
# Switch
uml_switch -unix switch1 > /dev/null < /dev/null &
uml_switch -unix switch2 > /dev/null < /dev/null &
uml_switch -unix switch3 > /dev/null < /dev/null &
uml_switch -unix switch4 > /dev/null < /dev/null &
uml_switch -unix switch5 > /dev/null < /dev/null &
uml_switch -unix switch13 > /dev/null < /dev/null &
uml_switch -unix switch15 > /dev/null < /dev/null &
uml_switch -unix switch16 > /dev/null < /dev/null &
uml_switch -unix switch17 > /dev/null < /dev/null &
uml_switch -unix switch18 > /dev/null < /dev/null &
uml_switch -unix switch19 > /dev/null < /dev/null &
uml_switch -unix switch20 > /dev/null < /dev/null &
uml_switch -unix switch21 > /dev/null < /dev/null &
uml_switch -unix switch22 > /dev/null < /dev/null &
uml_switch -unix switch25 > /dev/null < /dev/null &

# Router
xterm -T SURABAYA -e linux ubd0=SURABAYA,jarkom umid=SURABAYA eth0=tuntap,,,10.151.78.61 eth1=daemon,,,switch1 eth2=daemon,,,switch2 eth3=daemon,,,switch4 eth4=daemon,,,switch13 mem=64M &
xterm -T PASURUAN -e linux ubd0=PASURUAN,jarkom umid=PASURUAN eth0=daemon,,,switch2 eth1=daemon,,,switch3 eth2=daemon,,,switch19 mem=64M &
xterm -T PROBOLINGGO -e linux ubd0=PROBOLINGGO,jarkom umid=PROBOLINGGO eth0=daemon,,,switch3 eth1=daemon,,,switch15 eth2=daemon,,,switch16 mem=64M &
xterm -T BATU -e linux ubd0=BATU,jarkom umid=BATU eth0=daemon,,,switch4 eth1=daemon,,,switch5 eth2=daemon,,,switch21 eth3=daemon,,,switch22 mem=64M &
xterm -T MADIUN -e linux ubd0=MADIUN,jarkom umid=MADIUN eth0=daemon,,,switch22 eth1=daemon,,,switch25 mem=64M &
xterm -T KEDIRI -e linux ubd0=KEDIRI,jarkom umid=KEDIRI eth0=daemon,,,switch5 eth1=daemon,,,switch17 eth2=daemon,,,switch18 mem=64M &
xterm -T BLITAR -e linux ubd0=BLITAR,jarkom umid=BLITAR eth0=daemon,,,switch17 eth1=daemon,,,switch20 mem=64M &

# Server
xterm -T MALANG -e linux ubd0=MALANG,jarkom umid=MALANG eth0=daemon,,,switch18 mem=64M &
xterm -T MOJOKERTO -e linux ubd0=MOJOKERTO,jarkom umid=MOJOKERTO eth0=daemon,,,switch13 mem=64M &

# Klien
xterm -T SAMPANG -e linux ubd0=SAMPANG,jarkom umid=SAMPANG eth0=daemon,,,switch1 mem=64M &
xterm -T SIDOARJO -e linux ubd0=SIDOARJO,jarkom umid=SIDOARJO eth0=daemon,,,switch19 mem=64M &
xterm -T BANYUWANGI -e linux ubd0=BANYUWANGI,jarkom umid=BANYUWANGI eth0=daemon,,,switch16 mem=64M &
xterm -T JEMBER -e linux ubd0=JEMBER,jarkom umid=JEMBER eth0=daemon,,,switch16 mem=64M &
xterm -T BONDOWOSO -e linux ubd0=BONDOWOSO,jarkom umid=BONDOWOSO eth0=daemon,,,switch15 mem=64M &
xterm -T BOJONEGORO -e linux ubd0=BOJONEGORO,jarkom umid=BOJONEGORO eth0=daemon,,,switch25 mem=64M &
xterm -T JOMBANG -e linux ubd0=JOMBANG,jarkom umid=JOMBANG eth0=daemon,,,switch22 mem=64M &
xterm -T NGANJUK -e linux ubd0=NGANJUK,jarkom umid=NGANJUK eth0=daemon,,,switch21 mem=64M &
xterm -T TULUNGAGUNG -e linux ubd0=TULUNGAGUNG,jarkom umid=TULUNGAGUNG eth0=daemon,,,switch20 mem=64M &
xterm -T LUMAJANG -e linux ubd0=LUMAJANG,jarkom umid=LUMAJANG eth0=daemon,,,switch17 mem=64M &
```


### Konfigurasi UML

- Pada semua UML router, ketikkan nano /etc/sysctl.conf serta uncomment net.ipv4.ip_forward=1 . Untuk mengaktifkan perubahan baru ketikkan ```sysctl -p```.
- Setting pada semua interface UML seperti pada konfigurasi dibawah ini. Dengan mengetikkan 


```
nano /etc/network/interfaces
```

#### SURABAYA (Sebagai Router)


<img src="https://github.com/hrswcksono/Jarkom_Modul4_Lapres_D14/blob/main/image/SURABAYA.JPG" >

#### PASURUAN (Sebagai Router)


<img src="https://github.com/hrswcksono/Jarkom_Modul4_Lapres_D14/blob/main/image/PASURUAN.JPG" >


#### MOJOKERTO (Sebagai Server)


<img src="https://github.com/hrswcksono/Jarkom_Modul4_Lapres_D14/blob/main/image/MOJOKERTO.JPG" >


#### SAMPANG (Sebagai Klien)


<img src="https://github.com/hrswcksono/Jarkom_Modul4_Lapres_D14/blob/main/image/SAMPANG.JPG" >


#### PROBOLINGGO (Sebagai Router)

<img src="https://github.com/hrswcksono/Jarkom_Modul4_Lapres_D14/blob/main/image/PROBOLINGGO.JPG" >


#### SIDOARJO (Sebagai Klien)

<img src="https://github.com/hrswcksono/Jarkom_Modul4_Lapres_D14/blob/main/image/SIDOARJO.JPG" >

#### BANYUWANGI (Sebagai Klien)


<img src="https://github.com/hrswcksono/Jarkom_Modul4_Lapres_D14/blob/main/image/BANYUWANGI.JPG" >


#### JEMBER (Sebagai Klien)

<img src="https://github.com/hrswcksono/Jarkom_Modul4_Lapres_D14/blob/main/image/JEMBER.JPG" >

#### BONDOWOSO (Sebagai Klien)

<img src="https://github.com/hrswcksono/Jarkom_Modul4_Lapres_D14/blob/main/image/BONDOWOSO.JPG" >

#### BATU (Sebagai Router)

<img src="https://github.com/hrswcksono/Jarkom_Modul4_Lapres_D14/blob/main/image/BATU.JPG" >


#### KEDIRI (Sebagai Router)


<img src="https://github.com/hrswcksono/Jarkom_Modul4_Lapres_D14/blob/main/image/KEDIRI.JPG" >


#### JOMBANG (Sebagai Klien)


<img src="https://github.com/hrswcksono/Jarkom_Modul4_Lapres_D14/blob/main/image/JOMBANG.JPG" >



#### MADIUN (Sebagai Router)


<img src="https://github.com/hrswcksono/Jarkom_Modul4_Lapres_D14/blob/main/image/MADIUN.JPG" >


#### BOJONEGORO (Sebagai Klien)


<img src="https://github.com/hrswcksono/Jarkom_Modul4_Lapres_D14/blob/main/image/BOJONEGORO.JPG" >



#### NGANJUK (Sebagai Klien)


<img src="https://github.com/hrswcksono/Jarkom_Modul4_Lapres_D14/blob/main/image/NGANJUK.JPG" >


#### MALANG (Sebagai Server)


<img src="https://github.com/hrswcksono/Jarkom_Modul4_Lapres_D14/blob/main/image/MALANG.JPG" >



#### BLITAR (Sebagai Router)

<img src="https://github.com/hrswcksono/Jarkom_Modul4_Lapres_D14/blob/main/image/BLITAR.JPG" >


#### LUMAJANG (Sebagai Klien)


<img src="https://github.com/hrswcksono/Jarkom_Modul4_Lapres_D14/blob/main/image/LUMAJANG.JPG" >



#### TULUNGAGUNG (Sebagai Klien)


<img src="https://github.com/hrswcksono/Jarkom_Modul4_Lapres_D14/blob/main/image/TULUNGAGUNG.JPG" >


- pada UML SURABAYA diketikkan perintah 


```
iptables –t nat –A POSTROUTING –o eth0 –j MASQUERADE –s 192.168.0.0/16.
```


- Pada 4 router yaitu SURABAYA, PASURUAN, BATU, dan KEDIRI ditambahkan route baru. Berikut ini konfigurasi routing :

- Surabaya
<img src="https://github.com/hrswcksono/Jarkom_Modul4_Lapres_D14/blob/main/image/R_SURABAYA.JPG" >

- Pasuruan
<img src="https://github.com/hrswcksono/Jarkom_Modul4_Lapres_D14/blob/main/image/R_PASURUAN.JPG" >

- Batu
<img src="https://github.com/hrswcksono/Jarkom_Modul4_Lapres_D14/blob/main/image/R_BATU.JPG" >

- Kediri
<img src="https://github.com/hrswcksono/Jarkom_Modul4_Lapres_D14/blob/main/image/R_KEDIRI.JPG" >


- Jalankan bash script pada UML, menggunakan perintah source, jalankan dengan perintah ```source route.sh```.

### TESTING

- Lakukan testing dengan ping  untuk memastikan rancangan yang sudah dibentuk dalam topologi bekerja / connect satu sama lain.

- Berikut ini beberapa testing :

- Dari Jember ping ke Bondowoso
<img src="https://github.com/hrswcksono/Jarkom_Modul4_Lapres_D14/blob/main/image/jemberbondo.JPG" >


- Dari Batu ping ke Batu
<img src="https://github.com/hrswcksono/Jarkom_Modul4_Lapres_D14/blob/main/image/madiunbatu.JPG" >

- Dari Sampang ping ke Google
<img src="https://github.com/hrswcksono/Jarkom_Modul4_Lapres_D14/blob/main/image/sampangits.JPG" >








