# Posttest4_KantorPolisi


(MASUK PROGRAM)
Secara tampilan dan fungsi, output program pada Post Test 2 sama seperti Post Test 1, saat dijalankan aplikasi menampilkan menu utama (Informasi Kantor Polisi, Jadwal Patroli, Kasus Penyelidikan), tiap menu membuka sub-menu CRUD, dan data dicetak dalam tabel konsol rapi (mis. NRP | Nama | Pangkat | Status), sehingga perilaku hasil di layar tidak berubah; perbedaannya ada pada arsitektur dan kualitas internal kode dipisah per package dan program lebih terstruktur .

image
=> PENJELASAN

Saat dijalankan, 'AplikasiKantorPolisi' membuat data contoh (seed), lalu menampilkan Menu Utama berisi tiga yaitu: Informasi Kantor Polisi, Jadwal Patroli, dan Kasus Penyelidikan. saya memilih menu, kemudian di sub-menu menjalankan CRUD (tambah, lihat tabel, ubah, hapus) serta fitur cari/filter sesuai modul; setiap input dicek validasinya (NRP 3 digit unik, status hanya nilai yang diizinkan, dan NRP harus terdaftar saat membuat jadwal/kasus). Setelah sebuah aksi selesai, aplikasi kembali ke sub-menu; jika memilih Kembali, pengguna balik ke Menu Utama. Seluruh data selalu ditampilkan dalam tabel yang rapi dengan judul di tengah. Bila saya memilih Keluar, program menutup dengan aman.

MENGETIK ANGKA 1 (Informasi kantor Polisi) dan 1 (Tambah data Polisi)
image
=> PENJELASAN

Di layar ini saya masuk ke Informasi Kantor Polisi, memilih 1. POLISI, lalu terbuka submenu Fitur Informasi Polisi. Saya pilih 1. Tambah data polisi sehingga aplikasi meminta isian berurutan NRP, Nama, Pangkat, dan Status sambil melakukan validasi (NRP harus 3 digit dan unik, status hanya Aktif/Cuti). Saya mengisi NRP: 109, Nama: Yolla Karin, Pangkat: Brimob, Status: Aktif. Karena semua valid, data disimpan dan muncul pesan “Berhasil ditambahkan.” Setelah itu program kembali ke submenu Fitur Informasi Polisi supaya saya bisa lanjut aksi lain misalnya Lihat Data untuk memastikan Yolla Karin sudah tercatat, Ubah/Hapus, atau Kembali ke menu sebelumnya.

FITUR INFORMASI POLISI (2. Lihat data)
image
=> PENJELASAN

Selanjutnya saya berada di sub-menu Fitur Informasi Polisi dan memilih opsi 2 (Lihat Data), sehingga program menampilkan tabel "DAFTAR POLISI" berkolom NRP, Nama, Pangkat, dan Status yang berisi seluruh personel yang tersimpan saat ini; terlihat data yang baru saya tambahkan sebelumnya, yaitu NRP 109 Yolla Karin berpangkat Brimob dengan status Aktif, sedangkan baris lain adalah personel seed; setelah tabel dicetak, aplikasi otomatis kembali ke sub-menu yang sama agar saya bisa melanjutkan tindakan lain seperti melihat detail per NRP, mengubah, mencari, menghapus data, atau kembali ke Menu Utama.

FITUR INFORMASI POLISI (3. Detail ringkasan (by NRP))
image image
=> PENJELASAN

Pada tampilan ini saya berada di sub-menu Fitur Informasi Polisi dan memilih opsi 3 (Detail Ringkasan by NRP); program meminta saya memasukkan NRP, saya ketik 106, lalu sistem mencari data personel dengan NRP tersebut dan menampilkan ringkasan satu orang—NRP 106 atas nama Dhany Indra, pangkat Jendral, status Aktif dalam kotak “DETAIL RINGKASAN”; jika NRP tidak ditemukan mestinya muncul pesan penolakan, dan setelah ringkasan ditampilkan program otomatis mengembalikan saya ke sub-menu Fitur Informasi Polisi untuk memilih aksi berikutnya.

