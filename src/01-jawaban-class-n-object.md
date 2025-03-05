# **SOAL**

## 1. Jelaskan apa yang dimaksud dengan class dan object!

# **JAWABAN :**

**1. Class**
Class adalah sebuah template atau blueprint yang mendefinisikan atribut (variabel) dan perilaku (method) yang dimiliki oleh objek. Class sendiri belum bisa digunakan secara langsung sampai dibuat instansinya dalam bentuk object.

```java
// Definisi class Mobil
class Mobil {
    // Atribut (Properti)
    String merk;
    String warna;

    // Method (Perilaku)
    void tampilkanInfo() {
        System.out.println("Merk: " + merk);
        System.out.println("Warna: " + warna);
    }
}
```

---


**2. Object**
Object adalah instansi nyata dari sebuah class. Saat object dibuat, ia akan memiliki nilai untuk atribut yang ada dalam class tersebut dan bisa menggunakan method yang telah didefinisikan dalam class.

```java
// Program utama untuk membuat object dari class Mobil
public class Main {
    public static void main(String[] args) {
        // Membuat object dari class Mobil
        Mobil mobil1 = new Mobil();
        
        // Memberikan nilai pada atribut mobil1
        mobil1.merk = "Toyota";
        mobil1.warna = "Merah";

        // Memanggil method untuk menampilkan informasi mobil
        mobil1.tampilkanInfo();
    }
}
```

**Penjelasan Kode**

Class "Mobil" dibuat dengan atribut merk dan warna, serta method tampilkanInfo().

Object "mobil1" dibuat dalam method main() menggunakan new Mobil();

Nilai atribut merk dan warna diatur secara langsung.

Method tampilkanInfo() dipanggil untuk menampilkan informasi dari object yang telah dibuat.
