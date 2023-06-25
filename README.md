# HACKATHON SYSTEM ADMINISTRATOR - SEMESTA BATCH 5

### NAMA : YOGA ADITYA PURNAMA PUTRA
### ASAL SEKOLAH : SMK TELKOM MALANG


Berikut penjelasan terkait 2 project terpisah yang dikerjakan dalam HACKATHON ini :
[PROJECT 1]
Pembuatan Topologi infrastruktur jaringan SEVIMA dengan membuat data center yang diharapkan mampu menunjang performa aplikasi maupun backup sehingga waktu yang tidak terlalu lama.Oleh karena itu saya sebagai System Administrator membuat design jaringan dengan menerapkan beberapa macam layer diantaranya EDGE,CORE,DISTRIBUTION,ACCESS DAN DATA CENTER. Dimana pada masing-masing layer tersebut memiliki tugas masing-masing untuk mendistribusikan data maupun aplikasi ke DATA CENTER, sehingga performa akses aplikasi dapat berjalan secara optimal.
  Dalam Jaringan ini terdapat configuration yang diimplementasikan dimasing-masing layer diantaranya :
- EDGE(Router), bertugas sebagai link utama yang menghubungkan antara KANTOR PUSAT SEVIMA dan DATA CENTER. Di layer inilah proses routing antar ip dan firewall (ACL) terjadi.
- CORE(Switch L3), bertugas sebagai mengatur jaringan seperti routing ke UPLINK, membuat TRUNK to DOWN-LINK hingga VLAN MANAGEMENT $ DHCP. Di Core juga diterapkan Hot Standby Router Protocol (HSRP) sebagai redudancy / backup link apabila terjadi Disconnected LINK sehingga tidak terjadinya DOWN-TIME
- DISTRIBUTION (Switch L3), bertugas sebagai menyalur jaringan antara CORE dan ACCESS dikarenakan dari distribution inilah seluruh akses ke switch client disebar. Dengan adanya Distribution ini juga menambah keamanan jaringan agar client tidak langsung ke CORE layer.
- ACCESS (Switch L2), bertugas membagi hak akses yang dibutuhkan setiap user agar dapat terkoneksi jaringan sesuai dengan plot masing-masing menggunakan VLAN ACCESS
- DATA CENTER, adalah pusat berkumpulnya data seperti layaknya Cloud, dimana dalam desain ini dibuat terpisah sehingga proses data yang diharapkan juga sama dengan implementasi dilapangan. Selain itu dengan dibuat terpisah bisa menerapkan sistem protection jaringan baik intranet maupun ekstranet.

[PROJECT 2]