FITUR INFORMASI POLISI (4. Ubah data)
image image
=> PENJELASAN

Pada tampilan ini saya memilih opsi 4 (Ubah Data) di Fitur Informasi Polisi, lalu memasukkan NRP 102 agar sistem mencari record personel yang ingin diubah; program menawarkan tiga kolom yang bisa diisi sebagian atau dilewati (kosong = tidak diubah), jadi saya membiarkan nama kosong (tetap seperti semula), mengganti pangkat menjadi Kapolsek, dan mengisi status menjadi aktif; karena NRP 102 valid dan nilai status sesuai aturan (Aktif/Cuti), sistem berhasil memperbarui data dan menampilkan pesan “Diupdate.”, kemudian saya dikembalikan lagi ke sub-menu Fitur Informasi Polisi untuk melanjutkan aksi lain (misalnya lihat tabel untuk memastikan perubahan); jika NRP tidak ditemukan atau status tidak valid, muncul pesan penolakan dan perubahan dibatalkan.

FITUR INFORMASI POLISI (5. Cari (nama,pangkat))
image
=> PENJELASAN

Pada tampilan selanjutnya saya memilih opsi 5 (Cari) di Fitur Informasi Polisi, lalu saya memasukkan kata kunci "dhany indra"; sistem melakukan pencarian tidak pada kolom nama dan pangkat di seluruh data personel, kemudian menampilkan hasilnya dalam tabel "DAFTAR POLISI", dan karena hanya satu yang cocok maka muncul baris NRP 106 atas nama Dhany Indra berpangkat Jendral dengan status Aktif; jika tidak ada yang cocok tabel akan ditandai kosong, dan setelah hasil ditampilkan saya otomatis kembali ke sub-menu Fitur Informasi Polisi untuk melanjutkan tindakan lain seperti lihat detail, ubah, hapus, atau kembali ke Menu Utama.

FITUR INFORMASI POLISI (6. Hapus data)
image image
=> PENJELASAN

Selanjutnya saya berada di Fitur Informasi Polisi dan memilih opsi 6 (Hapus Data Polisi), lalu saya memasukkan NRP 108; sistem mengecek keberadaan NRP tersebut, menemukan recordnya, kemudian menghapusnya dari daftar personel dan menampilkan pesan "Dihapus." sebelum mengembalikan saya ke submenu yang sama; jika NRP tidak ada atau formatnya salah, akan muncul pesan penolakan dan tidak ada data yang berubah, dan bila saya memilih "Lihat Data" setelah ini, baris dengan NRP 108 sudah tidak tampil lagi.

FITUR INFORMASI POLISI (7. Kembali)
image
=> PENJELASAN

Di layar Fitur Informasi Polisi saya menekan 7 (Kembali). Perintah ini menutup submenu tersebut tanpa ada perubahan data. Aplikasi kemudian naik satu level ke layar INFORMASI KANTOR POLISI, yang berisi tiga opsi: 1. POLISI, 2. STAFF SIPIL, dan 3. Kembali. Kursor berhenti di bagian “Pilih:” menunggu perintah berikutnya; dari sini saya bisa masuk lagi ke modul Polisi, beralih ke Staff Sipil, atau menekan 3 untuk kembali ke Menu Utama.

FITUR STAFF SIPIL (1. Tambah Staff)
image
=> PENJELASAN

Dari layar Informasi Kantor Polisi saya memilih 2 (STAFF SIPIL), sehingga sistem membuka submenu Fitur Staff Sipil. Di submenu itu saya memilih 1 (Tambah Staff). Program lalu meminta data berurutan dan saya isi: ID Staff 204, Nama Zelsya, Bagian Keuangan, dan Status Aktif. Sistem memvalidasi bahwa ID harus 3 digit dan unik serta status hanya Aktif/Cuti; karena input saya valid, muncul konfirmasi “Berhasil ditambahkan.” Setelah penyimpanan, aplikasi menampilkan kembali layar Fitur Staff Sipil dan kursor berhenti di “Pilih:” untuk menunggu perintah berikutnya (lihat data, ubah, cari, hapus, atau kembali).

