Nama:yudhistira ramadhani
Nrp: 3123521005
TI:A
. dining problem
Dining Philosophers Problem adalah masalah klasik dalam pemrograman konkuren dan sinkronisasi yang mengilustrasikan kebutuhan untuk menghindari deadlock ,deadlock adalah situasi dalam sistem komputasi dimana dua atau lebih proses tidak dapat melanjutkan eksekusinya karena masing masing menunggu sumber daya yang sedang digunakan oleh proses lain dan dapat diilustrasikan sebagai berikut  terdapat lima orang filsuf yang akan makan di meja disediakan lima buah sumpit  
![download (3)](https://github.com/YudhistiraRamadhani/SysOp24-3123521005/assets/154694700/06981673-27b0-4b42-bc44-153d6712c914)

jika filsuf lapar betul  maka ia akan mengambil dua  buah sumpit yaitu di tangan kanan dan tangan kiri  Namun adakalanya hanya diambil sumpit satu saja. Jika ada filsuf yang mengambil dua buah sumpit, maka ada filsuf yang harus menunggu sampai sumpit tersebut ditaruh kembali. Di dalam problema ini ada kemungkinan terjadi deadlock


reader writer problem
masalah sinkronisasi klasik pada sistem operasi ini berkisar pada tantangan mengelola sumberdaya bersama khususnya struktur data atau bagian kode yang diakses oleh banyak thread masalah muncul ketika menyeimbangkan kebutuhan akses oleh banyak  pembaca dengan akses eksklusif bagi satu penulis untuk memastikan konsistensi dan integritas data. Berbagai solusi seperti kunci, semafor, dan mekanisme sinkronisasi lainnya telah diusulkan untuk mengatasi masalah ini secara efisien. 
![reader writer](https://github.com/YudhistiraRamadhani/SysOp24-3123521005/assets/154694700/8e8a2136-f1fc-4121-868c-9e9eeb313ada)

 
Untuk menangani masalah ini, harus dipastikan bahwa tidak ada proses bersamaan yang menyebabkan segala bentuk ketidakkonsistenan data dalam sistem operasi. Masalah pembaca-penulis di os dapat diasumsikan

Solusi untuk Masalah tersebut
Untuk mengatasi masalah tersebut, kami memelihara tiga variabel, yaitu mutex, semaphore, dan readCount.
Mutex melakukan proses untuk melepaskan dan memperoleh kunci ketika readCount diperbarui. Kunci diperoleh ketika readCount diperbarui dan dikurangi kembali setelah melakukan operasi. Penulis menunggu semaphore sampai tiba gilirannya menulis dan menambah proses lain untuk menulis.
Idenya tetap menggunakan semaphore ketika pembaca memasuki bagian kritis hingga keluar dari bagian kritis sehingga tidak ada penulis yang dapat masuk di antara keduanya karena dapat menyebabkan inkonsistensi data. Semaphore digunakan untuk mencegah penulis mengakses sumber daya ketika ada satu atau lebih pembaca yang mengaksesnya.

