# Praktikum Modul 4 Jaringan Komputer

# Anggota Kelompok E27 :
| No.  | Nama Anggota       | NRP          |
|------|--------------------|--------------|
| 1    |Rachman Ridwan       | 5025201061   |
| 2    | Akmal Nafis         | 5025211216   |

#### Aura
```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet dhcp

auto eth1
iface eth1 inet static
address 10.50.0.25
netmask 255.255.255.252


auto eth2
iface eth2 inet static
address 10.50.0.21
netmask 255.255.255.252
```

### Revolte
```
auto eth0
iface eth0 inet static
address 10.50.0.2
netmask 255.255.255.252
gateway 10.50.0.1
```

### Richter
```
auto eth0
iface eth0 inet static
address 10.50.0.6
netmask 255.255.255.252
gateway 10.50.0.5
```


### Sein
```
auto eth0
iface eth0 inet static
address 10.50.4.2
netmask 255.255.252.0
gateway 10.50.4.1
```

### GrobeForest
```
auto eth0
iface eth0 inet dhcp
address 10.50.4.3
netmask 255.255.252.0
gateway 10.50.4.1
```

### Fern
```
auto lo
iface lo inet loopback

auto eth2
iface eth2 inet static
address 10.50.0.1
netmask 255.255.255.252
gateway 10.50.0.129

auto eth1
iface eth1 inet static
address 10.50.0.5
netmask 255.255.255.252

auto eth0
iface eth0 inet static
address 10.50.0.130
netmask 255.255.255.128
```

### Himmel
```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet static
address 10.50.0.14
netmask 255.255.255.252
gateway 10.50.0.13

auto eth1
iface eth1 inet static
address 10.50.2.1
netmask 255.255.254.0

auto eth2
iface eth2 inet static
address 10.50.0.129
netmask 255.255.255.128
```

#### Frieren
```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet static
address 10.50.0.22
netmask 255.255.255.252
gateway 10.50.0.21

auto eth1
iface eth1 inet static
address 10.50.0.17
netmask 255.255.255.252

auto eth2
iface eth2 inet static
address 10.50.0.13
netmask 255.255.255.252
```

#### Heiter
```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet static
address 10.50.0.26
netmask 255.255.255.252
gateway 10.50.0.25

auto eth1
iface eth1 inet static
address 10.50.8.1
netmask 255.255.248.0

auto eth2
iface eth2 inet static
address 10.50.4.1
netmask 255.255.252.0
```


### SchwerMountain
```
auto eth0
iface eth0 inet dhcp
address 10.50.0.131
netmask 255.255.255.128
gateway 10.50.0.129
```

### LaubHills
```
auto eth0
iface eth0 inet dhcp
address 10.50.2.2
netmask 255.255.254.0
gateway 10.50.2.1
```

### Stark
```
auto eth0
iface eth0 inet static
address 10.50.0.18
netmask 255.255.255.252
gateway 10.50.0.17
```

### TurkRegion
```
auto eth0
iface eth0 inet dhcp
address 10.50.8.2
netmask 255.255.248.0
gateway 10.50.8.1
```

## Routing

### Fern
```
echo nameserver 192.168.122.1 > /etc/resolv.conf
route add -net 10.50.0.0 netmask 255.255.255.252 gw 10.50.0.1
route add -net 10.50.0.4 netmask 255.255.255.252 gw 10.50.0.5
```

### Himmel
```
echo nameserver 192.168.122.1 > /etc/resolv.conf
route add -net 10.50.2.0 netmask 255.255.254.0 gw 10.50.2.1
route add -net 10.50.0.128 netmask 255.255.255.128 gw 10.50.0.129
route add -net 10.50.0.0 netmask 255.255.255.252 gw 10.50.0.130
route add -net 10.50.0.4 netmask 255.255.255.252 gw 10.50.0.130
```

### Frieren
```
echo nameserver 192.168.122.1 > /etc/resolv.conf
route add -net 10.50.0.16 netmask 255.255.255.252 gw 10.50.0.17
route add -net 10.50.0.12netmask 255.255.255.252 gw 10.50.0.14
route add -net 10.50.2.0 netmask 255.255.254.0 gw 10.50.0.14
route add -net 10.50.0.128 netmask 255.255.255.128 gw 10.50.0.14
route add -net 10.50.0.0 netmask 255.255.255.252 gw 10.50.0.14
route add -net 10.50.0.4 netmask 255.255.255.252 gw 10.50.0.14
```

### Heiter
```
echo nameserver 192.168.122.1 > /etc/resolv.conf
route add -net 10.50.4.0  netmask 255.255.252.0 gw 10.50.4.1
route add -net 10.50.8.0  netmask 255.255.248.0  gw 10.50.8.1
```

### Aura
```
route add -net 10.50.4.0  netmask 255.255.252.0 gw 10.50.0.26
route add -net 10.50.8.0  netmask 255.255.248.0  gw 10.50.0.26
route add -net 10.50.0.24  netmask 255.255.255.252 gw 10.50.0.26
route add -net 10.50.0.20 netmask 255.255.255.252 gw 10.50.0.22
route add -net 10.50.0.16 netmask 255.255.255.252 gw 10.50.0.22
route add -net 10.50.0.12netmask 255.255.255.252 gw 10.50.0.22
route add -net 10.50.2.0 netmask 255.255.254.0 gw 10.50.0.22
route add -net 10.50.0.128 netmask 255.255.255.128 gw 10.50.0.22
route add -net 10.50.0.0 netmask 255.255.255.252 gw 10.50.0.22
route add -net 10.50.0.4 netmask 255.255.255.252 gw 10.50.0.22
```

