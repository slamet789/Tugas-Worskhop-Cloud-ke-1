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

Langkah ketiga, lakukan editing file index.html di salah satu pods nginx-697d4d67f9-m9s9d. Berikut prosesnya :

![Hasil proses1()](https://github.com/slamet789/Tugas-Worskhop-Cloud-ke-1/blob/master/5.jpg)

![Hasil proses2()](https://github.com/slamet789/Tugas-Worskhop-Cloud-ke-1/blob/master/6.jpg)

![Hasil proses3()](https://github.com/slamet789/Tugas-Worskhop-Cloud-ke-1/blob/master/7.jpg)

Langkah keempat, untuk membuktikan data file index.html yang telah diedit bersifat stateless. Lakukan delete terhadap pods nginx-697d4d67f9-m9s9d dengan perintah 

``` kubectl delete pods nginx-697d4d67f9-m9s9d ```

![Hasil delete()](https://github.com/slamet789/Tugas-Worskhop-Cloud-ke-1/blob/master/8.jpg)

Kubernetes secara otomatis akan membuat pods yang baru setiap dilakukan penghapusan terhadap salah satu pods. Berikut merupakan pods yang baru terbentuk 

![Hasil baru()](https://github.com/slamet789/Tugas-Worskhop-Cloud-ke-1/blob/master/9.jpg)

Data file index.html yang tersimpan di pod nginx-697d4d67f9-m9s9d secara otomatis akan terhapus dan digantikan data file index.html yang yang ada di pod nginx-697d4d67f9-j6zrz (pod yang baru terbentuk). Berikut merupakan pengecekan dan tampilan outputnya

![Hasil cek()](https://github.com/slamet789/Tugas-Worskhop-Cloud-ke-1/blob/master/10.jpg)

![Hasil cek2()](https://github.com/slamet789/Tugas-Worskhop-Cloud-ke-1/blob/master/11.jpg)

![Hasil cek3()](https://github.com/slamet789/Tugas-Worskhop-Cloud-ke-1/blob/master/12.jpg)



