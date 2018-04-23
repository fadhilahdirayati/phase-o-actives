#Data Type

Data Type, atau dalam bahasa Indonesia kita sebut sebagai Tipe Data, adalah sekumpulan data dengan nilai yang memiliki karakteristik berbeda. Beberapa contoh dari tipe data adalah:

- Number: tipe data dengan nilai berupa angka
- String: tipe data dengan nilai berupa kumpulan atau set dari beberapa karakter
- Boolean: tipe data dengan nilai berupa `true` atau `false`.

#Variable

Variable, atau dalam bahasa Indonesia kita sebut variabel, bisa memegang atau berisi hampir semua tipe data yang tersedia. Variabel memungkinkan kita untuk memuat atau menyimpan nilai data ke dalam sesuatu. Biasanya bersifat sementara saat program dijalankan.

```javascript
var tampung = 5;
console.log(tampung); // 5
```

```javascript
var angkaGanjil = 1;
var angkaGenap = 2;
console.log(angkaGanjil); // 1
console.log(angkaGenap); // 2
```

:warning: Waspadai pemanggilan variable yang tidak bernilai!
```javascript
var tampungBaru;
console.log(tampungBaru); // undefined
```
