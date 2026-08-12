**TECHNICAL TEST**


**JAVA SPRING BOOT DEVELOPER - MEDIUM LEVEL**


**Framework:** Spring Boot

---

### **General Instructions**

1. Waktu pengerjaan maksimal *(disesuaikan dengan jadwal kandidat)*.


2. Gunakan framework Spring Boot.


3. Implementasi harus menggunakan logic dan pemahaman pribadi kandidat. Menerapkan *SOLID principles* dan *Clean Code* akan menjadi nilai tambah.


4. Tidak diperbolehkan menggunakan starter, template, atau library yang secara langsung menyediakan fitur authentication siap pakai tanpa implementasi kandidat, seperti:


* Starter/template authentication yang menyediakan login dan register siap pakai.


* Boilerplate atau generated project dengan authentication end-to-end siap pakai.


* Library authentication sejenis yang menggantikan implementasi kandidat. (Spring Security diperbolehkan sepanjang konfigurasi dan flow authentication dibuat oleh kandidat).




5. Kandidat diperbolehkan menggunakan dokumentasi resmi sebagai referensi.


6. Pastikan project dapat dijalankan dan diuji setelah selesai.


7. Prioritaskan functionality, code structure, clean code, dan best practice.



### **Tugas**

Buat aplikasi **User Management berbasis RESTful API** (Pengembangan tingkat lanjut) yang mencakup fitur:

* User & Role Management (Role: ADMIN, USER)
* Login (dengan JWT Authentication)


* Register



### **Objectives**

**1. CRUD Operations & Architecture**
Implementasikan fungsi Create, Read, Update, dan Delete (CRUD) untuk User Management dengan menggunakan:

* Spring Data JPA / Hibernate ORM.


* MVC Architecture.


* **(Medium Add-on):** Gunakan *Data Transfer Object (DTO)* untuk memisahkan *Entity* database dengan objek *response/request*.
* **(Medium Add-on):** Implementasikan fitur *Pagination* dan *Sorting* pada saat menampilkan daftar User, serta gunakan skema *Soft Delete* (data tidak benar-benar dihapus dari database, melainkan menggunakan flag seperti `is_deleted`).

**2. Validation & Error Handling**
Implementasikan request validation menggunakan Spring Validation / Jakarta Bean Validation dengan format sebagai berikut:

* a. Jadikan email sebagai Kunci utama (primary key) dalam proses registrasi.


* b. Apabila alamat email sudah terdaftar maka tidak bisa didaftarkan kembali (berikan notifikasinya di form register).


* c. Nama tidak boleh ada karakter selain huruf dan spasi (number dan special character tidak di izinkan).


* d. Nama tidak boleh dimulai dengan karakter selain huruf.


* e. Password minimal 6 karakter.


* f. Password harus terdiri dari Huruf, angka, Huruf Kapital dan Karakter Spesial.


* **(Medium Add-on):** Buatlah *Global Exception Handler* (`@ControllerAdvice`) untuk menangkap error validasi dan mereturn *Response JSON* dengan format baku (misal: memunculkan `message`, `status`, dan detail error validasi).

**3. RESTful API**
Buat dan implementasikan RESTful API endpoints yang dibutuhkan untuk menjalankan fungsi pada aplikasi menggunakan Spring MVC/REST Controller.

* **(Medium Add-on):** Pastikan pengembalian *HTTP Status Code* sesuai standar (misal: 200 OK, 201 Created, 400 Bad Request, 401 Unauthorized, 403 Forbidden). Seluruh response harus dibungkus dalam *Generic Response Wrapper* format JSON.

**4. Database Interactions**
Implementasikan pengelolaan database menggunakan:

* Migration (Flyway/Liquibase atau mekanisme migration yang setara).


* Seeder/initial data (Seeder harus membuat otomatis minimal 1 akun `ADMIN` pada saat aplikasi pertama kali dijalankan).


* Efficient database queries.


* **(Medium Add-on):** Rancang skema relasi *One-to-Many* atau *Many-to-Many* yang tepat antara entitas `User` dan `Role`.

**5. Security & Authorization (Medium Add-on)**

* Gunakan JWT (JSON Web Token) sebagai mekanisme authentikasi.
* Terapkan *Role-Based Access Control (RBAC)*. Endpoint untuk mengambil semua data user (Read All), menambah (Create), mengubah (Update), dan menghapus (Delete) hanya bisa diakses oleh akun dengan role `ADMIN`.
* User dengan role `USER` hanya memiliki akses untuk melihat profilnya sendiri (Read Self) dan mengupdate datanya sendiri (Update Self).

**6. Unit Testing (Medium Add-on)**

* Implementasikan *Unit Testing* minimal untuk bagian *Service Layer* menggunakan **JUnit** dan **Mockito**.

### **Expected Result**

Pada akhir pengerjaan, aplikasi minimal dapat menjalankan:

1. Register User (secara otomatis assign ke role `USER` secara default).


2. Login User (menghasilkan JWT Bearer Token).


3. Menampilkan data User (dengan Pagination & Proteksi khusus ADMIN).


4. Menambahkan data User (Khusus ADMIN).


5. Mengubah data User.


6. Menghapus data User (Soft delete).



### **Submission**

Setelah pengerjaan selesai, kandidat diminta untuk:

1. Mengisi Google Form yang telah dikirimkan melalui email.


2. Menyertakan file README.md, yang berisi:


* a. Langkah-langkah instalasi project dan requirement Java/JDK.


* b. Konfigurasi database.


* c. Cara menjalankan migration dan seeder / initial data.


* d. Cara menjalankan aplikasi.


* e. Informasi endpoint REST API yang telah dibuat (jika ada).


* **(Medium Add-on) f.** Menyertakan file *Postman Collection* (`.json`) yang mencakup semua endpoint yang telah dikembangkan lengkap beserta payload data untuk mempermudah reviewer melakukan testing API.

