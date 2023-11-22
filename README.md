# Nama: Surya Raavi Adiputra 
# NPM: 2206082404

# Tugas 9

## 1. Apakah bisa kita melakukan pengambilan data JSON tanpa membuat model terlebih dahulu? Jika iya, apakah hal tersebut lebih baik daripada membuat model sebelum melakukan pengambilan data JSON?
:
  Kita tetap bisa melakukan pengambilan data JSON tanpa membuat model terlebih dahulu. Akan tetapi, dalam pengambilan data JSON, disarankan membuat model terlebih dahulu karena dengan adanya model kita bisa melakukan modifikasi data JSON berdasarkan atribut yang sudah didefinisikan di model, membuat data yang kita gunakan lebih konsisten, dan meningkatkan keamanan dan validasi data JSON yang tidak sesuai model atau mengandung kesalahan sintaks.

## 2. Jelaskan fungsi dari CookieRequest dan jelaskan mengapa instance CookieRequest perlu untuk dibagikan ke semua komponen di aplikasi Flutter.
:
  CookieRequest berfungsi untuk mengirim permintaan HTTP yang melampirkan cookie di dalamnya sehingga dengan adanya CookieRequest ini, kita bisa mengirim cookie ke sesama server setiap kali melakukan permintaan HTTP, tanpa harus login lagi. Instance CookieRequest perlu untuk dibagikan ke semua komponen di aplikasi Flutter karena kita mungkin perlu mengakses data yang sama dari server di berbagai halaman atau fitur aplikasi. Jika kita tidak membagikan instance CookieRequest, kita harus membuat instance baru setiap kali kita ingin mengirim permintaan HTTP dengan cookie yang mana akan memakan banyak memori dan mengurangi kinerja aplikasi. 

## 3. Jelaskan mekanisme pengambilan data dari JSON hingga dapat ditampilkan pada Flutter.
:
  Mekanisme pengambilan data dari JSON untuk ditampilkan di flutter sebagai berikut.
  1. Membuat sebuah permintaan HTTP (Hypertext Transfer Protocol) ke sebuah API (Application Programming Interface) endpoint yang menyediakan data JSON. Dalam hal ini, karena kita ingin mengambil data dari JSON, kita akan menggunakan method GET.
  2. Menerima sebuah respons HTTP dari server yang berisi data JSON. Respons HTTP adalah sebuah cara untuk mengirimkan data dari server ke aplikasi, yang memiliki beberapa komponen seperti status code, header, dan body. Secara umum, informasi yang ingin kita ambil berada pada body.
  3. Mengurai atau mem-parsing data JSON menjadi sebuah objek atau struktur data Dart yang dapat kita manipulasi dan tampilkan di aplikasi Flutter. Sebelum melakukan parsing data JSON ke struktur data dart, kita harus melakukan generate struktrur data JSON terlebih dahulu yang bisa dilakukan secara manual atau melalui web yang bisa otomatis menghasilkan kode konversi data JSON ke struktur data Dart, seperti quicktype. Setelah itu, kode yang sudah kita salin dari quicktype, dilampirkan pada file baru yang khusus untuk mengambil data unntuk nantinya bisa diproses oleh flutter.
  4. Menampilkan data JSON yang sudah diurai ke dalam widget Flutter yang sesuai dengan kebutuhan kita. Widget dapat dibuat dengan menggunakan konstruktor bawaan dari Flutter, misalnya Text, Image, RaisedButton, Column, dan lain-lain. 

