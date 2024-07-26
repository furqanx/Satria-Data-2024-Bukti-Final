#### **Penjelasan**

**Note** : *jika ada yang tidak dipahami, mohon jangan sungkan untuk menanyakan atau mengklarifikasikan dengan kami lagi ya kak*

Alur pengerjaan notebook ini adalah sebagai berikut:
- **Lakukan preprocessing pada data unlabeled** kemudian data hasil preprocessing disimpan untuk digunakan pada tahap pelabelan data
- **Lakukan training model machine learning** dengan menggunakan model pretrained IndoBERT. Pelatihan model dilakukan sebanyak 10 kali dengan menggunakan nilai parameter yang berbeda (batch size, learning rate, dan jumlah epoch). Untuk informasi mengenai parameter-parameter yang digunakan, kami memberikan informasinya seperti dibawah ini.

berikut dibawah ini jenis parameter yang digunakan :
- menggunakan model IndoBERT Large P2 dengan epoch 3, learning rate 2e-5, dan batch size 32.
- menggunakan model IndoBERT Large P2 dengan epoch 10, learning rate 1e-5, dan batch size 32.
- menggunakan model IndoBERT Large P2 dengan epoch 10, learning rate 2e-5, dan batch size 32.
- menggunakan model IndoBERT Large P2 dengan epoch 2, learning rate 2e-5, dan batch size 32.
- menggunakan model IndoBERT Large P2 dengan epoch 2, learning rate 2e-5, dan batch size 64.
- menggunakan model IndoBERT Large P2 dengan epoch 2, learning rate 3e-5, dan batch size 32.
- menggunakan model IndoBERT Large P2 dengan epoch 2, learning rate 3e-5, dan batch size 64.
- menggunakan model IndoBERT Large P2 dengan epoch 3, learning rate 1e-5, dan batch size 32.
- menggunakan model IndoBERT Large P2 dengan epoch 3, learning rate 2e-5, dan batch size 32.
- menggunakan model IndoBERT Large P2 dengan epoch 3, learning rate 2e-5, dan batch size 64.

Setiap selesai pelatihan model, langsung gunakan model untuk memberikan label pada data unlabeled. Hasil labeling disimpan ke dalam file csv karena nantinya hasil csv tersebut akan digunakan untuk voting.

- **Load seluruh data voting**
- **Jalankan kode program yang berfungsi untuk melakukan voting**
- Dikarenakan mungkin nanti bakalan terdapat voting yang seimbang, artinya class yang memiliki frekuensi terbanyak terdapat lebih dari satu, maka data tersebut akan diberikan label oleh model yang memiliki tingkat akurasi tertinggi pada saat pelatihan model. Model tersebut adalah model dengan parameter epoch 3, learning rate 2e-5, dan batch size 64. 