FITUR STAFF SIPIL (2. Lihat Data)
image
=> PENJELASAN

Di submenu Fitur Staff Sipil saya memilih 2 (Lihat Data). Sistem lalu menampilkan tabel Daftar Staff Sipil yang berisi data aktif saat ini—termasuk entri yang baru saya tambahkan sebelumnya. Pada layar terlihat empat baris: 201 Rani Puspita (Administrasi, Aktif), 202 Gilang P (Keuangan, Aktif), 203 Sinta Lestari (Umum, Cuti), dan 204 Zelsya (Keuangan, Aktif). Setelah tabel dicetak, aplikasi kembali menampilkan menu Fitur Staff Sipil dan kursor berhenti di “Pilih:”, siap menunggu perintah berikutnya (misalnya Detail/Ubah/Cari/Hapus atau kembali).

FITUR STAFF SIPIL (3. Detail Ringkasan - by ID)
image
=> PENJELASAN

Di menu Fitur Staff Sipil saya memilih 3 (Detail Ringkasan). Sistem meminta ID Staff, lalu saya masukkan 201. Aplikasi mencari data dengan ID tersebut dan menampilkan panel ringkasan berisi ID, Nama, Bagian, dan Status (pada layar: 201 / Rani Puspita / Administrasi / Aktif). Fitur ini hanya menampilkan informasi tidak mengubah data. Jika ID tidak ditemukan atau formatnya bukan 3 digit angka, sistem akan memberi pesan kesalahan. Setelah detail dicetak, aplikasi kembali ke menu Fitur Staff Sipil dan menunggu perintah berikutnya.

FITUR STAFF SIPIl (4. Ubah data)
image
=> PENJELASAN

Di menu Fitur Staff Sipil saya memilih 4 (Ubah Data). Sistem meminta ID Staff, lalu saya isi 204. Pada prompt berikutnya saya kosongkan Nama (artinya tidak diubah), lalu mengganti Bagian menjadi “Umum” dan Status menjadi “Aktif”. Aplikasi memvalidasi bahwa ID 3 digit tersebut ada dan status hanya boleh Aktif/Cuti. Karena valid, muncul konfirmasi “Diupdate.”. Setelah itu sistem kembali ke layar Fitur Staff Sipil dan menunggu perintah berikutnya. (Jika ID tidak ditemukan atau status tidak sesuai, sistem akan menolak dan menampilkan pesan error.)

FITUR STAFF SIPIL (5. Cari — nilai tambah)
image
=> PENJELASAN

Di submenu Fitur Staff Sipil saya memilih 5 (Cari) — ini adalah fitur pencarian (search) sehingga termasuk nilai tambahan dibanding Post Test 2 (di luar CRUD dasar). Saya mengetik kata kunci “Zelsya”. Program melakukan pencarian case-insensitive dan substring pada Nama dan Bagian, lalu menampilkan hasilnya dalam tabel Daftar Staff Sipil. Pada layar terlihat satu baris yang cocok: ID 204 / Zelsya / Umum / Aktif (sesuai data yang sebelumnya sudah saya ubah). Setelah hasil ditampilkan, aplikasi kembali ke menu Fitur Staff Sipil dan menunggu perintah berikutnya.

FITUR STAFF SIPIL (6. Hapus Data Staff → 2. Lihat Data)
image
=> PENJELASAN

Di submenu Fitur Staff Sipil saya memilih 6 (Hapus Data Staff), lalu memasukkan ID 204. Sistem memvalidasi ID (harus 3 digit dan ada di data); karena valid, muncul konfirmasi “Dihapus.”. Setelah balik ke menu yang sama, saya pilih 2 (Lihat Data) untuk memastikan. Tabel Daftar Staff Sipil tampil hanya dengan 201 Rani Puspita, 202 Gilang P, dan 203 Sinta Lestari artinya ID 204 (Zelsya) sudah benar-benar terhapus dari daftar.

FITUR STAFF SIPIL (7. Kembali) dan INFORMASI KANTOR POLISI (3. Kembali)
image
=> PENJELASAN

