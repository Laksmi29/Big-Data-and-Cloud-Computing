# Big-Data-and-Cloud-Computing

Dalam praktek kali ini, menggunakan layanan Amazon DynamoDB untuk membuat table, mengimport data, menggunakan Query, dan mengekspor hasil.

# **Membuat Sebuah Tabel di DynamoDB**
Setelah masuk akun pada AWS, cari layanan DynamoDB.
![image](https://github.com/Laksmi29/laksmidyah/assets/100764109/9f1394ba-d371-47e6-9d10-23a945fec645)

Pada menu Tables, untuk membuat tabel baru klik "Create table".
![image](https://github.com/Laksmi29/laksmidyah/assets/100764109/0412fa60-cc2a-4106-a239-a6e29390bbcd)

Masukkan nama table, Partition key, dan sort key (optional) yang ingin dibuat.
![image](https://github.com/Laksmi29/laksmidyah/assets/100764109/85ae0cb0-c0c5-4598-b3f4-f8deb4ab94e5)

Pada Table Setting, biarkan pada Default setting. Kemudian klik Create table.
![image](https://github.com/Laksmi29/laksmidyah/assets/100764109/986e5aa1-23d3-45bc-aad6-6b70aae0bd85)

Bila sudah aktif, klik tabel yang sudah dibuat, lalu klik 'Explore". Kemudian, klik pada Create item untuk membuat item yang diperlukan. Jika sudah, klik Create item.
![image](https://github.com/Laksmi29/laksmidyah/assets/100764109/7261e156-f7df-467c-b700-b4193e51d866)

Jika ingin menambah atribut, klik Add new attribute.
![image](https://github.com/Laksmi29/laksmidyah/assets/100764109/df650134-5f00-44b1-a1af-8c912988cdab)

# **Import Data**
Pada menu, pilih "Imports from S3", lalu klik "Import from S3".
![image](https://github.com/Laksmi29/laksmidyah/assets/100764109/09cf6273-c037-417b-ba2f-0e181b9c81e5)

Cari data yang akan digunakan. Klik Broesr S3.
![image](https://github.com/Laksmi29/laksmidyah/assets/100764109/1256025c-8057-49b1-8a39-30e5db3c44a5)
Sebelum itu, pastikan file yang akan digunakan sudah tersimpan pada S3.

Pada Table name, masukkan nama tabel. Pada partition key,  masukkan kolom yang berada pada file tersebut :"Id". Pada Sort key (optional), masukkan: "SepalLengthCM".
![image](https://github.com/Laksmi29/laksmidyah/assets/100764109/92076ca0-1853-401e-87b6-f1c7be363b69)

Pastikan format file sesuai dengan format file yang akan diimport. Klik Next.
![image](https://github.com/Laksmi29/laksmidyah/assets/100764109/6ea1a289-d4f5-43c6-b66c-472c5061086d)
Kemudian klik Import.

Jika sudah sukses, pada menu Tables bisa lihat data yang tadi sudah kita import.
![image](https://github.com/Laksmi29/laksmidyah/assets/100764109/454a00bb-f0bb-44b6-aefa-af531132cfcb)

# **Scan Data**
Scan digunakan untuk mempermudah pencarian informasi.
Pada menu "Explore items" klik file yang sudah diimport. Kemudian, pilih "Scan".
Pada "Select a table or index", biarkan pada file yang tadi. Pada "Select attribut projection", pilih All attributes jika ingin melihat semua atribut.

Bagian Filter:
Pada "Attribute name" pilih Sepal LengthCM dan pada "Type" pilih tipe data yang sesuai dengan atribut. "Condition", pilih Grather than jika ingin melihat data paling tinggi dengan "Value" 5.

Kemudian, klik "Run"
![image](https://github.com/Laksmi29/laksmidyah/assets/100764109/c30f410d-688e-43de-adb7-9ee1e2894fa7)

Berikut hasil scan
![image](https://github.com/Laksmi29/laksmidyah/assets/100764109/b9e4e2bd-74e1-4afe-9b26-8ff712e22b7a)

# **Querying Data**
Pada menu "Explore items" klik file yang sudah diimport. Kemudian, pilih "Query".
Pada "Select a table or index", biarkan pada file yang tadi. Pada "Select attribut projection", pilih All attributes jika ingin melihat semua atribut.
Pada Id, pilih Id pada data. Kemudian klik "Run"
![image](https://github.com/Laksmi29/laksmidyah/assets/100764109/641c5de0-6f41-4514-911b-c1d4599b59b5)

Berikut hasil query
![image](https://github.com/Laksmi29/laksmidyah/assets/100764109/8ce47bc1-1f1b-42c1-adb1-3a5dae5800de)

# **Export Data**
Pilih menu "Export to S3". Lalu, klik "Export to S3"
![image](https://github.com/Laksmi29/laksmidyah/assets/100764109/d32ec2c2-4c14-4571-8db5-3cda9ff5a768)

Pilih tabel yang akan diexport dan tujuan bucket-nya. Kemudian, klik Export
![image](https://github.com/Laksmi29/laksmidyah/assets/100764109/1371c015-14ea-431a-8715-da3549959bb9)

![image](https://github.com/Laksmi29/laksmidyah/assets/100764109/18fc7302-b16e-4e95-bca2-f773ff6a56ec)
Jika sudah sukses, pada S3 bucket akan muncul folder baru hasil export
![image](https://github.com/Laksmi29/laksmidyah/assets/100764109/5113f59f-b455-4d38-9f6e-273f25528e35)
