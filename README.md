# Lab - 6 - Web

Nama : Ghefira Azka Fardani 

NIM : 312410521

Kelas : TI.24.A5

### 1. container
Membungkus seluruh layout hasil Praktikum 4 ke dalam Bootstrap Container agar lebih rapi dan responsif.

```html
<!-- Sebelumnya -->
<div id="container">

<!-- Jadi -->
<div class="container my-4">

<!-- Tambahkan di <head> -->
<link 
  href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css"
  rel="stylesheet">

<!-- Tambahkan di akhir sebelum </body> -->
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
```

#### ```- penjelasan``` : 
Struktur HTML-nya tetap sama — tapi:

- ```id="container"``` diganti jadi ```class="container my-4"```

- link CSS manual (```style.css```) dihapus (Bootstrap menggantikan styling-nya)

- ditambahkan link Bootstrap CSS dan JS.

#### ```- hasil```
![foto](https://github.com/azkaa-pixel/Lab---6---Web/blob/ad7a466bc0a33ae8636fc0aeb3e5b28d0d76362d/praktikum%206/1(1).png)

![foto](https://github.com/azkaa-pixel/Lab---6---Web/blob/ad7a466bc0a33ae8636fc0aeb3e5b28d0d76362d/praktikum%206/1(2).png)

![foto](https://github.com/azkaa-pixel/Lab---6---Web/blob/ad7a466bc0a33ae8636fc0aeb3e5b28d0d76362d/praktikum%206/1(3).png)

![foto](https://github.com/azkaa-pixel/Lab---6---Web/blob/ad7a466bc0a33ae8636fc0aeb3e5b28d0d76362d/praktikum%206/1(4).png)

### 2. Grid System
Memahami cara menggunakan Bootstrap Grid System (sistem 12 kolom) untuk membagi halaman menjadi beberapa kolom yang responsif tanpa perlu ```float``` atau ```width``` manual.

```html
<!-- Sebelumnya -->
<section id="wrapper">
  <section id="main"> ... </section>
  <aside id="sidebar"> ... </aside>
</section>

<!-- Jadi -->
<section id="wrapper" class="row">
  <section id="main" class="col-md-8"> ... </section>
  <aside id="sidebar" class="col-md-4"> ... </aside>
</section>
```

#### ```- penjelasan``` : 

Di Praktikum 4, kamu pakai CSS manual dengan ```float:left; width:640px;``` buat main content, dan ```width:260px;``` buat sidebar.
Nah, di Bootstrap kita cukup pakai class:

- ```.row``` → pembungkus baris (mengatur kolom di dalamnya)

- ```.col-md-8``` → kolom lebar 8 dari 12 bagian

- ```.col-md-4``` → kolom lebar 4 dari 12 bagian

Kelebihannya: di layar kecil, dua kolom ini otomatis turun ke bawah (jadi stack), tanpa bikin CSS tambahan.

#### ```- hasil```
![foto](https://github.com/azkaa-pixel/Lab---6---Web/blob/ad7a466bc0a33ae8636fc0aeb3e5b28d0d76362d/praktikum%206/2.png)

### 3.Button & Navbar 
Memahami cara menggunakan komponen tombol (button) dan navigasi (navbar) di Bootstrap untuk mempercantik tampilan halaman serta membuatnya responsif di berbagai ukuran layar.

#### navbar
```html
<nav class="navbar navbar-expand-lg navbar-dark bg-primary mb-4">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">Layout Sederhana</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav">
        <li class="nav-item"><a class="nav-link active" href="#">Home</a></li>
        <li class="nav-item"><a class="nav-link" href="#">Artikel</a></li>
        <li class="nav-item"><a class="nav-link" href="#">About</a></li>
        <li class="nav-item"><a class="nav-link" href="#">Kontak</a></li>
      </ul>
    </div>
  </div>
</nav>
```
#### tombol
```html
<!-- Sebelumnya -->
<a href="home.html" class="btn btn-large">Learn more &raquo;</a>

<!-- Jadi -->
<a href="home.html" class="btn btn-primary btn-lg">Learn more &raquo;</a>
```
#### Dan ubah semua tombol "View Detail" jadi tombol outline:
```html
<a href="#" class="btn btn-outline-primary">View detail</a>
```

#### ```- penjelasan``` : 
```Tombol (Button):```

- ```.btn``` + ```.btn-primary``` (biru), ```.btn-secondary```, ```.btn-success```, ```.btn-danger```, dsb.

- Kamu nggak perlu styling manual seperti ```background-color```, ```border```, dll.

```Navbar (Navigasi):```

- Pakai tag ```<nav class="navbar">``` dan kombinasi ```.navbar-expand-lg``` biar bisa berubah jadi menu hamburger di layar kecil.

- Warna background dan teksnya diatur dengan class ```.navbar-dark bg-primary``` atau ```.navbar-light bg-light```.

#### ```- hasil```
![foto](https://github.com/azkaa-pixel/Lab---6---Web/blob/ad7a466bc0a33ae8636fc0aeb3e5b28d0d76362d/praktikum%206/3.png)

### 4. Card
Mengubah elemen kotak biasa (box) dan widget sidebar menjadi komponen card Bootstrap,
supaya tampilannya lebih modern, rapi, dan konsisten dengan gaya Bootstrap. 

#### sidebar
```html
<!-- Sebelumnya -->
<div class="widget-box">
  <h3 class="title">Widget Header</h3>
  <ul>
    <li><a href="#">Widget Link</a></li>
  </ul>
</div>

<!-- Jadi -->
<div class="card mb-3">
  <div class="card-header bg-primary text-white">Widget Header</div>
  <ul class="list-group list-group-flush">
    <li class="list-group-item"><a href="#">Widget Link</a></li>
  </ul>
</div>
```
#### box
Ubah ```<div class="box">``` jadi ```<div class="card">``` dengan .card-body di dalamnya.

#### ```- penjelasan``` : 
Di praktikum sebelumnya, kamu pakai ```<div class="box">``` dan ```<div class="widget-box">``` untuk bikin konten berbentuk kotak.
Nah, di Bootstrap kamu bisa ganti dengan class ```.card```, ```.card-body```, ```.card-header```, dan ```.card-footer```.

#### ```- hasil```
![foto](https://github.com/azkaa-pixel/Lab---6---Web/blob/ad7a466bc0a33ae8636fc0aeb3e5b28d0d76362d/praktikum%206/4.png)

### 5.Form 
Membuat form kontak tampil lebih rapi dan interaktif menggunakan class bawaan Bootstrap seperti .form-label, .form-control, dan .btn.

```html
<form>
  <div class="mb-3">
    <label for="nama" class="form-label">Nama:</label>
    <input type="text" class="form-control" id="nama" name="nama" required />
  </div>

  <div class="mb-3">
    <label for="email" class="form-label">Email:</label>
    <input type="email" class="form-control" id="email" name="email" required />
  </div>

  <div class="mb-3">
    <label for="pesan" class="form-label">Pesan:</label>
    <textarea
      class="form-control"
      id="pesan"
      name="pesan"
      rows="5"
      required
    ></textarea>
  </div>

  <button type="submit" class="btn btn-primary">Kirim Pesan</button>
</form>
```
#### ```- penjelasan``` : 
Bootstrap punya sistem form siap pakai:

- Label: pakai ```.form-label```

- Input & Textarea: pakai ```.form-control```

- Button: pakai ```.btn``` + warna (```.btn-primary```, ```.btn-outline-success```, dll)

Setiap elemen form dibungkus dalam ```<div class="mb-3">``` buat ngasih jarak vertikal antar field.

#### ```- hasil```
![foto](https://github.com/azkaa-pixel/Lab---6---Web/blob/ad7a466bc0a33ae8636fc0aeb3e5b28d0d76362d/praktikum%206/5.png)

### 6. Responsive Layout
Menyelesaikan tahap akhir dengan menyusun ulang layout agar responsif, memastikan setiap bagian seperti hero, grid, sidebar, form, dan footer bisa menyesuaikan ukuran layar otomatis (tanpa CSS manual).

Tambahkan class berikut di elemen-elemen gambar dan section:
```html
<img src="..." class="img-fluid rounded" alt="...">
```
dan tambahkan spacing di setiap section:

#### ```- penjelasan``` :

Bootstrap udah punya sistem responsif otomatis, asal kita:

- Gunakan kombinasi class grid yang sesuai kayak ```.row```, ```.col-md-6```, ```.col-md-4```, ```.col-lg-8```, dsb.

- Tambahkan margin/padding utilitas (```.mt-4```, ```.mb-3```, ```.p-4```, dst).

- Pastikan gambar dan teks nggak keluar dari kolom dengan .img-fluid biar ukuran gambar ikut layar.

Kita juga bisa kasih beberapa penyesuaian kecil:

- Tambahin class="img-fluid" di semua <img> biar otomatis mengecil.

- Tambahin jarak antar section pakai .mt-5 atau .my-5.

- Pastikan semua konten pakai sistem container Bootstrap.

#### ```- hasil```
![foto](https://github.com/azkaa-pixel/Lab---6---Web/blob/ad7a466bc0a33ae8636fc0aeb3e5b28d0d76362d/praktikum%206/6.png)

# TUGAS 
## 1.

### A. Gunakan <nav> Bootstrap untuk bagian Navigasi
Mengganti elemen `<nav>` biasa dari praktikum 4 yang masih polos jadi navbar Bootstrap, supaya tampilannya lebih rapi, responsif, dan otomatis berubah jadi menu hamburger di layar kecil.

#### - code :
```html
<nav class="navbar navbar-expand-lg navbar-dark bg-primary mb-4">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">Layout Sederhana</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav">
        <li class="nav-item"><a class="nav-link active" href="#">Home</a></li>
        <li class="nav-item"><a class="nav-link" href="#">Artikel</a></li>
        <li class="nav-item"><a class="nav-link" href="#">About</a></li>
        <li class="nav-item"><a class="nav-link" href="#">Kontak</a></li>
      </ul>
    </div>
  </div>
</nav>
```

### B.Gunakan class ```.row```, ```.col-md-8```, dan ```.col-md-4``` untuk Main Content dan Sidebar
Membagi halaman jadi dua kolom: konten utama (main content) dan sidebar, menggunakan sistem grid Bootstrap.

#### - code :
```html
<section id="wrapper" class="row">
  <section id="main" class="col-md-8">
    <!-- isi konten utama di sini -->
  </section>

  <aside id="sidebar" class="col-md-4">
    <!-- isi sidebar di sini -->
  </aside>
</section>
```

### C. Gunakan Komponen ```.card``` Bootstrap untuk Menggantikan ```.widget-box``` (Sidebar)
Mengganti struktur lama ```div.widget-box``` di sidebar menjadi komponen Bootstrap Card, supaya tampilannya rapi dan konsisten tanpa CSS manual.

#### - code :
```html
  <div class="card mb-3">
    <div class="card-header bg-primary text-white">Widget Header</div>
    <ul class="list-group list-group-flush">
      <li class="list-group-item"><a href="#">Widget Link</a></li>
      <li class="list-group-item"><a href="#">Widget Link</a></li>
      <li class="list-group-item"><a href="#">Widget Link</a></li>
    </ul>
  </div>

  <div class="card">
    <div class="card-header bg-primary text-white">Widget Text</div>
    <div class="card-body">
      <p>
        Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt arcu.
      </p>
    </div>
  </div>
</aside>
```

### D. Gunakan Komponen ```.card``` untuk Menggantikan ```.box``` (Bagian "Heading" 3 Kolom)
Mengganti setiap elemen `.box` (yang ada gambar bundar, judul, dan teks) dengan komponen `.card` Bootstrap supaya tampilannya modern dan otomatis responsif di berbagai ukuran layar.

#### - code :
```html
<div class="row text-center">
  <div class="col-md-4 mb-4">
    <div class="card p-3">
      <img src="https://dummyimage.com/120/db7d25/fff.png" class="img-fluid rounded-circle mx-auto mb-2" alt="">
      <h3>Heading</h3>
      <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p>
      <a href="#" class="btn btn-primary">View Detail</a>
    </div>
  </div>

  <div class="col-md-4 mb-4">
    <div class="card p-3">
      <img src="https://dummyimage.com/120/3e73e6/fff.png" class="img-fluid rounded-circle mx-auto mb-2" alt="">
      <h3>Heading</h3>
      <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p>
      <a href="#" class="btn btn-primary">View Detail</a>
    </div>
  </div>

  <div class="col-md-4 mb-4">
    <div class="card p-3">
      <img src="https://dummyimage.com/120/71e6d4/fff.png" class="img-fluid rounded-circle mx-auto mb-2" alt="">
      <h3>Heading</h3>
      <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p>
      <a href="#" class="btn btn-primary">View Detail</a>
    </div>
  </div>
</div>
```

### D. Tidak Boleh Menggunakan CSS `float` atau `clear` Manual 
Menghapus semua penggunaan CSS float atau clear karena di Bootstrap, tata letak kolom dan baris sudah otomatis diatur menggunakan sistem grid (`.row` dan `.col-*`), jadi kita gak perlu lagi atur posisi elemen secara manual.

#### - code :
```html
.mb-3 { margin-bottom: 1rem; }
.my-4 { margin-top: 1.5rem; margin-bottom: 1.5rem; }
```

## 2. Ubah tampilan form biar rapi pakai class-class Bootstrap (`.form-control`, `.form-label`, `.btn`)
Merapikan tampilan form dari praktikum 5 supaya lebih bagus dan responsif pakai komponen form dari Bootstrap.

#### - code 
```html
<div class="mb-3">
  <label for="nama" class="form-label">Nama:</label>
  <input type="text" class="form-control" id="nama" name="nama" required />
</div>

<div class="mb-3">
  <label for="email" class="form-label">Email:</label>
  <input type="email" class="form-control" id="email" name="email" required />
</div>

<div class="mb-3">
  <label for="pesan" class="form-label">Pesan:</label>
  <textarea class="form-control" id="pesan" name="pesan" rows="5" required></textarea>
</div>

<button type="submit" class="btn btn-primary">Kirim Pesan</button>
```

## 3. Buat Halaman Portfolio Sederhana

### A. Sebuah Navbar di bagian atas

#### - code :
```html
<nav class="navbar navbar-expand-lg navbar-dark" style="background-color: #2C2C2E;">
  <div class="container">
    <a class="navbar-brand fw-bold text-warning" href="#">Portofolio Saya</a>
    <button
      class="navbar-toggler"
      type="button"
      data-bs-toggle="collapse"
      data-bs-target="#navbarNav"
    >
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav ms-auto">
        <li class="nav-item">
          <a class="nav-link active text-warning" href="#">Home</a>
        </li>
        <li class="nav-item">
          <a class="nav-link text-light" href="#">Tentang Saya</a>
        </li>
        <li class="nav-item">
          <a class="nav-link text-light" href="#">Portfolio</a>
        </li>
      </ul>
    </div>
  </div>
</nav>
```

#### - hasil 
![foto](https://github.com/azkaa-pixel/Lab---6---Web/blob/ad7a466bc0a33ae8636fc0aeb3e5b28d0d76362d/praktikum%206/a.png)


### B. Section "Tentang Saya"

#### - code :
```html
<section id="tentang-saya" class="py-5" style="background-color: #1C1C1E;">
  <div class="container">
    <div class="row align-items-center">
      <!-- Kolom kiri: Foto -->
      <div class="col-md-4 text-center mb-4 mb-md-0">
        <img src="https://via.placeholder.com/250" alt="Foto Saya" class="img-fluid rounded-circle border border-warning" />
      </div>
      <!-- Kolom kanan: Nama & deskripsi -->
      <div class="col-md-8 text-light">
        <h2 class="fw-bold">Ghefira Azka Fardani</h2>
        <p>
          Halo! Saya seorang developer web pemula yang antusias belajar desain UI/UX dan pengembangan website. 
          Saya suka membuat tampilan yang elegan, responsif, dan user-friendly. 
          Saya juga senang bereksperimen dengan warna dan layout agar website terlihat modern.
        </p>
      </div>
    </div>
  </div>
</section>
```

#### - hasil
![foto](https://github.com/azkaa-pixel/Lab---6---Web/blob/ad7a466bc0a33ae8636fc0aeb3e5b28d0d76362d/praktikum%206/B.png)

### C. Section “Portfolio Saya” 

#### - code :
```html
<!-- Section Portfolio Saya -->
<section id="portfolio" class="py-5" style="background-color: #000000;">
  <div class="container">
    <h2 class="text-warning fw-bold mb-4 text-center">Portfolio Saya</h2>
    <div class="row g-4">
      <!-- Proyek 1 -->
      <div class="col-md-4">
        <div class="card bg-dark text-light h-100 border border-warning shadow">
          <img src="https://via.placeholder.com/400x250" class="card-img-top" alt="Proyek 1">
          <div class="card-body">
            <h5 class="card-title text-warning">Proyek 1</h5>
            <p class="card-text">Website portfolio pribadi dengan layout modern dan responsif.</p>
          </div>
        </div>
      </div>
      <!-- Proyek 2 -->
      <div class="col-md-4">
        <div class="card bg-dark text-light h-100 border border-warning shadow">
          <img src="https://via.placeholder.com/400x250" class="card-img-top" alt="Proyek 2">
          <div class="card-body">
            <h5 class="card-title text-warning">Proyek 2</h5>
            <p class="card-text">Aplikasi sederhana untuk manajemen tugas harian dengan Bootstrap.</p>
          </div>
        </div>
      </div>
      <!-- Proyek 3 -->
      <div class="col-md-4">
        <div class="card bg-dark text-light h-100 border border-warning shadow">
          <img src="https://via.placeholder.com/400x250" class="card-img-top" alt="Proyek 3">
          <div class="card-body">
            <h5 class="card-title text-warning">Proyek 3</h5>
            <p class="card-text">Landing page interaktif dengan animasi dan efek hover menarik.</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>
```

#### - hasil 
![foto](https://github.com/azkaa-pixel/Lab---6---Web/blob/ad7a466bc0a33ae8636fc0aeb3e5b28d0d76362d/praktikum%206/c.png)



















  
  



