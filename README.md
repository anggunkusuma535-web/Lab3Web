# Praktikum 3: CSS Dasar

**Nama:** Anggun Kusuma Wardani
**NIM:** [312510045]  
**Mata Kuliah:** Pemrograman Web  

## Pemrograman Web

Repository ini dibuat untuk memenuhi tugas **Praktikum 3: CSS Dasar** pada mata kuliah Pemrograman Web. Praktikum ini membahas konsep dasar CSS, aturan penulisan CSS, penggunaan selector, serta penerapan CSS pada dokumen HTML untuk menghasilkan tampilan halaman web yang lebih menarik, terstruktur, dan mudah dibaca.

## Daftar Isi

1. [Tujuan Praktikum](#1-tujuan-praktikum)
2. [Landasan Teori](#2-landasan-teori)
3. [Struktur Repository](#3-struktur-repository)
4. [Langkah-Langkah Praktikum](#4-langkah-langkah-praktikum)
5. [Hasil Praktikum](#5-hasil-praktikum)
6. [Pertanyaan dan Jawaban](#6-pertanyaan-dan-jawaban)
7. [Kesimpulan](#7-kesimpulan)

---

## 1. Tujuan Praktikum

Tujuan pelaksanaan Praktikum 3: CSS Dasar adalah:

1. Memahami konsep dasar Cascading Style Sheets (CSS).
2. Memahami aturan penulisan CSS pada dokumen HTML.
3. Memahami penggunaan selector sebagai pengontrol penerapan CSS.
4. Mampu membuat dan menerapkan pengaturan CSS pada HTML.

## 2. Landasan Teori

### 2.1 Pengertian CSS

Cascading Style Sheets (CSS) adalah bahasa stylesheet yang digunakan untuk mengatur tampilan dan tata letak elemen HTML pada halaman web. CSS digunakan untuk menentukan warna, jenis dan ukuran huruf, jarak antar-elemen, garis tepi, latar belakang, posisi, serta berbagai aspek visual lainnya.

CSS bukan bahasa pemrograman, melainkan bahasa untuk mendeskripsikan gaya tampilan dokumen. Dengan menggunakan CSS, struktur konten yang dibuat menggunakan HTML dapat dipisahkan dari pengaturan tampilannya. Pemisahan ini membuat kode lebih terstruktur, mudah dipelihara, dan lebih mudah dikembangkan.

CSS juga memungkinkan satu aturan tampilan digunakan pada banyak elemen atau halaman. Apabila aturan tersebut diubah, tampilan elemen yang menggunakan aturan tersebut dapat ikut berubah tanpa perlu mengubah setiap elemen HTML satu per satu.

### 2.2 Struktur CSS

Secara umum, aturan CSS terdiri atas dua komponen utama, yaitu selector dan declaration.

- **Selector** adalah bagian yang menentukan elemen HTML yang akan dikenai aturan CSS.
- **Declaration** adalah aturan yang diterapkan kepada elemen yang dipilih.
- **Property** adalah aspek tampilan yang ingin diatur.
- **Value** adalah nilai yang diberikan kepada property.

Contoh:

```css
h1 {
    color: blue;
    text-align: center;
}
```

Keterangan:

- `h1` merupakan selector.
- `color` dan `text-align` merupakan property.
- `blue` dan `center` merupakan value.
- Seluruh aturan di dalam kurung kurawal merupakan declaration block.

### 2.3 Jenis Penulisan CSS

Terdapat tiga cara utama untuk menerapkan CSS pada HTML.

**A. Internal CSS**

Internal CSS ditulis menggunakan tag `<style>` di dalam bagian `<head>` dokumen HTML.

```html
<head>
    <style>
        body {
            background-color: lightblue;
        }

        p {
            color: blue;
            font-size: 20px;
        }
    </style>
</head>
```

Internal CSS cocok digunakan ketika aturan tampilan hanya diperlukan pada satu dokumen HTML.

**B. External CSS**

External CSS ditulis dalam file terpisah yang memiliki ekstensi `.css`. File tersebut dihubungkan ke dokumen HTML menggunakan tag `<link>`.

```html
<head>
    <link rel="stylesheet" href="style_eksternal.css">
</head>
```

Contoh aturan dalam file `style_eksternal.css`:

```css
body {
    font-family: Arial, sans-serif;
}

nav {
    background-color: #20A759;
    padding: 10px;
}
```

External CSS memudahkan pengelolaan tampilan karena satu file CSS dapat digunakan oleh beberapa halaman HTML.

**C. Inline CSS**

Inline CSS ditulis langsung pada elemen HTML menggunakan atribut `style`.

```html
<p style="text-align: center; color: blue;">
    Saya sedang belajar CSS.
</p>
```

Inline CSS memengaruhi elemen tempat atribut tersebut dituliskan. Cara ini praktis untuk pengaturan tertentu, tetapi penggunaan berlebihan dapat membuat kode sulit dikelola.

### 2.4 CSS Selector

Selector digunakan untuk memilih elemen HTML yang akan menerima aturan CSS.

**A. Element Selector**

Element selector menggunakan nama tag HTML sebagai selector.

```css
p {
    color: green;
    font-size: 16px;
}
```

Aturan tersebut diterapkan kepada seluruh elemen `<p>` yang sesuai.

**B. Class Selector**

Class selector menggunakan tanda titik (`.`) sebelum nama class.

```css
.merah {
    color: red;
}

.rata-tengah {
    text-align: center;
}
```

Penggunaannya pada HTML:

```html
<h1 class="merah">Heading berwarna merah</h1>
<p class="rata-tengah">Paragraf rata tengah</p>
```

Class dapat digunakan pada beberapa elemen HTML. Satu elemen juga dapat mempunyai beberapa class sekaligus.

**C. ID Selector**

ID selector menggunakan tanda pagar (`#`) sebelum nama ID.

```css
#intro {
    background-color: #418fb1;
    padding: 10px;
}
```

Penggunaannya pada HTML:

```html
<div id="intro">
    <h1>Hello World</h1>
</div>
```

ID digunakan untuk mengidentifikasi satu elemen tertentu dalam dokumen HTML. Dalam satu dokumen, nilai ID sebaiknya unik.

### 2.5 CSS Cascade dan Specificity

CSS memiliki mekanisme cascade untuk menentukan aturan yang digunakan ketika beberapa deklarasi memengaruhi elemen yang sama. Penentuannya antara lain dipengaruhi oleh prioritas deklarasi, specificity selector, dan urutan aturan.

Pada deklarasi normal, inline style umumnya mengungguli aturan internal maupun eksternal yang memiliki prioritas normal. Sementara itu, jika specificity sama, aturan yang ditulis lebih akhir biasanya akan diterapkan.

Secara umum, ID selector memiliki specificity lebih tinggi daripada class selector, sedangkan class selector memiliki specificity lebih tinggi daripada element selector.

---

## 3. Struktur Repository

Struktur repository praktikum ini adalah sebagai berikut:

```text
Lab3Web/
├── .vscode/
├── Screenshot/
├── README.md
├── lab2_css_dasar.html
├── lab2_css_eksperimen.html
├── lab2_css_eksternal.html
└── style_eksternal.css
```

Keterangan:

| File atau folder | Fungsi |
|---|---|
| `.vscode/` | Menyimpan konfigurasi editor VS Code jika digunakan. |
| `Screenshot/` | Menyimpan dokumentasi gambar hasil praktikum. |
| `README.md` | Berisi penjelasan praktikum, langkah kerja, jawaban, dan kesimpulan. |
| `lab2_css_dasar.html` | Dokumen HTML untuk praktik CSS internal, inline, dan selector. |
| `lab2_css_eksperimen.html` | Dokumen untuk melakukan percobaan perubahan properti dan nilai CSS. |
| `lab2_css_eksternal.html` | Dokumen HTML untuk praktik penggunaan CSS eksternal. |
| `style_eksternal.css` | File stylesheet eksternal yang digunakan untuk mengatur tampilan halaman HTML. |

Nama file HTML mengikuti penamaan pada modul praktikum, meskipun kegiatan ini merupakan Praktikum 3.

## 4. Langkah-Langkah Praktikum

### 4.1 Membuat Dokumen HTML

Langkah pertama adalah menyiapkan dokumen HTML menggunakan Visual Studio Code. Dokumen dibuat dengan struktur HTML dasar yang terdiri atas `<!DOCTYPE html>`, `<html>`, `<head>`, dan `<body>`.

Pada bagian body ditambahkan elemen header, navigasi, judul, paragraf, serta tautan informasi.

Bagian utama kode:

```html
<header>
    <h1>CSS Internal dan <i>Inline CSS</i></h1>
</header>

<nav>
    <a href="lab2_css_dasar.html">CSS Dasar</a>
    <a href="lab2_css_eksternal.html">CSS Eksternal</a>
    <a href="lab1_tag_dasar.html">HTML Dasar</a>
</nav>

<div id="intro">
    <h1>Hello World</h1>
    <p>
        Kami sedang belajar HTML dan CSS dasar,
        pada mata kuliah Pemrograman Web.
    </p>

    <a class="button btn-primary" href="#intro">
        Informasi selengkapnya.
    </a>
</div>
```

**Hasil yang diharapkan:** halaman menampilkan judul, tautan navigasi, bagian pengenalan, paragraf, dan tautan informasi.


### 4.2 Mendeklarasikan CSS Internal

Langkah kedua adalah menambahkan aturan CSS internal pada bagian `<head>` menggunakan tag `<style>`.

```html
<style>
    body {
        font-family: 'Open Sans', sans-serif;
    }

    header {
        min-height: 80px;
        border-bottom: 1px solid #77CCEF;
    }

    h1 {
        font-size: 24px;
        color: #0F189F;
        text-align: center;
        padding: 20px 10px;
    }

    h1 i {
        color: #6d6a6b;
    }
</style>
```

Aturan tersebut mengatur jenis huruf halaman, tinggi minimum header, garis bawah header, ukuran judul, warna judul, perataan teks, dan warna teks miring di dalam heading.

Setelah kode ditambahkan, simpan file dan muat ulang halaman di browser.


### 4.3 Menambahkan Inline CSS

Langkah ketiga adalah menambahkan inline CSS pada elemen paragraf sesuai modul.

```html
<p style="text-align: center; color: #ccd8e4;">
    Kami sedang belajar HTML dan CSS dasar.
</p>
```

Properti `text-align: center` digunakan untuk meratakan teks ke tengah, sedangkan `color: #ccd8e4` memberikan warna teks abu-abu kebiruan yang terang.

Inline CSS diterapkan secara langsung pada elemen yang diberi atribut `style`.


### 4.4 Membuat CSS Eksternal

Langkah keempat adalah membuat file `style_eksternal.css` untuk memisahkan aturan tampilan dari dokumen HTML.

Contoh kode CSS navigasi:

```css
nav {
    background: #20A759;
    color: #fff;
    padding: 10px;
}

nav a {
    color: #fff;
    text-decoration: none;
    padding: 10px 20px;
}

nav .active,
nav a:hover {
    background: #0B6B3A;
}
```

Keterangan:

- `background` mengatur warna latar belakang.
- `color` mengatur warna teks.
- `padding` memberikan jarak di dalam elemen.
- `text-decoration: none` menghilangkan garis bawah tautan.
- `nav a:hover` mengatur tampilan tautan ketika penunjuk diarahkan ke atasnya.

Hubungkan file CSS ke HTML menggunakan tag berikut di bagian `<head>`:

```html
<link rel="stylesheet" href="style_eksternal.css" type="text/css">
```

Simpan perubahan dan muat ulang halaman. Navigasi akan memiliki latar belakang hijau, teks putih, serta perubahan warna ketika tautan disorot.

### 4.5 Menambahkan CSS ID dan Class Selector

Langkah kelima adalah menerapkan ID selector dan class selector untuk mengatur bagian pengenalan dan tombol informasi.

Contoh ID selector:

```css
#intro {
    background: #418fb1;
    border: 1px solid #099249;
    min-height: 100px;
    padding: 10px;
}

#intro h1 {
    text-align: left;
    border: 0;
    color: #fff;
}
```

ID `intro` mengatur latar belakang, garis tepi, tinggi minimum, dan jarak bagian pengenalan. Selector `#intro h1` mengatur heading yang berada di dalam elemen dengan ID `intro`.

Contoh class selector:

```css
.button {
    padding: 15px 20px;
    background: #bebcbd;
    color: #fff;
    display: inline-block;
    margin: 10px;
    text-decoration: none;
}

.btn-primary {
    background: #E42A42;
}
```

Penggunaan class pada HTML:

```html
<a class="button btn-primary" href="#intro">
    Informasi selengkapnya.
</a>
```

Elemen tautan menggunakan dua class sekaligus, yaitu `button` dan `btn-primary`. Dengan demikian, elemen tersebut menerima aturan dari kedua class, sedangkan warna latar belakang merah berasal dari `.btn-primary`.


### 4.6 Melakukan Eksperimen CSS

Eksperimen dilakukan dengan mengubah atau menambahkan property dan value CSS untuk mengamati pengaruhnya terhadap tampilan halaman.

Contoh perubahan yang dapat dilakukan:

```css
body {
    background-color: #f4f7fb;
    font-family: Arial, sans-serif;
}

#intro {
    padding: 20px;
    border-radius: 8px;
}

.button {
    padding: 12px 18px;
    font-size: 16px;
}
```

Perubahan tersebut dapat mengatur warna latar belakang halaman, jenis huruf, jarak bagian pengenalan, sudut elemen, dan ukuran teks tombol.

Setiap perubahan perlu disimpan dan diuji melalui browser agar hasilnya dapat diamati.


## 5. Hasil Praktikum

Berdasarkan langkah-langkah yang dilakukan, hasil praktikum yang diharapkan adalah:

1. Dokumen HTML dapat dibuat dan ditampilkan melalui browser.
2. CSS internal dapat mengatur tampilan elemen HTML melalui tag `<style>`.
3. Inline CSS dapat mengubah tampilan elemen tertentu melalui atribut `style`.
4. CSS eksternal dapat digunakan dengan menghubungkan file `.css` menggunakan tag `<link>`.
5. Element selector, class selector, dan ID selector dapat digunakan untuk memilih elemen yang berbeda.
6. Perubahan property dan value CSS menghasilkan perubahan tampilan yang dapat diamati.
7. Dokumentasi screenshot dapat digunakan sebagai bukti pelaksanaan setiap tahap praktikum.

## 6. Pertanyaan dan Jawaban

### Pertanyaan 1

**Lakukan eksperimen dengan mengubah dan menambah properti dan nilai pada kode CSS dengan mengacu pada CSS Cheat Sheet yang diberikan pada file terpisah dari modul ini.**

**Jawaban:**

Eksperimen dilakukan dengan mengubah beberapa property dan value CSS, seperti `color`, `background-color`, `font-size`, `font-family`, `text-align`, `padding`, `margin`, `border`, dan `border-radius`.

Contoh kode:

```css
body {
    background-color: #f4f7fb;
    font-family: Arial, sans-serif;
}

h1 {
    color: #0F189F;
    font-size: 28px;
    text-align: center;
}

p {
    color: #333333;
    font-size: 16px;
    line-height: 1.6;
}

.button {
    background-color: #E42A42;
    color: white;
    padding: 12px 18px;
    border-radius: 5px;
}
```

Hasil eksperimen menunjukkan bahwa perubahan nilai pada property CSS memengaruhi tampilan elemen HTML. Misalnya, `font-size` mengubah ukuran teks, `color` mengubah warna teks, `background-color` mengubah warna latar belakang, dan `text-align` mengatur perataan teks.

Eksperimen ini membantu memahami hubungan antara property dan value serta cara CSS mengendalikan tampilan halaman web.

### Pertanyaan 2

**Apa perbedaan pendeklarasian CSS elemen `h1 {...}` dengan `#intro h1 {...}`? Berikan penjelasannya!**

**Jawaban:**

Selector `h1` merupakan element selector yang berlaku untuk seluruh elemen `<h1>` yang sesuai dalam dokumen HTML. Sebaliknya, selector `#intro h1` merupakan selector gabungan yang hanya menargetkan elemen `<h1>` yang berada di dalam elemen dengan ID `intro`.

Contoh:

```css
h1 {
    color: blue;
    text-align: center;
}

#intro h1 {
    color: white;
    text-align: left;
}
```

Contoh HTML:

```html
<h1>Judul Halaman</h1>

<div id="intro">
    <h1>Hello World</h1>
</div>
```

Pada contoh tersebut, judul pertama berwarna biru dan rata tengah. Sementara itu, heading `Hello World` yang berada di dalam `#intro` berwarna putih dan rata kiri.

Hal ini terjadi karena selector `#intro h1` memiliki specificity lebih tinggi daripada selector `h1`, sehingga deklarasi tersebut menang untuk property yang sama dalam kondisi normal.

### Pertanyaan 3

**Apabila ada deklarasi CSS secara internal, lalu ditambahkan CSS eksternal dan inline CSS pada elemen yang sama, deklarasi manakah yang akan ditampilkan pada browser? Berikan penjelasan dan contohnya!**

**Jawaban:**

Pada deklarasi CSS normal, inline CSS umumnya memiliki prioritas lebih tinggi daripada deklarasi internal dan eksternal yang mengatur elemen yang sama. Di antara CSS internal dan eksternal, apabila specificity sama dan tidak ada aturan prioritas lain yang mengubah hasilnya, deklarasi yang ditulis lebih akhir akan digunakan.

Contoh CSS internal:

```html
<style>
    p {
        color: blue;
    }
</style>
```

Contoh CSS eksternal dalam file `style_eksternal.css`:

```css
p {
    color: green;
}
```

Contoh inline CSS:

```html
<p style="color: red;">Belajar CSS Dasar</p>
```

Pada contoh tersebut, teks paragraf akan berwarna merah karena inline CSS menetapkan `color: red`.

Apabila inline CSS dihapus, warna paragraf akan ditentukan oleh aturan internal dan eksternal berdasarkan specificity dan urutan deklarasinya. Oleh karena itu, tidak tepat menyimpulkan bahwa CSS eksternal selalu mengalahkan CSS internal atau sebaliknya tanpa melihat susunan aturan yang sebenarnya.

### Pertanyaan 4

**Pada sebuah elemen HTML terdapat ID dan Class. Apabila masing-masing selector tersebut terdapat deklarasi CSS, deklarasi manakah yang akan ditampilkan pada browser? Berikan penjelasan dan contohnya dengan elemen `<p id="paragraf-1" class="text-paragraf">`.**

**Jawaban:**

Jika sebuah elemen HTML memiliki ID dan class sekaligus, elemen tersebut dapat menerima aturan dari kedua selector. Apabila keduanya mengatur property yang sama dengan deklarasi normal dan tidak ada faktor prioritas lain, ID selector memiliki specificity lebih tinggi daripada class selector.

Contoh CSS:

```css
#paragraf-1 {
    color: red;
    font-size: 18px;
}

.text-paragraf {
    color: blue;
    text-align: justify;
}
```

Contoh HTML:

```html
<p id="paragraf-1" class="text-paragraf">
    Saya sedang mempelajari CSS selector.
</p>
```

Pada contoh tersebut:

- Teks berwarna merah karena `#paragraf-1` memiliki specificity lebih tinggi daripada `.text-paragraf` untuk property `color`.
- Ukuran teks menjadi 18 piksel karena diatur oleh ID selector.
- Teks rata kanan-kiri karena property `text-align` diatur oleh class selector dan tidak ditimpa oleh ID selector.

Dengan demikian, aturan dari ID dan class tidak selalu saling menghapus. Property yang berbeda dapat diterapkan bersamaan, sedangkan property yang sama ditentukan melalui mekanisme cascade dan specificity.

---

## 7. Kesimpulan

Praktikum 3: CSS Dasar memberikan pemahaman mengenai cara mengatur tampilan halaman web menggunakan Cascading Style Sheets. CSS memungkinkan elemen HTML memiliki tampilan yang lebih terstruktur dan menarik tanpa harus mengubah struktur konten secara keseluruhan.

Melalui praktikum ini, dipelajari tiga metode penulisan CSS, yaitu internal CSS, external CSS, dan inline CSS. Setiap metode memiliki karakteristik dan kegunaan masing-masing. Internal CSS ditulis pada bagian `<head>`, external CSS disimpan dalam file terpisah, sedangkan inline CSS diterapkan secara langsung pada elemen HTML.

Praktikum ini juga membahas element selector, class selector, dan ID selector. Pemahaman terhadap selector sangat penting karena menentukan elemen mana yang akan menerima aturan CSS. Selain itu, pemahaman mengenai cascade dan specificity membantu menjelaskan bagaimana browser menentukan deklarasi yang digunakan ketika beberapa aturan saling memengaruhi.

Dengan melakukan eksperimen terhadap property dan value CSS, perubahan tampilan dapat diamati secara langsung melalui browser. Secara keseluruhan, praktikum ini menjadi dasar untuk mempelajari pengembangan tampilan web yang lebih konsisten, terstruktur, mudah dikelola, dan responsif terhadap berbagai ukuran perangkat.