## 4. Jelaskan mekanisme autentikasi dari input data akun pada Flutter ke Django hingga selesainya proses autentikasi oleh Django dan tampilnya menu pada Flutter.
:
  Mekanisme autentikasi dari input data akun pada Flutter ke Django dapat dilakukan melalui tahapan berikut.
  1. Membuat sebuah form Login di Flutter yang memungkinkan pengguna untuk memasukkan data akun seperti username dan password. 
  2. Membuat sebuah fungsi Login di Flutter yang bertugas untuk mengirim data akun dari form Login ke Django melalui permintaan HTTP POST. Fungsi Login juga bertugas untuk menerima respons HTTP dari Django yang berisi status dan hasil dari autentikasi.
  3. Membuat sebuah view Login di Django yang bertugas untuk menerima data akun dari Flutter melalui permintaan HTTP POST. View Login akan mengatur logika bisnis dari aplikasi web, seperti mengambil, memproses, dan mengembalikan data, serta memeriksa data akun dengan menggunakan fungsi authenticate yang disediakan oleh Django, yang akan membandingkan data akun dengan data yang tersimpan di database.
  4. Membuat sebuah respons HTTP di Django yang bertugas untuk mengirim status dan hasil dari autentikasi ke Flutter. Respons HTTP adalah sebuah cara untuk mengirim data dari server ke aplikasi, yang memiliki beberapa komponen seperti status code, header, dan body. Status code adalah sebuah angka yang menunjukkan hasil dari permintaan HTTP, misalnya 200 berarti sukses, 401 berarti tidak terotentikasi, dan 403 berarti tidak memiliki izin. Header adalah sebuah informasi tambahan yang menyertai respons HTTP, misalnya Content-Type, Content-Length, dan Set-Cookie. Body adalah sebuah bagian utama dari respons HTTP yang berisi data yang kita kirim, dalam hal ini status dan hasil dari autentikasi.
  5. Membuat sebuah fungsi Navigate di Flutter yang bertugas untuk mengarahkan pengguna ke halaman atau menu yang sesuai dengan hasil dari autentikasi. Fungsi Navigate juga bertugas untuk menampilkan pesan atau notifikasi yang sesuai dengan hasil dari autentikasi, misalnya menggunakan widget SnackBar atau AlertDialog.

