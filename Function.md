# Function/Method

Function adalah sebuah blok kode yang disusun sedemikian rupa untuk menjalankan sebuah tindakan.
Blok kode ini dibuat untuk dapat bisa digunakan kembali. Cara atau bentuk penulisan function adalah
sebagai berikut:

```javascript
function nama_function(parameter 1, parameter 2, ...) {
  [Isi dari function berupa tindakan]
  return [expression];
}
```

Kode di atas tidak dapat kita copy-paste kan langsung, melainkan hanya sebuah bentuk penulisan `function`.
Sebuah `function`, umumnya melakukan tindakan dan sebelum `function` berakhir, `function` bisa
mengembalikan nilai dengan cara menambahkan sintaks return.

Kita juga dapat mengirimkan nilai ke dalam sebuah `function` dengan mencantumkannya ke dalam tanda kurung
dalam penulisan `function`. Untuk mengirimkan nilai lebih dari satu, gunakan tanda `,` sebagai pemisah.

**Contoh Function 1:** Function sederhana tanpa return

```javascript
function tampilkan() {
  console.log("halo!");
}

tampilkan();
```

**Contoh Function 2:** Function sederhana dengan return

```javascript
function munculkanAngkaDua() {
  return 2
}

var tampung = munculkanAngkaDua();
console.log(tampung)
```

**Contoh Function 3:** Function dengan parameter

```javascript
function kalikanDua(angka) {
  return angka * 2
}

var tampung = kalikanDua(2);
console.log(tampung)

```

**Contoh Function 4:** Pengiriman parameter lebih dari satu

```javascript
function tampilkanAngka(angkaPertama, angkaKedua) {
  return angkaPertama + angkaKedua
}

console.log(tampilkanAngka(5,3))
```

**Contoh Function 5:** NUMBER JUMPER

#### `PROBLEM`
numberJumper adalah sebuah function yang menerima tiga parameter.
Parameter pertama disebut firstNum,
parameter kedua disebut secondNum,
dan parameter ketiga disebut jumper.
number Jumper akan membentuk deret angka (bukan array) dengan range
menggunakan firstNum dan secondNum, dan deret angka harus naik (increment)
dengan penambahan sesuai nilai jumper. Jangan lupa angka terakhir juga ditampilkan, terlepas pertambahannya sampai berapapun.

##### `EXAMPLE`
input: numberJumper(3, 6, 1)
proses: console log angka dari 3 - 6, dengan pertambahan 1.
output:

3
4 < - ini pertambahan 1 dari 3
5 < - ini pertambahan 1 dari 5
6 < - ini pertambahan 1 dari 5, sekaligus buntut nya!

input: numberJumper(5, 2, 2)
proses: console log angka dari 2 - 5. dengan pertambahan 2.
output:

2
4 <- ini pertambahan 2 dari 2
5 <- ini buntut nya!

input: numberJumper(13, 1, 10)
proses: console log angka dari 1 - 13. dengan pertambahan 10.
output:

1
11 <- ini pertambahan 10 dari 1
13 <- ini buntut nya

#### `RULES`

- Wajib menggunakan pseudocode sebelum memulai kode
- Dilarang menggunakan Math.max, Math.min, .apply, .bind, .call
- Dilarang menggunakan spread operator (abaikan jika tidak tahu ini apa, belum penting untuk sekarang :))
- Dilarang menggunakan regex metode apapun
*/
// 1. Buat kondisi jika fisrtnum lebih kecil dari secondNum, Maka 
  //1.a Buat perulangan dari indeks pertama adalah firstnum, indeks kurang dari secondnum, dengan pertambahan sesuai dengan jumper 
  //1.b Tampilkan perulangan ke i
  //1.c Jika i dikurang dengan indeks sebelumnya tidak sama dengan jumper
  //1.d Tampilkan i yang di kurang 1
// 2. Jika kondisi secondNum lebih kecil dari secondNum, maka
  //2.a Buat perulangan dari indeks pertama adalah second indeks kurang dari firstnum dengan pertambahan sesuai dengan jumper 
  //2.b Tampilkan perulangan ke J

function numberJumper(firstNum, secondNum, jumper) {
  if (firstNum <= secondNum) {
    for (var i = firstNum; i <= secondNum; i = i + jumper) {
        console.log(i);
      }
      if(i-(i-1) !== jumper){
      console.log(i-1)
    }
  }
  
  
  if (secondNum <= firstNum) {
    for (var j = secondNum; j <= firstNum; j = j + jumper) {
      console.log(j)
    }
  }
}


numberJumper(1, 6, 2);
/*
1
3
5
6
*/

numberJumper(7, 1, 3);
/*
1
4
7
*/

numberJumper(1, 3, 2);
/*
1
3
*/

**Contoh Function 5:** Inisialisasi parameter dengan nilai default

```javascript
function tampilkanAngka(angka = 1) {
  return angka
}

console.log(tampilkanAngka(5)) // 5, sesuai dengan nilai parameter yang dikirim
console.log(tampilkanAngka()) // 1, karena default dari parameter adalah 1
```

:warning: Waspadai pengiriman parameter yang UNDEFINED!

Kita juga dapat menampung function sebagai variable dengan sebuah bentuk function
yang dinamakan Anonymous Function.

```javascript
var fungsiPerkalian = function(angkaPertama, angkaKedua) {
  return angkaPertama * angkaKedua
}

console.log(fungsiPerkalian(2,4))
```
