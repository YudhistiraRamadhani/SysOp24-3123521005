Nama: Yudhistira Ramadhani
Nrp: 3123521005
TI : A
Producer,concumen problem in C (masalah produsen dan konsumen di C) Atau yang disebut masalah terikat buffer

Buffer adalah tempat penyimpanan di memori yang menyimpan data , buffer pada permasalahan produsen dan konsumen adalah di c adalah berisi barang yang di produksi oleh produsen 

Gambarannya adalah produsen itu seperti pembuat/bagian memproduksi dan konsumen adalah orang yang mengkonsumsi produk dan buffer adalah tempat penyimpanan sementara di memori dan dalam masalah producen dan konsumen ini buffer diibaratkan tempat untuk mengelola bahan produsen karena buffer adalah tempat penyimpanan yang pada permasalahan ini diibaratkan oleh oven karena menyimpan data data itu diibaratkan adonan roti yang dimasukkan ke oven yaitu buffer 

Contoh problemnya adalah penjual roti penjual(produsen)  roti menerima pesanan oleh pelanggan (konsumen)  sementara mesin pembuat roti (buffer) mampu memproduksi maksimal 50 kue karena mesin pembuat roti (buffer) mampu membuat maksimal 50 kue karena mesin pembuat roti (buffer) belum terlalu besar 
 Dan mempunyai kode sistem manajemen roti

int OVEN_SIZE = 50; 
int kue = 0;
prosedur pembuat roti() 
{ 
    while (benar) 
    { 
        kue = kue_bake(); 

        if (kue == OVEN_SIZE) 
        { 
            tidur(); 
        } 

        putCakeInDisplay(kue); 
        kue = kue + 1; 

        if (kue == 1) 
        { 
            bangun(konsumen); 
        } 
    } 
} 

prosedur pelanggan() 
{ 
    while (benar) 
    { 

        if (kue == 0) 
        { 
            tidur(); 
        } 

        barang = takeCakeFromBakery(); 
        kue = kue - 1; 

        if (kue == OVEN_SIZE - 1) 
        { 
            bangun(tukang roti); 
        } 

        beli_kue(kue); 
    } 
}
Dari kode di atas; secara intuitif kita dapat memahami hal berikut:
1.	Jika toko roti Anda memiliki kue==0; lalu Anda mengirim pesan ke semua pelanggan Anda bahwa “sleep();” 
Artinya : jika  toko roti Anda memiliki kue = 0 , maka Anda mengirim kan pesan ke semua pelanggan Anda bahwa tidur
2.	Sampai oven Anda belum penuh (kue != 50), pembuat roti Anda terus membuat kue segar.
Artinya : apabila kue di oven tidak sampai 50 pembuat roti terus membuat kue 
3.	Namun, jika oven sudah penuh, pembuat roti akan tidur sampai pelanggan membeli kue dan kue != 50. Ini mengirimkan pesan kepada pembuat roti bangun(baker);

4.	Dan jika kue Anda == 1, maka ia akan mengirimkan pesan kepada Pelanggan bahwa wakeup(customer);
Artinya : jika kue = 1 maka produsen mengirikan pesan kepada pelanggan bahwa bangun ! (customer}



![Screenshot (1147)](https://github.com/YudhistiraRamadhani/SysOp24-3123521005/assets/154694700/9a305dbe-4b62-4ea8-9ab7-53b9c042c99d)

Keterangan : Masalah produsen konsumen adalah masalah sinkronisasi. Ada buffer dengan ukuran tetap (di sini, OVEN_SIZE) dan produsen (tukang roti) memproduksi item (kue) dan memasukkannya ke dalam buffer (oven) . Konsumen (pelanggan) mengeluarkan barang dari buffer dan mengkonsumsi (membeli) barang tersebut  yaitu kue 