## 5. Sebutkan seluruh widget yang kamu pakai pada tugas ini dan jelaskan fungsinya masing-masing.
  1. Widget dalam file list_product.dart
    - MaterialApp: Widget utama yang mengonfigurasi pengaturan tertinggi untuk aplikasi Flutter.
    - Scaffold: Mengimplementasikan struktur visual dasar desain material dengan memberikan kerangka kerja untuk AppBar, Drawer, BottomNavigationBar, FloatingActionButton, dan Body.
    - AppBar: Mewakili bilah atas aplikasi yang memiliki judul "Product".
    - Drawer: Digunakan untuk kostum left drawer.
    - LeftDrawer: Widget kustom (tidak diberikan dalam potongan kode) yang mungkin menentukan konten dari menu samping.
    - FutureBuilder: Digunakan untuk secara asinkron mengambil data produk dari internet.
    - Center: Digunakan ketika data masih dimuat untuk menampilkan CircularProgressIndicator.
    - ListView.builder: Digunakan untuk menampilkan daftar produk.
    - Container: Digunakan untuk membuat wadah untuk setiap produk dalam daftar.
    - Column: Digunakan untuk mengatur informasi produk (nama, harga, deskripsi, dan jumlah) secara vertikal.
    - Text: Digunakan untuk menampilkan detail produk seperti nama, harga, deskripsi, dan jumlah.
    - SizedBox: Digunakan untuk menambahkan ruang antara berbagai informasi.
    - CircularProgressIndicator: Widget yang menunjukkan lingkaran berputar/buffering yang mengindikasikan bahwa aplikasi sedang sibuk.
    - TextStyle: Mendefinisikan gaya untuk teks, warna, ukuran font, dan ketebalan font.
  2. Widget dalam file login.dart
    - MaterialApp: Widget utama yang mengonfigurasi pengaturan tertinggi untuk aplikasi Flutter.
    - AppBar: Digunakan untuk menampilkan judul "Login".
    - TextField: Digunakan untuk input username dan password dari user.
    - ElevatedButton: Tombol untuk melakukan proses login. Ketika tombol ditekan, akan memeriksa kredensial, memproses respons, dan menavigasi pengguna ke halaman utama (MyHomePage) jika login berhasil.
    - onPressed (pada ElevatedButton): Logika yang dijalankan saat tombol login ditekan. Ini mengambil nilai dari controller username dan password, memeriksa kredensial dengan menggunakan CookieRequest, dan menangani respons sesuai dengan keberhasilan atau kegagalan login.
    - AlertDialog: Digunakan untuk menampilkan pesan kesalahan.
  3. Widget dalam file menu.dart
    - Scaffold: Digunakan untuk menyediakan struktur dasar aplikasi Flutter, termasuk app bar, drawer, dan body.
    - AppBar: Digunakan untuk mendefinisikan bilah judul aplikasi, yang biasanya menyertakan judul, ikon leading (misalnya, untuk navigasi kembali), dan tindakan (misalnya, untuk menambahkan item baru).
    - LeftDrawer: Digunakan sebagai widget kustom yang mengimplementasikan drawer yang rata kiri dengan daftar item.
    - SingleChildScrollView: Digunakan untuk membungkus widget anak dan memungkinkannya untuk menggulir secara vertikal jika kontennya melebihi ruang yang tersedia.
    - Padding: Digunakan untuk menambahkan padding di sekitar widget anak.
    - Column: Widget ini mengatur anak-anaknya secara vertikal, satu di bawah yang lain.
    - Text: Digunakan untuk menampilkan teks dengan properti yang dapat dikonfigurasi seperti ukuran font, berat, dan perataan.
    - GridView.count: Digunakan untuk mengatur anak-anaknya dalam pola grid dengan jumlah kolom yang ditentukan.
    - ShopCard: Digunakan untuk menampilkan nama, ikon, dan warna item, dan merespons ketukan dengan menavigasi ke layar ShopListForm.
    - ShopItem: Digunakan untuk menyimpan nama, ikon, dan warna item.
    - ProductData: Digunakan untuk menyimpan informasi tentang produk yang dipilih saat ini yang mencakup atribut nama produk, harga, jumlah, dan deskripsi.
  4. Widget dalam file shoplist_form.dart
    - Scaffold: Digunakan untuk mengatur struktur dasar aplikasi, dengan app bar di atas, drawer di sisi kiri, dan body di tengah.
    - AppBar: Digunakan untuk menampilkan judul aplikasi, ikon menu, dan ikon untuk menambahkan produk baru.
    - Form: Digunakan untuk mengumpulkan input untuk nama produk, harga, jumlah, dan deskripsi.
    - SingleChildScrollView: Digunakan untuk memungkinkan pengguna menggulir melalui form.
    - Column:  Digunakan untuk mengatur bidang formulir dan tombol "Simpan".
    - Padding: Digunakan untuk menambahkan ruang di sekitar bidang formulir dan tombol "Simpan".
    - TextFormField: Digunakan untuk mengumpulkan input untuk nama produk, harga, jumlah, dan deskripsi.
    - ElevatedButton: Digunakan untuk membuat tombol "Simpan" yang mengirimkan data formulir ke server.
    - SnackBar: Digunakan untuk menampilkan pesan yang menunjukkan apakah produk berhasil disimpan atau jika ada kesalahan.
  5. Widget dalam file left_drawer.dart
    - Drawer: digunakan untuk menyediakan menu navigasi dengan tautan ke halaman beranda, halaman tambah produk, dan halaman daftar produk.
    - ListView: Digunakan untuk menampilkan item menu navigasi di dalam widget Drawer.
    - DrawerHeader: Digunakan untuk membuat header dengan latar belakang biru, logo TeknoLand, dan deskripsi aplikasi.
    - ListTile: Digunakan untuk membuat item menu navigasi di dalam widget Drawer. Setiap widget ListTile memiliki ikon leading, judul yang mewakili opsi navigasi, dan callback onTap yang menangani navigasi saat item ditekan.
    - Text: digunakan untuk menampilkan logo TeknoLand, deskripsi aplikasi, dan judul item menu navigasi.
    - Icon: Digunakan untuk menampilkan ikon leading untuk item menu navigasi.
    - Padding: Digunakan untuk menambahkan padding di sekitar deskripsi aplikasi di dalam widget DrawerHeader.
  6. Widget dalam file shop_card.dart
    - Material: Digunakan untuk memberikan latar belakang berwarna untuk kartu belanja.
    - InkWell: Digunakan untuk membuat kartu belanja merespons ketukan. Saat kartu belanja diketuk, callback onTap dipanggil.
    - Container: Digunakan untuk menambahkan padding pada ikon dan teks dalam kartu belanja.
    - Center: Digunakan untuk memusatkan ikon dan teks dalam kartu belanja.
    - Column: Digunakan untuk mengatur ikon dan teks dalam kartu belanja.
    - Icon: Digunakan untuk menampilkan ikon untuk item kartu belanja.
    - Text: Digunakan untuk menampilkan nama item kartu belanja.
    - Padding: Digunakan untuk menambahkan padding di antara ikon dan teks dalam kartu belanja.
  7. Widget dalam file main.dart
    - Provider: Digunakan untuk menyediakan objek CookieRequest ke seluruh pohon widget sehingga widget apa pun di aplikasi dapat mengakses objek CookieRequest menggunakan metode context.watch().
    - MaterialApp: Digunakan untuk mendefinisikan judul, tema, dan halaman beranda aplikasi.
    - LoginPage: Digunakan untuk menampilkan layar login dengan mengumpulkan kredensial login pengguna dan mengirimkannya ke server.