Selanjutnya dari Fitur Staff Sipil saya menekan 7 (Kembali) sehingga submenu staff ditutup tanpa mengubah data apa pun. Sistem membawa saya ke layar Informasi Kantor Polisi yang berisi tiga opsi (Polisi, Staff Sipil, Kembali). Di sini saya pilih 3 (Kembali) lagi untuk naik satu level. Aplikasi kemudian memuat ulang banner KANTOR POLISI dengan sapaan SELAMAT DATANG DI SISTEM KANTOR POLISI dan menampilkan Menu Utama berisi empat pilihan: Informasi Kantor Polisi, Jadwal Patroli, Kasus Penyelidikan, dan Keluar. Kursor berhenti di kolom “Pilih:” menunggu perintah berikutnya saya bisa lanjut ke modul lain dengan mengetik 1/2/3, atau keluar dari program dengan 4.

MASUK KE MENU JADWAL PATROLI
image
=> PENJELASAN

Selanjutnya dari menu utama, pengguna mengetik angka 2 untuk masuk ke Jadwal Patroli; layar kemudian menampilkan kotak berjudul “JADWAL PATROLI” dengan enam opsi, yaitu membuat jadwal baru dengan mengisi tanggal berformat dd-MM-yyyy, area patroli, dan NRP petugas sehingga sistem otomatis memberi ID berformat J-angka dan status awal “Dijadwalkan”; melihat seluruh jadwal dalam tabel rapi agar tanggal, area, nama petugas, dan status mudah dibaca; mengubah jadwal tertentu dengan memilih ubah tanggal atau ubah area serta dapat menandai Telah Selesai bila patroli sudah dilakukan; memfilter daftar berdasarkan area atau status untuk menampilkan jadwal yang relevan saja; menghapus jadwal dengan memasukkan ID yang sesuai; dan kembali ke Menu Utama bila ingin berpindah ke fitur lain.

JADWAL PATROLI (1. Buat jadwal)
image
=> PENJELASAN

disini saya berada di menu Jadwal Patroli dan memilih opsi 1 (Buat Jadwal), lalu saya mengisi Tanggal: 10-10-2025, Area: Perjuangan, dan NRP personel: 104; sistem mengecek bahwa NRP 104 terdaftar di data personel, kemudian membuat entri jadwal baru dengan status awal “Dijadwalkan” dan memberi nomor otomatis J-4, ditandai oleh pesan “Ditambahkan dengan ID: J-4”. Setelah jadwal berhasil dibuat, program mengembalikan saya ke menu Jadwal Patroli; jika saya memilih “Lihat Jadwal”, baris J-4 akan muncul pada tabel, sedangkan bila NRP tidak valid maka pembuatan jadwal akan ditolak dengan pesan kesalahan.

JADWAL PATROLI (2. Lihat jadwal)
image
=> PENJELASAN

Disini program akan masuk kembali ke fitur menu pada jadwal patroli disini saya menginput dan mengetikan angka 2 sehingga masuk ke Lihat Jadwal pada menu Jadwal Patroli; sistem kemudian mencetak tabel "DAFTAR JADWAL" dengan kolom yang sejajar id berformat J-angka, Tanggal dalam pola dd-MM-yyyy, Area patroli, Nama Polisi yang otomatis diambil dari NRP dan ditampilkan bersama pangkat di dalam tanda kurung, serta Status yang menunjukkan "Dijadwalkan" atau "Telah Selesai". Seluruh baris diambil dari ArrayList jadwal yang sudah di seed maupun yang baru dibuat. Dari tampilan ini saya bisa menilai rencana patroli secara cepat, lalu kembali ke menu untuk mengubah jadwal, menandai selesai, memfilter berdasarkan area atau status, atau menghapus jadwal tertentu.

JADWAL PATROLI (3. Ubah jadwal(Tanggal/Area) & Tandai Telah Selesai)
image
=> PENJELASAN

