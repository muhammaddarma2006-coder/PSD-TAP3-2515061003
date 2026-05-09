Program Pencarian buku Searching Met.Sequential Search

Mmeilih implementasi pencarian buku didasarkan pada relevansi skenario dunia nyata dalam pengelolaan data perpustakaan atau koleksi pribadi yang diamna itu jauh lebih mudah
di implementasikan.Dan mengapa saya memilih metode Sequential Search didasarkan pada beberapa keunggulan teknis seperti Kesederhanaan Implementasi, lalu Efisiensi pada Skala Kecil
, terakhir karena Akurasi Pencarian Ganda di mana kita perlu memindai seluruh daftar guna menghitung total kemunculan data yang sama.

Source code

INPUT

![image alt](https://github.com/muhammaddarma2006-coder/PSD-TAP3-2515061003/blob/b95ed64846b18a5b8556fd4707cbf310a5053f25/Screenshot%20(2410).png)

[Gmabar satu] Fungsi sequential_search_buku dalam program ini dimulai dengan melakukan inisialisasi dua variabel utama, yaitu variabel i yang diatur ke angka 0 sebagai penunjuk indeks awal dan variabel counter yang juga diatur ke angka 0 sebagai wadah untuk menyimpan jumlah buku yang ditemukan nantinya. Sebelum memasuki proses pencarian, program melakukan normalisasi pada teks yang dicari dengan perintah target = target.lower() agar sistem tidak membedakan antara huruf besar dan kecil, sehingga pencarian menjadi lebih akurat bagi pengguna. Inti dari algoritma ini terletak pada perulangan while i < n yang bertugas menyisir setiap elemen di dalam daftar selama posisi penunjuk belum melewati total panjang data yang tersedia. Di dalam setiap putaran perulangan, program akan menjalankan logika pengkondisian untuk membandingkan apakah judul buku pada posisi tertentu yang juga sudah diubah ke huruf kecil memiliki kecocokan dengan judul target. Jika ditemukan kecocokan, maka nilai dalam variabel counter akan ditambah satu poin, dan setelah itu variabel i akan selalu ditambah satu agar program dapat berpindah memeriksa buku pada urutan selanjutnya. Setelah seluruh daftar selesai diperiksa tanpa ada yang terlewat, fungsi ini diakhiri dengan perintah return counter yang berfungsi untuk mengirimkan total laporan jumlah penemuan kembali ke bagian utama program untuk ditampilkan.


![image alt](https://github.com/muhammaddarma2006-coder/PSD-TAP3-2515061003/blob/b95ed64846b18a5b8556fd4707cbf310a5053f25/Screenshot%20(2411).png)

[Gambar dua] bagian ini fungsi utama, main() yang bertugas menyiapkan data awal sebelum pencarian dilakukan. Di dalamnya terdapat variabel data yang menyimpan daftar judul buku dalam bentuk list berjumlah tujuh judul buku, seperti "Struktur Data", "Basis Data", dan lainnya, yang berfungsi sebagai simulasi koleksi buku di sebuah rak. Selanjutnya, terdapat perintah n = len(data) yang berfungsi untuk menghitung secara otomatis berapa jumlah total buku yang ada di dalam daftar tersebut agar program mengetahui batas akhir pencarian. Terakhir, perintah print digunakan untuk menampilkan seluruh isi daftar buku ke layar sehingga pengguna dapat melihat buku apa saja yang tersedia di dalam rak tersebut sebelum mulai mencari.

![image alt](https://github.com/muhammaddarma2006-coder/PSD-TAP3-2515061003/blob/b95ed64846b18a5b8556fd4707cbf310a5053f25/Screenshot%20(2412).png)

[Gambar tiga] terakhir bagian ini adalah interaksi pengguna dan eksekusi program utama yang memastikan data diproses dengan benar. Bagian ini dimulai dengan perulangan while True yang berfungsi sebagai validasi input, di mana program akan terus meminta pengguna memasukkan judul buku dan hanya akan berhenti atau break jika input tersebut tidak kosong. Setelah mendapatkan nama buku yang valid, program memanggil fungsi sequential_search_buku dengan mengirimkan data, jumlah buku, dan target yang dicari, lalu menyimpan hasilnya ke dalam variabel jumlah_ditemukan. Logika berikutnya adalah pencabutan if-else yang bertugas menampilkan hasil akhir ke layar; jika nilai jumlah_ditemukan lebih besar dari nol, maka program mencetak pesan bahwa buku berhasil ditemukan beserta total jumlahnya, namun jika nol, maka akan muncul pesan bahwa buku tidak ditemukan. Bagian paling bawah, if __name__ == "__main__":, merupakan standar dalam Python untuk memastikan bahwa fungsi main() hanya akan dijalankan secara otomatis jika file ini dieksekusi secara langsung sebagai program utama.

OUTPUT

![image alt](https://github.com/muhammaddarma2006-coder/PSD-TAP3-2515061003/blob/be5651c969817d2f48f1dbc8bff2f46561d7d2e5/Screenshot%20(2414).png)

[Gambar scenario pertama] kita ambil contoh yang pertama dulu jika memasukkan input buku berjudul "Basis data", program menjalankan metode Sequential Search dengan memeriksa seluruh isi rak dari awal hingga akhir. Karena judul "Basis Data" muncul sebanyak tiga kali dalam daftar (terletak pada posisi kedua, kelima, dan ketujuh), variabel counter berhasil mengumpulkan total hitungan sebanyak tiga poin, sehingga sistem memberikan laporan bahwa ditemukan 3 buah buku di rak.

![image alt](https://github.com/muhammaddarma2006-coder/PSD-TAP3-2515061003/blob/be5651c969817d2f48f1dbc8bff2f46561d7d2e5/Screenshot%20(2415).png)

[Gambar scenrio kedua] pada contoh gambar kedua dengan input "Jaringan", program melakukan penyisiran yang sama namun hanya menemukan satu kecocokan tepat pada posisi keenam. Karena pencarian berlanjut hingga data terakhir dan tidak menemukan judul serupa lagi, variabel counter hanya bernilai satu, yang kemudian ditampilkan sebagai laporan akhir kepada Kita sebagai penggunanya.



video link demonstrasi program parkir sorting metode selection sort :
https://youtu.be/t2mWC4dumVU