## 5.  Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step! 
:
  Secara keseluruhan, implementasi checklist diatas sesuai dengan tutorial, tetapi ada beberapa hal yang saya tambahkan pada file product.dart dan shoplist_dart dimana saya menambahkan atribut amount/jumlah produk dengan tampilan seperti dibawah ini.
  - File product.dart
    Fields({
      required this.user,
      required this.name,
      required this.amount,
      required this.description,
      required this.price,
    });
    factory Fields.fromJson(Map<String, dynamic> json) => Fields(
      user: json["user"],
      name: json["name"],
      amount: json["amount"],
      description: json["description"],
      price: json["price"],
    );
  - File shoplist_form.dart
    onPressed: () async {
    if (_formKey.currentState!.validate()) {
      // Kirim ke Django dan tunggu respons
      // TODO: Ganti URL dan jangan lupa tambahkan trailing slash (/) di akhir URL!
      final response = await request.postJson(
          "http://127.0.0.1:8000/create-flutter/",
          jsonEncode(<String, String>{
            'name': _name,
            'price': _price.toString(),
            'description': _description,
            'amount': _amount.toString(),
            // TODO: Sesuaikan field data sesuai dengan aplikasimu
          }));
          ...
      }
      ...
    }  



# Tugas 8

## 1. Jelaskan perbedaan antara Navigator.push() dan Navigator.pushReplacement(), disertai dengan contoh mengenai penggunaan kedua metode tersebut yang tepat!
: 
  Dalam Flutter, Navigator.push() dan Navigator.pushReplacement() adalah dua metode yang digunakan untuk menavigasi ke layar baru. Perbedaan utama antara keduanya adalah bahwa Navigator.push() menambahkan rute baru ke dalam tumpukan rute, sedangkan Navigator.pushReplacement() mengganti rute teratas dalam tumpukan rute dengan rute baru. 
  - Contoh implementasi Navigator.push(): 
    Navigator.push(
      context,
      MaterialPageRoute(builder: (context) => SecondScreen()),
    );
  - Contoh implementasi Navigator.pushReplacement():
    Navigator.pushReplacement(
      context,
      MaterialPageRoute(builder: (context) => SecondScreen()),
    );

## 2. Jelaskan masing-masing layout widget pada Flutter dan konteks penggunaannya masing-masing!
:
  - Container: Widget ini digunakan untuk mengatur tampilan widget lainnya. Container  dapat digunakan untuk mengatur margin, padding, warna, dan sebagainya. Container juga dapat digunakan untuk mengatur ukuran widget lainnya.
  - Row: Widget ini digunakan untuk mengatur widget secara horizontal. Row dapat digunakan untuk mengatur susunan tombol, teks, dan sebagainya.
  - Column: Widget ini digunakan untuk mengatur widget secara vertikal. Column dapat digunakan untuk mengatur susunan tombol, teks, dan sebagainya.
  - Stack: Widget ini digunakan untuk mengatur widget secara tumpukan. Stack dapat digunakan untuk menumpuk widget seperti gambar, teks, dan sebagainya.
  - Expanded: Widget ini digunakan untuk mengisi ruang kosong dalam layout. Expanded dapat digunakan untuk mengisi ruang kosong dalam Row atau Column.
  - ListView: Widget ini digunakan untuk menampilkan daftar widget dalam bentuk scrollable. ListView dapat digunakan untuk menampilkan daftar teks, gambar, dan sebagainya.
  - GridView: Widget ini digunakan untuk menampilkan daftar widget dalam bentuk grid. GridView dapat digunakan untuk menampilkan daftar gambar, teks, dan sebagainya.
  - Wrap: Widget ini digunakan untuk mengatur widget dalam bentuk wrap. Wrap dapat digunakan untuk mengatur susunan tombol, teks, dan sebagainya.
  - SizedBox: Widget ini digunakan untuk mengatur ukuran widget. SizedBox dapat digunakan untuk mengatur ukuran lebar dan tinggi widget.
  - AspectRatio: Widget ini digunakan untuk mengatur rasio aspek widget. AspectRatio dapat digunakan untuk mengatur rasio aspek gambar, video, dan sebagainya.

