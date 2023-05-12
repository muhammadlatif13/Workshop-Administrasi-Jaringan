### Kelas : 2 D4 Informatika A 2021

# Konfigurasi DNS pada slave 
## 1. Edit file named.conf.local:
- Jalankan perintah berikut untuk akses edit
```
nano /etc/bind/named.conf.local
```
- edit menjadi allow-transfer seperti gambar dibawah ini
![named.conf.local](https://raw.githubusercontent.com/rizal15D/WorkshopAdministrasiJaringan/main/Minggu%2011/Assets/1.png)

## 2. Edit file /var/cache/bind9/kampus-07.takehome-forward
- Jalankan perintah berikut untuk akses edit
```
nano /var/cache/bind9/kampus-07.takehome-forward
```
- edit menjadi 10.252.108.10 seperti gambar dibawah ini
![forward](https://raw.githubusercontent.com/rizal15D/WorkshopAdministrasiJaringan/main/Minggu%2011/Assets/2.png)

## 3. Restart bind9
- Jalankan perintah berikut dan lihat statusnya
```
systemctl restart bind9.service
systemctl status bind9.service
```
![bind9](https://raw.githubusercontent.com/rizal15D/WorkshopAdministrasiJaringan/main/Minggu%2011/Assets/3.png)

## 4. berikut hasilnya
- Laravel berjalan namun masih ada error di laravel
![laravel](https://raw.githubusercontent.com/rizal15D/WorkshopAdministrasiJaringan/main/Minggu%2011/Assets/4.jpeg)
