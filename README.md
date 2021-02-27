Petunjuk Pemasangan dan penggunaan 
Traffic Light Integration System

*note Untuk dapat menggunakan dengan baik diperlukan pemahaman dasar mengenai 
Penggunaan web server dengan all in one packet seperti XAMPP/LAMPP/WAMPP/MAMPP dll.
Pengetahuan dasar elektronika untuk memasang kabel
Pengetahuan dasar program di Arduino IDE untuk menyesuaikan pin dengan program NodeMCU
Sudah membaca Makalahnya dan PPT (bisa dicari di repository)

Langkah-langkah pemasangan

Download 4 file dari folder Traffic Light Integration System di repository bit.ly/KIRSmegaRepo/ => Project Lomba => Traffic Light Integration System
Folder tersebut berisi 
File server+ Web App Trigger
File NodeMCU (untuk traffic Light dan sensor)
File arduino (unutk buzzer)
File Trigger_App untuk android
File petunjuk pemasangan ini
Pemasangan File Server. 
Ekstrak file server yang sudah di download, copy di folder htdocs, ubah nama file server tersebut menjadi trigger-rest. untuk mengecek berhasil/tidak buka browser, masukan alamat localhost/trigger-rest , jika berhasil tampil halaman login web app.
Pemasangan kabel jumper.
Traffic ligt merah, kuning, hijau berurutan dipasang di pin D0,D1,D2 dan gnd dipasang di gnd nodeMCU.
Sensor Ultrasonik HC-SR04. GND to GND, VCC pasang ke 5V board NodeMCU. Pemasangan Echo dan Trig berurutan, misal echo D3, Trig D4, echo D5 trig D6 dst. *sesuaikan dengan programnya
Untuk buzzer pasang sendiri dengan arduino 
Upload program.
Ekstrak file nodemcu, terdapat 5 folder, 1 folder untuk 1 sisi persimpangan, misal diakhiri huruf B maka untuk Barat, U untuk Utara dst. *Jika program tidak berjalan setelah done uploading, lepaskan seluruh daya dan colokan lagi.
Setting Network.
Siapkan hp android, setting hotspot dengan ssid ard password kandah11
hubungkan laptop ke hotspot hp, dan ganti ipnya menjadi statis 192.168.43.122/24 gateway dan dns server 192.168.43.1 
NodeMCU akan otomatis terhubung ke hotspot hp jika dihidupkan (dapat diubah di program arduino IDE)
Setelah ini kalian bisa akses web server di 192.168.43.122/trigger-rest *pastikan XAMPP sudah jalan

 Penggunaan Traffic Light Integration System
Penggunaan aplikasi
Download aplikasi trigger android, setelah di install login dengan username admin password ADMTRIGGER (berlaku 1 hari, keesokan harinya harus logout dan login kembali)
Penggunaan Traffic Light Integration System
1. Nyalahkan hotspot HP yang sudah disetting, pastikan server di laptop sudah berjalan.
2. Colokan board nodeMCU dengan adaptor 9v 1 A, secara bersama sama! (lebih mudahnya pakai terminal yang terdapat button on/off)
3. disini minimal akan ada 5 perangkat yang terhubung ke HP, yaitu (4 nodeMCU (Utara, Timur, Selata, dan Barat) dan 1 Laptop.
4. Cek urutan lampu lalu lintas berjalannya mulah dari Utara hijau dahulu, kemudian setelah itu timur, selatan dan barat, (Searah jarum jam). 
5. Data dari nodeMCU dikirim setiap lampu hijau sisi utara menyala.
6. di aplikasinya untuk mengatur harus lewat perempatan sirongge, akan ada 2 mode, mode manual artinya mengatur sendiri setiap sisi, mode otomatisasi artinya hanya mengatur nilai default, pertambahan jika ramai dan pengurangan waktu jika sepi. Waktu yang diatur waktu lampu hijau dan yang lain akan menyesuaikan.

Kendala penggunaan
Masalah upload program, cara mengatasi cabut suplay dari adaptor dan usb, lalu colokan hanya usb untuk upload program
Waktu urutan tidak sesuai, pastikan menghidupakn nodemcu secara serentak bersama sama
Aplikasi tidak load data, logout dahulu, dan kemudian login kembali, jika masih gagal ada masalah dalam server
Sensor tidak akurat. pastikan kabel sudah terhubung, posisi sensor harus benar, dan semua sensor akan bekerja jika menggunakan power supply di Board Dev NodeMCU 

jika ada kendala yang tidak bisa kalian atasi, coba tanyakan kepada saya *an Singgih Ardiansyah cp 088225492972 
Semoga KIR_Smega bisa lebih jaya lagi.
Untuk selanjutnya, keep learning and hungry!.