Selanjutnya saya berada di menu Jadwal Patroli dan memilih opsi 3 (Ubah Jadwal), kemudian saya memasukkan ID jadwal j-4; sistem membuka sub menu khusus "UBAH JADWAL: J-4" yang menawarkan empat aksi, saya memilih nomor 2 untuk mengubah area dan mengetik "Belatuk", sehingga data jadwal dengan ID J-4 diperbarui pada kolom Area (status dan tanggal tidak berubah) lalu saya dikembalikan ke menu Jadwal Patroli; jika setelah ini saya memilih "Lihat Jadwal", baris J-4 akan terlihat dengan area baru "Belatuk", sedangkan bila ID yang saya masukkan tidak valid, perubahan akan ditolak dan muncul pesan kesalahan.

JADWAL PATROLI (4. Filter Area/Status)
image image
=> PENJELASAN

Di bagian ini saya berada di menu Jadwal Patroli dan memilih opsi 4 (Filter Area/Status), lalu pada sub menu filter saya pilih nomor 2 (Status) dan mengetik “dijadwalkan”; sistem memvalidasi nilai status (hanya Dijadwalkan/Telah Selesai), kemudian menampilkan tabel “DAFTAR JADWAL” yang hanya berisi jadwal dengan status Dijadwalkan—terlihat J-1, J-2, dan J-4, di mana J-4 sudah memakai area baru “Belatuk”—serta kolom “Nama Polisi” diisi otomatis dari data personel (nama + pangkat); setelah hasil ditampilkan, saya dikembalikan ke menu Jadwal Patroli untuk melanjutkan aksi lain, dan jika saya memasukkan status yang tidak sesuai atau tidak ada data yang cocok maka tabel akan kosong.

JADWAL PATROLI (5. Hapus jadwal)
image
=> PENJELASAN

Pada bagian ini saya berada di menu Jadwal Patroli dan memilih opsi 5 (Hapus Jadwal); pertama saya memasukkan ID J-4, sistem menemukan data jadwal tersebut lalu menghapusnya dan menampilkan pesan "Dihapus.", setelah kembali ke menu saya mencoba lagi hapus dengan memasukkan ID yang tidak valid "12E2", sistem mengecek namun tidak menemukan data sehingga muncul pesan "ID tidak ditemukan." dan tidak ada perubahan pada data; jika ingin memastikan hasilnya, saya bisa memilih “Lihat Jadwal” untuk melihat bahwa J-4 sudah tidak ada.

JADWAL PATROLI (6. Kembali)
image
=> PENJELASAN

Selanjutnya pilih no 6 (Kembali) pada menu Jadwal Patroli, sehingga submenu ditutup tanpa mengubah data apa pun dan program langsung menampilkan lagi banner KANTOR POLISI serta SELAMAT DATANG DI SISTEM KANTOR POLISI, lalu memunculkan Menu Utama dengan empat opsi Informasi Polisi, Jadwal Patroli, Kasus Penyelidikan, dan Keluar serta kursor berhenti di kolom "Pilih:" untuk menunggu input berikutnya (1–4).

MASUK KE MENU KASUS PENYELIDIKAN
image
=> PENJELASAN

Dari Menu Utama disini ingin masuk kedalam menu kasus penyelidikan dan mengetik angka 3 untuk membuka Kasus Penyelidikan, lalu layar menampilkan kotak berisi pilihan pengelolaan kasus. Di sini pengguna dapat menambahkan kasus baru dengan mengisi judul dan NRP penyidik sehingga sistem otomatis membuat ID K-angka dan memberi status awal Baru; melihat daftar kasus dengan opsi filter sehingga dapat ditampilkan Semua, hanya yang Baru, yang sedang Proses, atau yang sudah Ditutup dalam tabel yang rapi; mengubah status suatu kasus dengan memasukkan ID lalu memilih apakah statusnya menjadi Baru, Proses, atau Ditutup agar perkembangan perkara tercatat; menghapus kasus tertentu dengan memasukkan ID bila datanya tidak lagi diperlukan; atau kembali ke Menu Utama. Seluruh perintah dijalankan dengan mengetik angka 1 sampai 5 pada kolom "Pilih:" sesuai kebutuhan.

KASUS PENYELIDIKAN (1. Tambah kasus)
image
=> PENJELASAN

