# HACKATHON SYSTEM ADMINISTRATOR - SEMESTA BATCH 5

### NAMA : YOGA ADITYA PURNAMA PUTRA
### ASAL SEKOLAH : SMK TELKOM MALANG


##### Berikut penjelasan terkait 2 project terpisah yang dikerjakan dalam HACKATHON ini :

[PROJECT 1]

  Pembuatan Topologi infrastruktur jaringan SEVIMA dengan membuat data center yang diharapkan mampu menunjang performa aplikasi maupun backup sehingga waktu yang tidak terlalu lama.Oleh karena itu saya sebagai System Administrator membuat design jaringan dengan menerapkan beberapa macam layer diantaranya EDGE,CORE,DISTRIBUTION,ACCESS DAN DATA CENTER. Dimana pada masing-masing layer tersebut memiliki tugas masing-masing untuk mendistribusikan data maupun aplikasi ke DATA CENTER, sehingga performa akses aplikasi dapat berjalan secara optimal.
   
  Dalam Jaringan ini terdapat configuration yang diimplementasikan dimasing-masing layer diantaranya :
- EDGE(Router), bertugas sebagai link utama yang menghubungkan antara KANTOR PUSAT SEVIMA dan DATA CENTER. Di layer inilah proses routing antar ip dan firewall (ACL) terjadi.
- CORE(Switch L3), bertugas sebagai mengatur jaringan seperti routing ke UPLINK, membuat TRUNK to DOWN-LINK hingga VLAN MANAGEMENT $ DHCP. Di Core juga diterapkan Hot Standby Router Protocol (HSRP) sebagai redudancy / backup link apabila terjadi Disconnected LINK sehingga tidak terjadinya DOWN-TIME
- DISTRIBUTION (Switch L3), bertugas sebagai menyalur jaringan antara CORE dan ACCESS dikarenakan dari distribution inilah seluruh akses ke switch client disebar. Dengan adanya Distribution ini juga menambah keamanan jaringan agar client tidak langsung ke CORE layer.
- ACCESS (Switch L2), bertugas membagi hak akses yang dibutuhkan setiap user agar dapat terkoneksi jaringan sesuai dengan plot masing-masing menggunakan VLAN ACCESS
- DATA CENTER, adalah pusat berkumpulnya data seperti layaknya Cloud, dimana dalam desain ini dibuat terpisah sehingga proses data yang diharapkan juga sama dengan implementasi dilapangan. Selain itu dengan dibuat terpisah bisa menerapkan sistem protection jaringan baik intranet maupun ekstranet.

[PROJECT 2]

  Pada Project kedua ini saya sebagai System Administrator dituntut untuk melakukan handover terhadap problem dari Indonesia Swasembada Corp yaitu melakukan deployment, testing dan build web aplikasi secara otomatis yang sudah ada. Terdapat 2 web aplikasi yang berjalan. Akan tetapi dalam project ini belum dilakukan building aplikasi sehingga diperlukannya beberapa langkah untuk melakukannya. Disini saya menggunakan Automation Dockerizing dalam pengetesan dan building aplikasi menjadi sebuah image dan container. Dimana fungsi docker image (Dockerfile) digunakan untuk menentukan langkah-langkah apa saja yang dilakukan untuk menjalankan aplikasi yang telah dibuat,Baik cara download paket, install paket hingga menjalankan file testing yang telah dipersiapkan sebelumnya. Kemudian dibuatlah file yang bernama Dockercompose digunakan untuk membuat server berupa container. Dalam file inilah ditentukan apa saja yang perlu di install dalam container. Bahkan diperlukan juga network untuk mengkoneksikan 2 container aplikasi dan aplikasi 2

Berikut cara running file yang telah saya buat dalam project ini:

- Masukan file docker-compose.yml, Dockerfile dan .env pada folder Aplikasi-1 kemudian masukan juga file docker-compose.yml dan Dockerfile
- Kemudian buatkan docker network pada docker engine yang anda buat dengan nama sevima_app1_api_network
- jika sudah selesai Build aplikasi 1 dan aplikasi 2
- Kemudian masuk pada web browser dan ketik https://localhost:3000 untuk mengakses aplikasi 1 dan kemudian ketik https://localhost:3000/aboutus untuk akses aplikasi 2.
  Note : aplikasi 2 juga dapat diakses melalui port 3001


###TERIMA KASIH
