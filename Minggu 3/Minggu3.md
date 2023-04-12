# ADMIN JARINGAN KELOMPOK - 9

- 3121600015 - Fazaa Hanifan Hidayatullah
- 3121600027 - Daffa Ridwhan Ramadhan
- 3121600030 - Muhammad Latif

## LIST PROGRES MINGGU - 3

### 1. Reset Configuration Router - 9

Reset Konfigurasi dilakukan dengan menggunakan Winbox melalui Wine
Akses fitur di bagian sidebar pada menu System -> pilih Reset Configuration -> centang No Default Configuration -> klik Reset Configuration.
Setelah itu akan otomatis melakukan rebooting pada router dan aplikasi akan melakukan reconnecting.

### 2. Config IP Local & Public

Setelah rebooting akses fitur di sidebar pada menu IP -> Addresses -> klik tombol "+" ->

#### ETHER 1

- Address = 10.252.108.19/24
- Network = 10.252.108.0
- Interface = ETHER 1

#### ETHER 2

- Address = 192.168.9.1/24
- Network = 192.168.9.1/24
- Interface = ETHER 2

![Screenshot from 2023-03-16 14-25-01](https://user-images.githubusercontent.com/89375335/225556949-cf4b0ef3-2c6c-469e-ad60-11acf60b03fe.png)

### 3. Config Default Route

Akses fitur di sidebar pada menu New Terminal

#### Configurasi Default Route

```console
ip route add dst-address=0.0.0.0/0 gateway=10.252.108.1
ip ro pr
```

### 3. Configurasi DNS

Akses fitur di sidebar pada menu IP -> DNS -> masukkan IP Server=202.9.85.3
![Screenshot from 2023-03-16 14-29-10](https://user-images.githubusercontent.com/89375335/225663360-f629fe87-7b01-4df9-9066-4b870c98251e.png)

### 4. Config Internet Client

- Berikut konfigurasi lengkapnya

![Screenshot from 2023-03-16 14-35-02](https://user-images.githubusercontent.com/89375335/225664154-e409f7ec-4742-46c1-9245-bd1e4b54fecb.png)

### 5. Menambah IP Routes

Ketikkan pada New Terminal Winbox

```console
ip ro add gateway 10.252.108.11 dst 192.168.1.0/24
ip ro add gateway 10.252.108.12 dst 192.168.2.0/24
ip ro add gateway 10.252.108.13 dst 192.168.3.0/24
ip ro add gateway 10.252.108.14 dst 192.168.4.0/24
ip ro add gateway 10.252.108.15 dst 192.168.5.0/24
ip ro add gateway 10.252.108.16 dst 192.168.6.0/24
ip ro add gateway 10.252.108.17 dst 192.168.7.0/24
ip ro add gateway 10.252.108.18 dst 192.168.8.0/24
```

![Screenshot from 2023-03-16 14-37-11](https://user-images.githubusercontent.com/89375335/225664420-9a59dfeb-3c24-433a-832d-05ac639e0dc9.png)

![Screenshot from 2023-03-16 14-37-36](https://user-images.githubusercontent.com/89375335/225665519-62f6bff7-f3ae-46cc-80e1-fa51b0f2d52e.png)

### 6. Tes ping antar client

![Screenshot from 2023-03-16 14-52-19](https://user-images.githubusercontent.com/89375335/225664659-37185519-1c1a-4521-9712-26359f2e747f.png)

### 7. Export Config

Akses fitur di sidebar pada menu New Terminal, lalu ketikkan :

```console
export
```

dan file sudah berhasil di download ke komputer