# **Jenis Jenis Method**

## **1. Instance Method**
Penjelasan:

-> Instance method adalah method yang terikat pada objek dari suatu class.
-> Untuk memanggil instance method, kita harus membuat objek dari class terlebih dahulu.
-> Instance method bisa memiliki akses langsung ke atribut class yang tidak bersifat static.

```java
// Class Komputer dengan Instance Method
public class Komputer {
    String jenis; // Atribut instance
    String merk;

    // Instance Method
    public void tampilkanInfo() {
        System.out.println("Jenis Komputer: " + jenis);
        System.out.println("Merk: " + merk);
    }

    public static void main(String[] args) {
        Komputer myKom = new Komputer(); // Membuat objek
        myKom.jenis = "Laptop";
        myKom.merk = "Asus";
        myKom.tampilkanInfo(); // Memanggil instance method
    }
}
```

🔹 Catatan:
Instance method tidak menggunakan static karena bergantung pada objek.


---


## **2. Static Method**
Penjelasan:

-> Static method adalah method yang dapat dipanggil tanpa membuat objek terlebih dahulu.
-> Static method ditandai dengan kata kunci static.
-> Tidak bisa mengakses atribut instance secara langsung, kecuali jika menggunakan objek.

```java
// Class dengan Static Method
public class Util {
    // Static Method
    public static void cetakPesan() {
        System.out.println("Ini adalah static method.");
    }

    public static void main(String[] args) {
        // Memanggil static method tanpa objek
        Util.cetakPesan();
    }
}
```

🔹 Catatan:
Static method bisa langsung dipanggil dengan NamaClass.method().


---


## **3. Setter and Getter Method**
Penjelasan:

-> Setter Method → digunakan untuk mengatur nilai atribut private dalam class.
-> Getter Method → digunakan untuk mengambil nilai dari atribut private.
-> Berguna dalam enkapsulasi, karena atribut dibuat private dan hanya bisa diakses melalui method.

```java
// Class dengan Setter dan Getter
public class Komputer {
    private String jenis;
    private String merk;

    // Setter Method
    public void setDataKomputer(String jenis, String merk) {
        this.jenis = jenis;
        this.merk = merk;
    }

    // Getter Method
    public String getJenis() {
        return jenis;
    }

    public String getMerk() {
        return merk;
    }

    public static void main(String[] args) {
        Komputer myKom = new Komputer();
        myKom.setDataKomputer("Laptop", "MacBook");
        
        System.out.println(myKom.getJenis()); // Output: Laptop
        System.out.println(myKom.getMerk());  // Output: MacBook
    }
}
```

🔹 Catatan:
Getter dan Setter menjaga enkapsulasi, sehingga atribut private tidak bisa diakses langsung dari luar class.


---


## **4. Abstract Method**
Penjelasan:

-> Abstract method adalah method yang dideklarasikan tanpa isi (hanya nama method tanpa implementasi).
-> Hanya bisa dibuat dalam abstract class.
-> Kelas yang mewarisi abstract class harus mengimplementasikan abstract method tersebut.

```java 
// Abstract Class dengan Abstract Method
abstract class Komputer {
    // Abstract Method (tidak memiliki isi)
    abstract void spesifikasi();
}

// Subclass yang mengimplementasikan Abstract Method
class Laptop extends Komputer {
    @Override
    void spesifikasi() {
        System.out.println("Laptop dengan spesifikasi tinggi.");
    }
}

public class Main {
    public static void main(String[] args) {
        Komputer myLaptop = new Laptop();
        myLaptop.spesifikasi(); // Memanggil method yang telah diimplementasikan
    }
}
```

🔹 Catatan:
-> Jika suatu class memiliki abstract method, maka class tersebut harus abstract.
-> Subclass wajib mengimplementasikan method tersebut agar bisa digunakan.