# Soal 1
Agar topologi yang kalian buat dapat mengakses keluar, kalian diminta untuk mengkonfigurasi Aura menggunakan iptables, tetapi tidak ingin menggunakan MASQUERADE.

```
ETH0_IP=$(ip -4 addr show eth0 | grep -oP '(?<=inet\s)\d+(\.\d+){3}')

iptables -t nat -A POSTROUTING -o eth0 -j SNAT --to-source $ETH0_IP
```

# Soal 2
Kalian diminta untuk melakukan drop semua TCP dan UDP kecuali port 8080 pada TCP.

```

# Menolak semua koneksi TCP yang ada kecuali pada port 8080
iptables -A INPUT -p tcp --dport 8080 -j ACCEPT
iptables -A INPUT -p tcp -j DROP

# Menolak semua koneksi UDP
iptables -A INPUT -p udp -j DROP
```

# Soal 3
Kepala Suku North Area meminta kalian untuk membatasi DHCP dan DNS Server hanya dapat dilakukan ping oleh maksimal 3 device secara bersamaan, selebihnya akan di drop.

```
# Allow related established connections
iptables -A INPUT -m state --state ESTABLISHED,RELATED -j ACCEPT

# Limit ICMP
iptables -A INPUT -p icmp -m connlimit --connlimit-above 3 --connlimit-mask 0 -j DROP
```

# Soal 4
Lakukan pembatasan sehingga koneksi SSH pada Web Server hanya dapat dilakukan oleh masyarakat yang berada pada GrobeForest.

```
iptables -A INPUT -p tcp --dport 22 -s 10.50.4.0/22 -j ACCEPT
iptables -A INPUT -p tcp --dport 22 -j DROP
```
# Soal 5
Selain itu, akses menuju WebServer hanya diperbolehkan saat jam kerja yaitu Senin-Jumat pada pukul 08.00-16.00.
```

iptables -A INPUT -p tcp --dport 80 -m time --timestart 08:00 --timestop 16:00 --weekdays Mon,Tue,Wed,Thu,Fri -j ACCEPT
```

# Soal 6
Lalu, karena ternyata terdapat beberapa waktu di mana network administrator dari WebServer tidak bisa stand by, sehingga perlu ditambahkan rule bahwa akses pada hari Senin - Kamis pada jam 12.00 - 13.00 dilarang (istirahat maksi cuy) dan akses di hari Jumat pada jam 11.00 - 13.00 juga dilarang (maklum, Jumatan rek).

```
iptables -A INPUT -p tcp --dport 80 -m time --timestart 12:00 --timestop 13:00 --weekdays Mon,Tue,Wed,Thu -j DROP
iptables -A INPUT -p tcp --dport 80 -m time --timestart 11:00 --timestop 13:00 --weekdays Fri -j DROP
```


# Soal 7
Karena terdapat 2 WebServer, kalian diminta agar setiap client yang mengakses Sein dengan Port 80 akan didistribusikan secara bergantian pada Sein dan Stark secara berurutan dan request dari client yang mengakses Stark dengan port 443 akan didistribusikan secara bergantian pada Sein dan Stark secara berurutan.
```
iptables -A PREROUTING -t nat -p tcp -d 10.50.4.2 --dport 80 -m statistics --mode nth --every 2 --packet 0 -j DNAT --to-destination 10.50.4.2:80
iptables -A PREROUTING -t nat -p tcp -d 10.50.4.2 --dport 80 -j DNAT --to-destination 10.50.0.14:80
```

# Soal 8
Karena berbeda koalisi politik, maka subnet dengan masyarakat yang berada pada Revolte dilarang keras mengakses WebServer hingga masa pencoblosan pemilu kepala suku 2024 berakhir. Masa pemilu (hingga pemungutan dan penghitungan suara selesai) kepala suku bersamaan dengan masa pemilu Presiden dan Wakil Presiden Indonesia 2024.

```
iptables -t nat -A PREROUTING -p tcp -d 10.50.0.4 --dport 443 -m statistic --mode nth --every 2 --packet 0 -j DNAT --to-destination 10.50.4.2:443
iptables -t nat -A PREROUTING -p tcp -d 10.50.0.4 --dport 443 -j DNAT --to-destination 10.50.0.14:443
```

# Soal 9
Sadar akan adanya potensial saling serang antar kubu politik, maka WebServer harus dapat secara otomatis memblokir  alamat IP yang melakukan scanning port dalam jumlah banyak (maksimal 20 scan port) di dalam selang waktu 10 menit. 
(clue: test dengan nmap)

# Soal 10
Karena kepala suku ingin tau paket apa saja yang di-drop, maka di setiap node server dan router ditambahkan logging paket yang di-drop dengan standard syslog level.
# Kesulitan dan masalah
