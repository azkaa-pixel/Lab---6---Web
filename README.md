# Lab---6---Web

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
![foto]()

![foto]()

![foto]()

![foto]()

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
![foto]

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
![foto]

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
![foto]

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
![foto]

### 6. Responsive Layout
Menyelesaikan tahap akhir dengan menyusun ulang layout agar responsif, memastikan setiap bagian seperti hero, grid, sidebar, form, dan footer bisa menyesuaikan ukuran layar otomatis (tanpa CSS manual).

Tambahkan class berikut di elemen-elemen gambar dan section:
```html
<img src="..." class="img-fluid rounded" alt="...">
```
dan tambahkan spacing di setiap section:
```html

#### ```- penjelasan``` : 

#### ```- hasil```
![foto]
### 6. 

```html
```
#### ```- penjelasan``` : 

#### ```- hasil```
![foto]