## 3. Sebutkan apa saja elemen input pada form yang kamu pakai pada tugas kali ini dan jelaskan mengapa kamu menggunakan elemen input tersebut!
:
  Dalam tugas ini, saya menggunakan TextFormField sebagai elemen input untuk menerima input dari pengguna. Implementasi TextFormField ini saya gunakan untuk mengambil masukan nama, harga, jumlah, dan deskripsi produk dari user dalam file shoplist_form.dart. Di dalam TextFormField, saya juga mendefinisikan beberapa elemen lain, yaitu InputDecoration untuk memberikan atribut tambahan pada field input dan OutlineInputBorder untuk mengatur border field input.

## 4. Bagaimana penerapan clean architecture pada aplikasi Flutter?
:
  Clean Architecture adalah suatu konsep arsitektur perangkat lunak yang bertujuan untuk memisahkan konsep bisnis (domain logic) dari detail teknis, seperti antarmuka pengguna dan penyimpanan data. Dalam konteks Flutter, penerapan Clean Architecture dapat melibatkan pemisahan kode ke dalam lapisan-lapisan utama domain layer (lapisan inti yang berisi logika bisnis atau aturan domain), data layer (lapisan yang bertanggung jawab untuk mengakses dan menyimpan data), dan presentation layer (lapisan yang menangani interaksi pengguna).