Di menu Kasus Penyelidikan saya memilih opsi 1 (Tambah Kasus), lalu saya mengisi judul "Pembunuhan" dan NRP penyidik 104; sistem memeriksa bahwa NRP 104 terdaftar di data personel, menetapkan status awal kasus sebagai "Baru", membuat ID otomatis K-4, dan menampilkan konfirmasi "Ditambahkan dengan ID: K-4", setelah itu saya kembali ke menu Kasus Penyelidikan untuk melanjutkan (jika NRP tidak valid, penambahan akan ditolak dan tidak ada data baru yang dibuat).

KASUS PENYELIDIKAN (2. Lihat Kasus (Filter Status))
image
=> PENJELASAN

Pada bagian ini saya berada di menu Kasus Penyelidikan dan memilih opsi 2 (Lihat Kasus), lalu di sub-menu "LIHAT KASU" saya memilih 1 (Semua) sehingga sistem menampilkan tabel "DAFTAR KASUS" berisi seluruh kasus saat ini lengkap dengan kolom ID, Judul, Status, dan NRP penyidik; terlihat K-1 "Pencurian Motor di Pasar Raya" berstatus Baru, K-2 "Penipuan Online" berstatus Proses, K-3 "Penganiayaan Ringan" berstatus Ditutup, serta kasus yang baru saya tambahkan tadi K-4 "Pembunuhan" berstatus Baru dengan penyidik 104; setelah daftar dicetak, program kembali ke menu Kasus Penyelidikan agar saya bisa memilih aksi berikutnya (lihat per status, ubah status, atau hapus kasus).

KASUS PENYELIDIKAN (3. Ubah Status (Baru/Proses/Ditutup))
image
=> PENJELASAN

Pada layar ini saya berada di menu Kasus Penyelidikan dan memilih opsi 3 (Ubah Status), lalu saya memasukkan ID kasus k-1 dan status baru proses; sistem mengecek bahwa ID ada dan status termasuk pilihan yang valid (Baru/Proses/Ditutup), kemudian memperbarui status kasus k-1 menjadi Proses dan menampilkan pesan “Diupdate.” sebelum mengembalikan saya ke menu Kasus Penyelidikan; jika saya mengisi ID yang tidak ada atau status di luar pilihan, perubahan akan ditolak dan muncul pesan kesalahan.

KASUS PENYELIDIKAN (4. Hapus kasus)
image
=> PENJELASAN

Di bagian ini saya berada di menu Kasus Penyelidikan dan memilih opsi 4 (Hapus Kasus), lalu saya memasukkan ID k-4; sistem mengecek keberadaan kasus tersebut, menemukan datanya, kemudian menghapusnya dari daftar dan menampilkan konfirmasi “Dihapus.” sebelum mengembalikan saya ke menu Kasus Penyelidikan; jika saya memilih “Lihat Kasus” setelah ini, baris dengan ID k-4 sudah tidak ada, sedangkan bila ID yang saya masukkan tidak valid maka muncul pesan “ID tidak ditemukan” dan tidak ada perubahan data.

KASUS PENYELIDIKAN (5. Kembali)
image
=> PENJELASAN

Selanjutnya saya mengetik no 5 (Kembali) pada menu Kasus Penyelidikan, sehingga submenu ditutup tanpa mengubah data apa pun dan program menampilkan lagi banner KANTOR POLISI serta SELAMAT DATANG DI SISTEM KANTOR POLISI, lalu muncul Menu Utama dengan empat opsi1 Informasi Polisi, 2 Jadwal Patroli, 3 Kasus Penyelidikan, 4 Keluar.

KELUAR DARI PROGRAM
image
=> PENJELASAN

Selanjutnya saya ingin keluar dari program dan mengetik angka 4 (Keluar) di Menu Utama, program menampilkan pesan “Selesai.” dan eksekusi berakhir. Terminal/IDE kemudian mencetak ringkasan proses (BUILD SUCCESS, durasi, dan waktu selesai) sebagai tanda bahwa aplikasi Sistem Kantor Polisi telah ditutup dengan normal tanpa error.
