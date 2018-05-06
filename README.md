# Tugas Worskhop Cloud ke 1
Tentang Deployment Stateless App Menggunakan Kubernetes

Langkah pertama proses deployment yaitu buat file nginx.yml dan service.yml, kemudian create deployment di kubernetes dengan perintah:

``` kubectl create -f nginx.yml ```

Setelah proses create, maka akan terbentuk 2 buah pods. Untuk mengeceknya dengan perintah :

``` kubectl get pods ```

![Hasil pods()](https://github.com/slamet789/Tugas-Worskhop-Cloud-ke-1/blob/master/1.jpg)

Langkah kedua, create service di kubernetes dengan perintah :

``` kubectl create -f service.yml ```

maka akan terbentuk service baru

![Hasil service()](https://github.com/slamet789/Tugas-Worskhop-Cloud-ke-1/blob/master/2.jpg)

Untuk mengecek apakah service telah berjalan, pada Display port katacoda isi dengan port 30562. Berikut merupakan output tampilannya :

![Hasil output1()](https://github.com/slamet789/Tugas-Worskhop-Cloud-ke-1/blob/master/3.jpg)

![Hasil output2()](https://github.com/slamet789/Tugas-Worskhop-Cloud-ke-1/blob/master/4.jpg)