## 5. Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step!
:
  - Implementasi Navigator.push() dan Navigator.pushReplacement()
    Navigator.push() digunakan untuk menambahkan rute baru pada stack berdasarkan context yang diambil dimana nantinya tampilan akan berubah sesuai tampilan rute tersebut. Contohnya, dalam tugas ini, saya menerapkan perintah di bawah ini dalam file shop_card.dart untuk menambahkan rute baru pada stack dan mengubah halaman ke halaman yang didefinisikan di kelas ShopFormPage.
    if (item.name == "Tambah Produk") {
            Navigator.push(context,
                MaterialPageRoute(builder: (context) => const ShopFormPage()));
    }
    Sementara itu, untuk implmentasi Navigator.pushReplacement digunakan untuk mengganti rute teratas dari stack dengan rute baru. Contohnya, dalam tugas ini, saya menerapkan perintah di bawah ini dalam file left_drawer.dart untuk mengganti rute teratas atau rute halaman saat ini dengan rute baru dengan tampilan yang didefinisikan di kelas MyHomePage. 
    onTap: () {
      Navigator.pushReplacement(
          context,
          MaterialPageRoute(
            builder: (context) => MyHomePage(),
          )
      );
    },
  - Implementasi layout widget
    Dalam tugas ini, saya menggunakan beberapa layout widget, yaitu:
    1. Column
       child: Column(
                crossAxisAlignment: CrossAxisAlignment.start,
                children: [
                  Padding(
                    padding: const EdgeInsets.all(8.0),
                    child: TextFormField(
                      decoration: InputDecoration(
                        hintText: "Nama Produk",
                        labelText: "Nama Produk",
                        border: OutlineInputBorder(
                          borderRadius: BorderRadius.circular(5.0),
                        ),
                      ),
                      onChanged: (String? value) {
                        setState(() {
                          _name = value!;
                        });
                      },
                      validator: (String? value) {
                        if (value == null || value.isEmpty) {
                          return "Nama tidak boleh kosong!";
                        }
                        return null;
                      },
                    ),
                  ),
                ]
              )
        Implementasi layout Column dalam file shoplist_form.dart tersebut digunakan untuk mengatur elemen child di dalamnya secara vertikal.
    2. Allign
       Align(
            alignment: Alignment.bottomCenter,
            child: Padding(
              padding: const EdgeInsets.all(8.0),
              child: ElevatedButton(
                style: ButtonStyle(
                  backgroundColor:
                  MaterialStateProperty.all(Colors.indigo),
                ),
              )
            )
        ......
       )
       Implementasi layout Align dalam file shoplist_form.dart digunakan untuk mengatur letak elemen child relatif dengan parent widgetnya.
    3. ListTile
       ListTile(
            leading: const Icon(Icons.home_outlined),
            title: const Text('Halaman Utama'),
            // Bagian redirection ke MyHomePage
            onTap: () {
              Navigator.pushReplacement(
                  context,
                  MaterialPageRoute(
                    builder: (context) => MyHomePage(),
                  ));
            },
          ),
          ListTile(
            leading: const Icon(Icons.add_shopping_cart),
            title: const Text('Tambah Produk'),
            // Bagian redirection ke ShopFormPage
            onTap: () {
              Navigator.pushReplacement(
                  context,
                  MaterialPageRoute(
                    builder: (context) => MyHomePage(),
                  ));
            },
          ),
       Implementasi ListTile dalam file left_drawer.dart digunakan untuk membuat baris Halaman Utama yang berisi teks "Halaman Utama" beserta ikonnya dan Tambah Produk yang berisi teks "Tambah Produk" beserta ikonnya.
    4. GridView
        GridView.count(
          // Container pada card kita.
          primary: true,
          padding: const EdgeInsets.all(20),
          crossAxisSpacing: 10,
          mainAxisSpacing: 10,
          crossAxisCount: 3,
          shrinkWrap: true,
          children: items.map((ShopItem item) {
            // Iterasi untuk setiap item
            return ShopCard(item);
          }).toList(),
          ...
        )
        Implementasi GridView pada file menu.dart digunakan untuk mengatur posisi elemen-elemen Lihat Produk, Tambah Produk, dan Logout dalam bentuk grid.
  - Implementasi elemen input pada file form
    TextFormField(
      decoration: InputDecoration(
        hintText: "Nama Produk",
        labelText: "Nama Produk",
        border: OutlineInputBorder(
          borderRadius: BorderRadius.circular(5.0),
        ),
      ),
    )
    Implementasi elemen input yang digunakan dalam file shoplist_form.dart adalah TextFormField yang mana dalam file tersebut saya juga mendefinisikan beberapa labelText, seperti harga produk, jumlah produk, dan deskripsi produk.
  - Implementasi clean architecture
    Dalam tugas ini, saya mengimplementasikan clean architecture dengan melakukan pemisahan kode dengan membuat beberapa file untuk meningkatkan readibility dan modularity. Contoh clean architecture yang saya terapkan dalam tugas ini, seperti dengan memindahkan class ShopCard dari file menu.dart ke sebuah file baru bernama shop_card.dart yang mana nantinya file menu.dart akan berperan sebagai lapisan domain, sedangkan ShopCard berperan sebagai lapisan presentasi untuk mengatur halaman yang akan ditampilkan selanjutnya ketika user melakukan aksi. Tidak hanya itu, terdapat juga file shoplist_form.dart sebagai lapisan presentasi yang berperan untuk menampilkan form penambahan produk.

# Tugas 7

## 1. Apa perbedaan utama antara stateless dan stateful widget dalam konteks pengembangan aplikasi Flutter?
: 
  - Stateless widget adalah sebuah keadaan dimana widget dalam keadaan yang statis,
    sedangkan stateful widget adalah sebuah keadaan dimana widget dalam keadaan yang dapat berubah-ubah. Keadaan (state) adalah kumpulan nilai atau data yang mengatur perilaku dari widget.
  - Dalam implementasinya, stateless widget memiliki satu objek yang mewakili widget
    widget tersebut, sedangkan stateful widget memiliki dua objek, yaitu objek StatefulWidget itu sendiri dan objek State yang mengatur perilaku widget itu.
  - Stateless widget hanya memiliki satu method yang wajib diimplementasikan, yaitu method 
    build yangmengembalikan widget yang akan ditampilkan dimana method ini ditampilkan sekali saat widget pertama kali dimuat dan tidak akan dipanggil lagi, kecuali ada perubahan konfigurasi. Sementara itu, stateful widget memiliki beberapa method siklus hidup (lifecycle) yang dapat diimplementasikan, seperti initState, didUpdateWidget, setState, dan dispose dimana method-method ini dipanggil saat terjadi perubahan keadaan widget.
  - Stateless widget cocok digunakan untuk widget yang sifatnya statis atau tidak  
    memerlukan perubahan nilai, seperti teks, ikon, atau gambar. Sementara itu, stateful widget cocok digunakan untuk widget yang sifatnya dinamis atau memerlukan perubahan nilai, seperti button, radiobutton, dan slider.

