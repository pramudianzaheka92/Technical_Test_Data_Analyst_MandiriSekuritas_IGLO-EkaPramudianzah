## Petunjuk Cara Penggunaan sekaligus Menjalankan Beberapa Code Script di dalam Repository ini:

### 1. SQL Query (Google BigQuery):

Agar Query SQL yang tersimpan di dalam repository ini dapat dijalankan, maka kita perlu mempersiapkan akun Google terlebih dahulu. Untuk mempersingkat, saya akan mengasumsikan jika Bapak/Ibu user telah memiliki akun Google dan telah mengetahui Google Cloud Platform. Dikarenakan BigQuery merupakan salah satu services dari Google Cloud Platform, maka kita harus membuka halaman website console Google Cloud melalui link berikut ini:

https://console.cloud.google.com/

Setelah membuka halaman website Google Cloud Platform, Bapak/Ibu dapat mengikuti langkah-langkah di bawah ini:
- Pertama-tama Bapak/Ibu user dapat meng-klik "New Project" serta memberikan nama project yang diinginkan. Setelah nama project telah berhasil dibuat, Bapak/Ibu user dapat klik button "Create" agar project berhasil terbuat di dalam sistem Bapak/Ibu

  <img width="415" height="569" alt="image" src="https://github.com/user-attachments/assets/faa58f6d-5da8-41c3-8b53-9149410c9b64" /> <img width="415" height="417" alt="image" src="https://github.com/user-attachments/assets/ffd3e267-5957-4fa5-bd92-f24fd592374c" />

- Setelah nama project berhasil dibuat, Bapak/Ibu user dapat klik “⋮” yang terdapat di samping kanan dari ID project yang Bapak/Ibu berhasil buat pada langkah pertama. Sebagai informasi tambahan, setiap user akan memiliki ID penamaan project yang berbeda-beda

  <img width="300" height="245" alt="image" src="https://github.com/user-attachments/assets/6bdf25aa-65d6-49b9-91a4-1eef0344308a" />

- Setelah Bapak/Ibu user meng-klik simbol “⋮” yang berada di samping kanan dari ID project Bapak/Ibu, selanjutnya Bapak/Ibu user dapat memberikan nama untuk database yang nantinya akan menyimpan 3 dataset file yaitu "cards_data.csv", "transactions_data.csv" dan "users_data.csv". Setelah Bapak/Ibu user memberikan nama di kolom "Dataset ID" dengan tetap mempertahankan default setting seperti "Location type" dan "Multi region", Bapak/Ibu dapat klik button "Create dataset"

<img width="300" height="724" alt="image" src="https://github.com/user-attachments/assets/643e5d3a-9ec7-43a5-8205-d77f3f51e589" />

- Tahap selanjutnya setelah Bapak/Ibu user telah sukses membuat database di dalam project BigQuery, Bapak/Ibu user sudah mulai dapat membuat table dataset dengan berbagai jenis cara seperti membuat table data dari tahap awal, menggunakan URL dataset yang telah disimpan di dalam Google Drive, meng-upload file dataset yang akan digunakan, dll. Namun menurut saya cara termudah adalah dengan meng-upload file dataset dari penyimpanan internal device kita. Maka dari itu jika ingin meng-upload file dataset ke dalam database yang telah tersimpan di dalam project BigQuery, kita dapat meng-klik simbol “⋮” yang berada di samping nama database => pilih opsi "Create table" kemudian click => Pilih opsi "Upload" pada kolom "Create table from", kemudian select lokasi file yang ingin dianalisis di dalam BigQuery, lalu click "Auto detect" pada Schema

<img width="300" height="43" alt="image" src="https://github.com/user-attachments/assets/e56b083c-5e7a-4820-a8db-0b58c5650a4e" /> => <img width="150" height="302" alt="image" src="https://github.com/user-attachments/assets/700ea483-d163-4964-bc7b-ee9c2c01c7d7" /> => <img width="250" height="771" alt="image" src="https://github.com/user-attachments/assets/aa920209-b145-4c36-8614-78aee8838cb0" />

- Tahap kelima adalah Bapak/Ibu user dapat klik "Create table" agar table yang baru saja di-upload dapat kita gunakan dan analisis di dalam project BigQuery. Jika file dataset yang ingin dianaliss lebih dari 1 data, maka Bapak/Ibu user dapat mengulangi tahap keempat

- Tahap terakhir adalah jika Bapak/Ibu user telah meng-upload file dataset sebanyak yang dibutuhkan (dalam kasus ini, terdapat 3 file dataset yang harus di-upload ke dalam Google BigQuery project yaitu dataset "cards_data.csv", "transactions_data.csv" dan "users_data.csv"), maka Bapak/Ibu user dapat mencoba Query SQL yang telah saya buat yang tersimpan di dalam sebuah file .txt bernama "Data Analyst - Technical Test Query SQL - Eka Pramudianzah.txt"


### 2. Python Notebook (Google Colaboratory)

Salah satu tantangan terbesar dalam menganalisis data di dalam Google BigQuery untuk user yang bukan subscription adalah keterbasan ukuran file dataset yang dapat digunakan. Dikarenakan file dataset "transactions_data.csv" memiliki ukuran yang sangat besar sehingga BigQuery tidak dapat menyimpannya, maka dari itu, saya membuat satu langkah tambahan menggunakan Google Colaboratory untuk memfilter data transaksi. Berikut adalah langkah-langkah yang dapat Bapak/Ibu user gunakan:

- Pertama-tama, Bapak/Ibu user dapat simpan dataset file "transactions_data.csv" di dalam masing-masing folder Google Drive Bapak/Ibu

- Buka service Google Colaboratory. Cara membukanya Bapak/Ibu user dapat melalui Google Drive ataupun langsung mengunjungi halaman website Google Colaboratory melalui URL di bawah ini:
https://colab.research.google.com/
Selain itu, letakkan Google Colaboratory 1 folder yang sama dengan file dataset "transactions_data.csv" yang Bapak/Ibu user simpan di dalam Google Drive

- Import library Pandas & Numpy => baca dataset tersebut ke dalam format DataFrame pandas => filter data berdasarkan tahun transaksi di mana data tahun transaksi diambil dari kolom data "date"

<img width="280" height="79" alt="image" src="https://github.com/user-attachments/assets/a38446ae-339d-44c8-a9ac-c38282d2d850" />


### 3. Looker Data Studio
Untuk membuka desain dashboard yang telah saya buat di dalam Looker Data Studio, Bapak/Ibu user dapat mengunjungi halaman URL yang ada di bawah ini:

https://lookerstudio.google.com/reporting/c52f39a8-2bf7-4039-a828-cb81f9139285
