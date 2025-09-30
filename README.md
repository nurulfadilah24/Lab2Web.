# Lab2Web

Praktikum Pemrograman Web – Universitas Pelita Bangsa

## Identitas

* Nama: **(Nurul fadilah)**
* NIM: **(312410689)**
* Mata Kuliah: **Pemrograman Web**
* Dosen: Agung Nugroho 

---

## Pertanyaan dan Jawaban

### 1. Eksperimen CSS

Saya melakukan eksperimen dengan menambahkan properti dari CSS Cheat Sheet seperti:

* `text-transform: uppercase;` → untuk membuat teks menjadi huruf besar.
* `letter-spacing: 2px;` → untuk memberi jarak antar huruf.
* `border-radius: 5px;` → membuat sudut paragraf membulat.
* `line-height: 1.6;` → membuat jarak antar baris lebih rapi.

### 2. Perbedaan `h1 {}` dengan `#intro h1 {}`

* `h1 {}`: semua elemen `<h1>` akan diberi style yang sama.
* `#intro h1 {}`: hanya elemen `<h1>` yang berada di dalam elemen dengan `id="intro"` yang terkena style.

Contoh:

```html
<h1>Judul Umum</h1> <!-- pakai style h1 {} -->
<div id="intro">
  <h1>Judul Bagian Intro</h1> <!-- pakai style #intro h1 {} -->
</div>
```

### 3. Internal, Eksternal, dan Inline CSS

* **Inline CSS** (`style="..."`) memiliki prioritas tertinggi.
* **Internal CSS** (di dalam `<style>...</style>`) prioritas kedua.
* **Eksternal CSS** (file `.css` terpisah) prioritas terakhir.

Contoh:

```html
<h1 style="color: green;">Judul</h1>
```

Meskipun di CSS eksternal tertulis `h1 { color: blue; }`, yang tampil tetap hijau karena inline CSS menang.

### 4. ID vs Class

Jika sebuah elemen punya **ID** dan **Class** dengan deklarasi berbeda, maka **ID lebih kuat**.

Contoh:

```html
<p id="paragraf-1" class="text-paragraf">Contoh Paragraf</p>
```

```css
#paragraf-1 { color: red; }
.text-paragraf { color: blue; }
```

👉 Yang ditampilkan browser adalah **merah**, karena selector ID lebih spesifik dibanding class.

---

## Struktur Project

```
Lab2Web/
│── index.html
│── style.css
│── README.md
```

### index.html

```html
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <title>Belajar CSS</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <h1 style="color: green;">Judul</h1>
  <p id="paragraf-1" class="text-paragraf">Contoh Paragraf</p>
  <h1>Judul Umum</h1>
  <div id="intro">
    <h1>Judul Bagian Intro</h1>
  </div>
  <p>Ini adalah contoh paragraf dengan styling CSS yang sudah diubah.</p>
</body>
</html>
```

### style.css

```css
body {
  font-family: Arial, Helvetica, sans-serif;
  background-color: #f5f5f5;
  margin: 20px;
}
h1 {
  color: blue;
  text-align: center;
  text-transform: uppercase;
  letter-spacing: 2px;
}
#intro h1 {
  color: red;
  font-style: italic;
}
p {
  color: #333;
  background-color: #fff;
  padding: 10px;
  border-left: 4px solid #20A759;
  border-radius: 5px;
  line-height: 1.6;
  max-width: 600px;
  margin: 20px auto;
}
#intro {
  background-color: #e8f5e9;
  padding: 15px;
  border: 1px solid #20A759;
  border-radius: 8px;
  max-width: 600px;
  margin: 20px auto;
}
#paragraf-1 {
  color: red;
}
.text-paragraf {
  color: blue;
}
```

---

## Cara Menjalankan

1. Clone repository atau download folder.
2. Buka `index.html` di browser.
3. Lihat hasil styling CSS sesuai eksperimen.

---

## Screenshot

Tambahkan screenshot hasil percobaan kamu di folder `screenshot/` lalu masukkan ke README dengan format:

```markdown
![Hasil Percobaan](screenshot/hasil1.png)
```

---

## Kesimpulan

* CSS memungkinkan styling lebih terstruktur dengan selector (elemen, class, ID).
* Urutan prioritas: Inline > Internal > Eksternal.
* ID lebih kuat dibanding Class dalam penerapan style.

