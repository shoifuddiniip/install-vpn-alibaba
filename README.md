Cara Config OpenVPN Server di Ubuntu
Dalam artikel ini, kami akan membahas cara config Openvpn server pada VPS Ubuntu. Pada contoh berikut, kami menggunakan VPS Alibaba Cloud. Berikut langkah-langkahnya.

Langkah 1. Cari Ip Address VPS
Pertama kita memastikan dulu IP Address yang akan kita gunakan apakah sudah sesuai dengan IP Address dari VPS-nya atau belum dengan perintah berikut.

#dig +short myip.opendns.com @resolver1.opendns.com

Cara Config OpenVPN Server di VPS Ubuntu image 1
Maka nanti akan muncul IP Address dari VPS yang digunakan.

Cara Config OpenVPN Server di VPS Ubuntu image 2
Langkah 2. Download dan jalankan
Selanjutnya ada download script OpenVPN yang akan kita gunakan untuk membuat OpenVPN Server pada VPS Ubuntu.

#wget https://git.io/vpn -O openvpn-install.sh


Pastikan file yang kita download menggunakan wget sudah berhasil, dengan menggunakan perintah ls.


Setelah itu kita tinggal jalankan script tersebut, dengan perintah berikut

# ./openvpn-install.sh


Ketika kita berhasil menjalankan scriptnya  maka akan muncul tampilan untuk menuliskan konfigurasi pada Openvpn Server yang akan dibuat. 

Hostname
Pada bagian Ip address/Hostname kita diminta untuk memasukan hostname, secara default kita bisa menggunakan Ip Address pada VPS


Protocol
Kita bisa menentukan Protocol yang akan didigunakan, dalam artikel ini kita akan mengikuti rekomendasi dari scripntya.


Port
Untuk Port, kita bisa menggunakan default dari OpenVPN.


DNS
Kita bisa memilih DNS yang kita inginkan namun dalam artikel ini kita akan menggunakan DNS Google.


Client name
Untuk nama client, silahkan sesuaikan dengan yang kita inginkan.



Terakhir dari konfigurasi diatas adalah setelah mengisikan data yang dibutuhkan maka nanti ketika kita klik enter maka secara otomatis akan melakukan installasi OpenVPN Server pada VPS Ubuntu.

Kemudian jika instalasi sudah selesai, kita start service OpenVPN nya lalu kita lihat status dari service tersebut.

#systemctl start openvpn-server@server.service


#systemctl status openvpn.service


Langkah 3. OpenVPN Client
Setelah konfigurasi berhasil, maka secara otomatis akan men generate file .ovpn yang nanti file tersebut kita gunakan untuk menghubungkan OpenVPN Client dengan Server yang sudah kita setting sebelumnya.

File tersebut secara default berada di home direktori, jika kita login sebagai root maka akan tergenerate pada “/root”. Dan nama filenya akan menggunakan nama dari client yang kita input pada konfigurasi sebelumnya.


Lalu kita bisa download file tersebut dan pindahkan ke perangkat yang akan kita hubungkan ke OpenVPN Server. Untuk detail cara menghubungkan perangkat mobile, komputer atau laptop ke OpenVPN Server yang telah dikonfigurasi bisa akses ke halaman berikut, klik disini.

Demikian artikel mengenai cara config OpenVPN Server di VPS Ubuntu, semoga dapat bermanfaat. Terima kasih 😀Cara Config OpenVPN Server di Ubuntu
Dalam artikel ini, kami akan membahas cara config Openvpn server pada VPS Ubuntu. Pada contoh berikut, kami menggunakan VPS Alibaba Cloud. Berikut langkah-langkahnya.

Langkah 1. Cari Ip Address VPS
Pertama kita memastikan dulu IP Address yang akan kita gunakan apakah sudah sesuai dengan IP Address dari VPS-nya atau belum dengan perintah berikut.

#dig +short myip.opendns.com @resolver1.opendns.com

Cara Config OpenVPN Server di VPS Ubuntu image 1
Maka nanti akan muncul IP Address dari VPS yang digunakan.

Cara Config OpenVPN Server di VPS Ubuntu image 2
Langkah 2. Download dan jalankan
Selanjutnya ada download script OpenVPN yang akan kita gunakan untuk membuat OpenVPN Server pada VPS Ubuntu.

#wget https://git.io/vpn -O openvpn-install.sh


Pastikan file yang kita download menggunakan wget sudah berhasil, dengan menggunakan perintah ls.


Setelah itu kita tinggal jalankan script tersebut, dengan perintah berikut

# ./openvpn-install.sh


Ketika kita berhasil menjalankan scriptnya  maka akan muncul tampilan untuk menuliskan konfigurasi pada Openvpn Server yang akan dibuat. 

Hostname
Pada bagian Ip address/Hostname kita diminta untuk memasukan hostname, secara default kita bisa menggunakan Ip Address pada VPS


Protocol
Kita bisa menentukan Protocol yang akan didigunakan, dalam artikel ini kita akan mengikuti rekomendasi dari scripntya.


Port
Untuk Port, kita bisa menggunakan default dari OpenVPN.


DNS
Kita bisa memilih DNS yang kita inginkan namun dalam artikel ini kita akan menggunakan DNS Google.


Client name
Untuk nama client, silahkan sesuaikan dengan yang kita inginkan.



Terakhir dari konfigurasi diatas adalah setelah mengisikan data yang dibutuhkan maka nanti ketika kita klik enter maka secara otomatis akan melakukan installasi OpenVPN Server pada VPS Ubuntu.

Kemudian jika instalasi sudah selesai, kita start service OpenVPN nya lalu kita lihat status dari service tersebut.

#systemctl start openvpn-server@server.service


#systemctl status openvpn.service


Langkah 3. OpenVPN Client
Setelah konfigurasi berhasil, maka secara otomatis akan men generate file .ovpn yang nanti file tersebut kita gunakan untuk menghubungkan OpenVPN Client dengan Server yang sudah kita setting sebelumnya.

File tersebut secara default berada di home direktori, jika kita login sebagai root maka akan tergenerate pada “/root”. Dan nama filenya akan menggunakan nama dari client yang kita input pada konfigurasi sebelumnya.


Lalu kita bisa download file tersebut dan pindahkan ke perangkat yang akan kita hubungkan ke OpenVPN Server. Untuk detail cara menghubungkan perangkat mobile, komputer atau laptop ke OpenVPN Server yang telah dikonfigurasi bisa akses ke halaman berikut, klik disini.

Demikian artikel mengenai cara config OpenVPN Server di VPS Ubuntu, semoga dapat bermanfaat. Terima kasih 😀
