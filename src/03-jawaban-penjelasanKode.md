# **SOAL**
Berdasarkan gambar berikut ini, jelaskan masing-masing bagian sesuai dengan nomor
yang ada!

# **JAWABAN:**
Jawaban berdasarkan pemahaman saya

1. DEKLARASI CLASS `KOMPUTER`

```java
public class Komputer { → Class Komputer
}
```

Ini adalah class yang menjadi blueprint untuk membuat objek Komputer.
Class ini berisi atribut dan method yang akan digunakan oleh objek.

---

2. ATRIBUT CLASS 

```java
String jenis_komputer; 
    private String merk; 
```

-> jenis_komputer adalah atribut yang dapat diakses secara default.
-> merk adalah atribut dengan modifier private, sehingga hanya bisa diakses dalam class ini.


---


3. Method SETTER untuk mengatur data

```java
public void setDataKomputer(String jenis, String merk) {  
    jenis_komputer = jenis;  
    this.merk = merk; // Keyword 'this' untuk membedakan atribut class dan parameter  
}  
```

-> Method ini menerima dua parameter (jenis dan merk).
-> this.merk = merk; digunakan untuk membedakan antara variabel instance (this.merk) dan parameter merk.


---


4. Method GETTER

```java
public String getJenis() {  
    return jenis_komputer;  
}  

public String getMerk() {  
    return merk;  
}  
```

-> Method ini digunakan untuk mengambil nilai dari jenis_komputer.
-> Method ini mengembalikan nilai dari atribut merk.


---


5. Method MAIN

```java
public static void main(String[] args) {  
    Komputer mykom = new Komputer();  
    mykom.setDataKomputer("LAPTOP", "MACBOOK");  
    System.out.println(mykom.getJenis()); 
    System.out.println(mykom.getMerk());
}  
```

-> main() adalah method utama yang dieksekusi pertama kali saat program dijalankan.
-> Komputer mykom = new Komputer(); membuat objek dari class Komputer.
-> Method ini digunakan untuk memberikan nilai pada atribut jenis_komputer dan merk.
-> getJenis() mengembalikan jenis komputer yang disimpan.
-> getMerk() mengembalikan merk komputer yang telah diatur sebelumnya.