## 2. Sebutkan seluruh widget yang kamu gunakan untuk menyelesaikan tugas ini dan jelaskan fungsinya masing-masing.
: 
  - StatelessWidget: Widget ini adalah widget yang bersifat statis. Widget ini hanya 
    memiliki satu metode yang wajib diimplementasikan, yaitu metode build, yang mengembalikan widget yang akan ditampilkan. Widget ini cocok digunakan untuk widget yang sifatnya statis atau tidak memerlukan perubahan nilai, seperti teks, ikon, atau gambar, seperti widget yang ada pada class MyHomePage dan ShopCard.
  - Scaffold: Widget ini adalah widget yang menyediakan kerangka dasar untuk membuat 
    tampilan aplikasi. Widget ini memiliki beberapa properti yang dapat digunakan untuk menentukan bagian-bagian dari tampilan, seperti appBar, body, drawer, floatingActionButton, dan bottomNavigationBar. Widget ini cocok digunakan untuk widget yang menjadi kontainer utama dari halaman aplikasi. Class yang menggunakan widget ini adalah MyHomePage.
  - AppBar: Widget ini adalah widget yang menyediakan toolbar atau panel atas untuk 
    halaman aplikasi. Widget ini memiliki beberapa properti yang dapat digunakan untuk menentukan tampilan dan fungsi dari toolbar, seperti title, leading, actions, backgroundColor, dan elevation. Widget ini cocok digunakan untuk widget yang menampilkan judul, menu, atau tombol pada bagian atas halaman aplikasi. Class yang menggunakan AppBar adalah MyHomePage.
  - SingleChildScrollView: Widget ini adalah widget yang dapat membuat konten yang terlalu 
    panjang untuk ditampilkan dalam satu layar menjadi dapat discroll. Widget ini memiliki satu properti yang wajib diisi, yaitu child, yang merupakan widget yang akan ditampilkan dalam mode scrollable. Widget ini cocok digunakan untuk widget yang memiliki konten yang melebihi ukuran layar, seperti teks, gambar, atau form. Class yang menggunakan SingleChildScrollView adalah MyHomePage.
  - Padding: Widget ini adalah widget yang dapat memberikan jarak atau ruang kosong antara 
    widget dengan widget lainnya. Widget ini memiliki dua properti yang wajib diisi, yaitu padding, yang merupakan nilai jarak yang diinginkan, dan child, yang merupakan widget yang akan diberi jarak. Widget ini cocok digunakan untuk widget yang ingin menambahkan margin atau spacing pada konten, seperti teks, gambar, atau tombol. Class yang menggunakan Padding adalah MyHomePage dan ShopCard.
  - Column: Widget ini adalah widget yang dapat menampilkan beberapa widget secara 
    vertikal. Widget ini memiliki satu properti yang wajib diisi, yaitu children, yang merupakan daftar widget yang akan ditampilkan. Widget ini juga memiliki beberapa properti yang dapat digunakan untuk menentukan tata letak dan penyesuaian dari widget, seperti mainAxisAlignment, crossAxisAlignment, mainAxisSize, dan verticalDirection. Widget ini cocok digunakan untuk widget yang ingin menampilkan konten dalam bentuk kolom, seperti teks, gambar, atau form. Class yang menggunakan Column adalah MyHomePage dan ShopCard.
  - Text: Widget ini adalah widget yang dapat menampilkan teks pada layar. Widget ini 
    memiliki satu properti yang wajib diisi, yaitu data, yang merupakan teks yang akan ditampilkan. Widget ini juga memiliki beberapa properti yang dapat digunakan untuk menentukan tampilan dan gaya dari teks, seperti textAlign, style, maxLines, dan overflow. Widget ini cocok digunakan untuk widget yang ingin menampilkan informasi dalam bentuk teks, seperti judul, label, atau pesan. Class yang menggunakan Text adalah MyHomePage dan ShopCard.
  - GridView: Widget ini adalah widget yang dapat menampilkan beberapa widget dalam bentuk 
    grid atau kisi-kisi. Widget ini memiliki beberapa properti yang dapat digunakan untuk menentukan tampilan dan fungsi dari grid, seperti children, gridDelegate, crossAxisCount, crossAxisSpacing, mainAxisSpacing, shrinkWrap, dan primary. Widget ini cocok digunakan untuk widget yang ingin menampilkan konten dalam bentuk grid, seperti gambar, kartu, atau tombol. Class yang menggunakan GridView adalah MyHomePage.
  - Material: Widget ini adalah widget yang menyediakan efek visual yang sesuai dengan 
    konsep material design. Widget ini memiliki beberapa properti yang dapat digunakan untuk menentukan tampilan dan fungsi dari material, seperti color, elevation, shape, clipBehavior, dan animationDuration. Widget ini cocok digunakan untuk widget yang ingin menambahkan efek visual seperti bayangan, bentuk, atau warna pada konten, seperti gambar, kartu, atau tombol. Class yang menggunakan Material adalah ShopCard.
  - InkWell: Widget ini adalah widget yang dapat membuat area yang responsive terhadap 
    sentuhan. Widget ini memiliki beberapa properti yang dapat digunakan untuk menentukan tampilan dan fungsi dari area sentuhan, seperti child, onTap, onLongPress, splashColor, highlightColor, dan radius. Widget ini cocok digunakan untuk widget yang ingin menambahkan efek visual dan interaksi pada konten, seperti gambar, kartu, atau tombol. Class yang menggunakan InkWell adalah ShopCard.
  - Container: Widget ini adalah widget yang dapat menjadi kontainer atau wadah untuk 
    widget lainnya. Widget ini memiliki beberapa pr operti yang dapat digunakan untuk menentukan tampilan dan fungsi dari kontainer, seperti child, padding, margin, decoration, alignment, width, height, dan constraints. Widget ini cocok digunakan untuk widget yang ingin menyesuaikan ukuran, posisi, atau dekorasi dari konten, seperti teks, gambar, atau form. Class yang menggunakan Container adalah ShopCard.
  - Icon: Widget ini adalah widget yang dapat menampilkan ikon atau simbol pada layar. 
    Widget ini memiliki satu properti yang wajib diisi, yaitu icon, yang merupakan ikon yang akan ditampilkan. Widget ini juga memiliki beberapa properti yang dapat digunakan untuk menentukan tampilan dan gaya dari ikon, seperti size, color, semanticLabel, dan textDirection. Widget ini cocok digunakan untuk widget yang ingin menampilkan ikon yang merepresentasikan fungsi atau informasi, seperti menu, tombol, atau label. Class yang menggunakan Icon adalah ShopCard.
  - MaterialApp: Widget ini berfungsi untuk membungkus sejumlah widget lain yang umumnya 
    dibutuhkan untuk aplikasi yang menggunakan Material Design. Dalam widget ini, didefinisikan beberapa properti, yaitu title yang berfungsi untuk memberi judul aplikasi, theme yang berfungsi untuk memberikan tema yang digunakan pada aplikasi, seperti warna, font, dan ukuran teks, dan home yang berfungsi untuk menentukan widget yang akan ditampilkan pada rute default aplikasi, yaitu ./ dimana widget yang digunakan adalah widget yang didefinisikan pada class MyHomePage. Implementasi widget ini terletak pada file main.dart.

