# Conditional

Kondisional adalah sebuah metode dimana kode akan mengecek apakah sebuah premis benar atau tidak.
Jika kondisi sesuai, maka kode dalam kondisional akan dijalankan.

## Contoh Conditional 1** Menjalankan proses apabila statement kondisi `true`.

```javascript
if(true) {
  console.log("Jalankan kode"); // baris kode ini akan di panggil
}
```

## Contoh Conditional 2** Tidak menjalankan proses di dalam block/scope conditional apabila statement kondisi `false`.

```javascript
if(false) {
  console.log("Jalankan kode"); // baris kode ini tidak di panggil
}
```

## Contoh Conditional 3** Conditional dengan statement yang akan menghasilkan nilai `true` atau `false`

```javascript
var tampung = 5;
if(tampung == 5) {
  console.log("angka yang ditampung adalah 5!");
}
```

Di dalam conditional, kita juga mengenal dengan yang dinamakan dengan branching. Branching, atau dalam bahasa indonesia berarti pencabangan, kita menjalankan potongan kode kita sesuai dengan "cabang" atau "jalur" yang memenuhi kondisi tersebut.

Contoh sangat sederhana-nya adalah sebuah kasus berikut ini:

Seorang anak diminta oleh ibunya untuk membeli telur di supermarket dan langsung pulang ke rumah. Jika di supermarket tersebut kehabisan telur, maka anak itu harus menelepon ibunya dan mengabari kalau supermarket kehabisan telur. Anak tersebut akan datang ke supermarket dan menemukan kondisi yang bercabang:

- Jika di supermarket terdapat telur, anak itu akan membeli telur itu dan pulang, atau
- Jika di supermarket tidak terdapat telur, anak itu akan menelepon ibunya.

pada JavaScript dan berbagai bahasa pemrograman, "jika tidak terdapat telur", atau bisa dibilang kondisi yang terjadi diluar "ekspektasi", terdapat `else` yang akan menjalankan proses lain jika `if` bernilai `false`. Contoh lebih jelas bisa dilihat dari contoh dibawah ini:

## Contoh Conditional 4** Branching Sederhana (If-else)

```javascript
var tampung = 5;
if(tampung == 5) {
  console.log("angka yang ditampung adalah 5!");
}
else {
  console.log("angka yang ditampung bukan 5!");
}
```

Tidak hanya sampai situ, kondisional bisa juga bersifat bertumpuk, atau biasanya disebut juga sebagai nested-if.

##  Contoh Conditional 5** Branching Bertumpuk Sederhana (If-else)

```javascript
var tampung = 5;
if(tampung == 5) {
  console.log("angka yang ditampung adalah 5!");
}
else {
  if(tampung < 5) {
    console.log("angka yang ditampung bukan 5, tapi lebih kecil dari 5.");
  }
  else {
    console.log("angka yang ditampung bukan 5, tapi lebih besar dari 5.");
  }
}
```

Contoh di atas juga bisa dibuat dalam bentuk lain, yaitu `else if`. `else-if` adalah sebuah kondisional, dimana statement `else if` akan dijalankan apabila `if` tidak memenuhi kondisi / `false`, dan dijalankan sebelum statement `else`.

## Contoh Conditional 5** Branching Bertumpuk Sederhana (If-else)

```javascript
var tampung = 5;
if(tampung == 5) {
  console.log("angka yang ditampung adalah 5!");
}
else if(tampung < 5) {
    console.log("angka yang ditampung bukan 5, tapi lebih kecil dari 5.");
}
else {
  console.log("angka yang ditampung bukan 5, tapi lebih besar dari 5.");
}
```

Selain menggunakan if-else, ada satu cara lagi untuk melakukan conditional, yaitu switch-case. Switch case ini biasanya lebih sering digunakan untuk skenario yang melibatkan banyak kondisi atau branching yang banyak. Contoh sederhananya adalah dengan sebuah remote TV.

```javascript
var buttonPushed = 1;
switch(buttonPushed) {
  case 1:   { console.log('matikan TV!'); break; }
  case 2:   { console.log('turunkan volume TV!'); break; }
  case 3:   { console.log('tingkatkan volume TV!'); break; }
  case 4:   { console.log('matikan suara TV!'); break; }
  default:  { console.log('Tidak terjadi apa-apa'); }
}
```  

Seperti dilihat di kode di atas, `switch` akan mengambil nilai, dan `case` adalah skenario apa saja yang memungkinkan untuk menjalankan satu proses. Kamu mungkin menyadari ada 1 sintaks baru yang kamu temukan: `break;`. Break memungkinkan kamu untuk "berhenti" dari proses kondisional/switch-case, dengan tujuan agar proses tidak berlanjut ke case selanjutnya. untuk eksperimenmu, kamu bisa mencoba menghapus `break` dan perhatikan apa yang terjadi.

Kamu bisa eksperimen dan mencoba kode di atas [disini](http://jsbin.com/qucoma/edit?js,console)
