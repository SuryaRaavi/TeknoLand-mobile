Nama: Surya Raavi Adiputra
NPM: 2206082404

## Tugas 7

# 1. Apa perbedaan utama antara stateless dan stateful widget dalam konteks pengembangan aplikasi Flutter?
: - Stateless widget adalah sebuah keadaan dimana widget dalam keadaan yang statis,
    sedangkan stateful widget adalah sebuah keadaan dimana widget dalam keadaan yang dapat berubah-ubah. Keadaan (state) adalah kumpulan nilai atau data yang mengatur perilaku dari widget.
  - Dalam implementasinya, stateless widget memiliki satu objek yang mewakili widget
    widget tersebut, sedangkan stateful widget memiliki dua objek, yaitu objek StatefulWidget itu sendiri dan objek State yang mengatur perilaku widget itu.
  - Stateless widget hanya memiliki satu method yang wajib diimplementasikan, yaitu method 
    build yangmengembalikan widget yang akan ditampilkan dimana method ini ditampilkan sekali saat widget pertama kali dimuat dan tidak akan dipanggil lagi, kecuali ada perubahan konfigurasi. Sementara itu, stateful widget memiliki beberapa method siklus hidup (lifecycle) yang dapat diimplementasikan, seperti initState, didUpdateWidget, setState, dan dispose dimana method-method ini dipanggil saat terjadi perubahan keadaan widget.
  - Stateless widget cocok digunakan untuk widget yang sifatnya statis atau tidak  
    memerlukan perubahan nilai, seperti teks, ikon, atau gambar. Sementara itu, stateful widget cocok digunakan untuk widget yang sifatnya dinamis atau memerlukan perubahan nilai, seperti button, radiobutton, dan slider.

# 2. Sebutkan seluruh widget yang kamu gunakan untuk menyelesaikan tugas ini dan jelaskan fungsinya masing-masing.
: - StatelessWidget: Widget ini adalah widget yang bersifat statis. Widget ini hanya 
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
    widget lainnya. Widget ini memiliki beberapa properti yang dapat digunakan untuk menentukan tampilan dan fungsi dari kontainer, seperti child, padding, margin, decoration, alignment, width, height, dan constraints. Widget ini cocok digunakan untuk widget yang ingin menyesuaikan ukuran, posisi, atau dekorasi dari konten, seperti teks, gambar, atau form. Class yang menggunakan Container adalah ShopCard.
  - Icon: Widget ini adalah widget yang dapat menampilkan ikon atau simbol pada layar. 
    Widget ini memiliki satu properti yang wajib diisi, yaitu icon, yang merupakan ikon yang akan ditampilkan. Widget ini juga memiliki beberapa properti yang dapat digunakan untuk menentukan tampilan dan gaya dari ikon, seperti size, color, semanticLabel, dan textDirection. Widget ini cocok digunakan untuk widget yang ingin menampilkan ikon yang merepresentasikan fungsi atau informasi, seperti menu, tombol, atau label. Class yang menggunakan Icon adalah ShopCard.

# 3. Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step (bukan hanya sekadar mengikuti tutorial).
: - Instalasi flutter dan android studio serta melakukan konfigurasi pada aplikasi  
    yang sudah diinstal sesuai tutorial.
  - Pembuatan direktori baru untuk menyimpan proyek flutter bernama TeknoLand_mobile dan 
    pembuatan proyek flutter baru dengan nama teknoland melalui terminal di direktori TeknoLand_mobile dengan perintah flutter create teknoland.
  - Pembuatan repositori baru di github dan menghubungkan dengan proyek flutter yang sudah 
    dibuat sebelumnya.
  - Modifikasi file main.dart dan membuat file menu.dart pada direktori teknoland/lib 
    sesuai pada tutorial. Dalam mengintegrasikan warna yang berbeda pada button Lihat Item, Tambah Item, dan Logout, dilakukan dengan membuat atribut baru pada class ShopItem pada file menu.dart yang bernama color dengan tipe Color. Setelah itu, menambahkan paramater color pada objek ShopItems pada variabel items di class MyHomePage dan mengubah nilai dari objek color di class ShopCard pada widget Material menjadi item.color.
  - Untuk mengetahui bagaimana tampilan aplikasinya, bisa dilakukan dengan perintah 
    flutter run pada direktori proyek teknoland di terminal.