## 3. Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step (bukan hanya sekadar mengikuti tutorial).
: 
  - Instalasi flutter dan android studio serta melakukan konfigurasi pada aplikasi  
    yang sudah diinstal sesuai tutorial.
  - Pembuatan direktori baru untuk menyimpan proyek flutter bernama TeknoLand_mobile dan 
    pembuatan proyek flutter baru dengan nama teknoland melalui terminal di direktori TeknoLand_mobile dengan perintah flutter create teknoland.
  - Pembuatan repositori baru di github dan menghubungkan dengan proyek flutter yang sudah 
    dibuat sebelumnya.
  - Modifikasi file main.dart dan membuat file menu.dart pada direktori teknoland/lib 
    sesuai pada tutorial. Dalam mengintegrasikan warna yang berbeda pada button Lihat Item, Tambah Item, dan Logout, dilakukan dengan membuat atribut baru pada class ShopItem pada file menu.dart yang bernama color dengan tipe Color. Setelah itu, menambahkan paramater color pada objek ShopItems pada variabel items di class MyHomePage dan mengubah nilai dari objek color di class ShopCard pada widget Material menjadi item.color.
  - Untuk mengetahui bagaimana tampilan aplikasinya, bisa dilakukan dengan perintah 
    flutter run pada direktori proyek teknoland di terminal.
