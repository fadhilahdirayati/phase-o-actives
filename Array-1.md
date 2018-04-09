###JavaScript Data Types - Array

**Contoh Soal 1 - Array Mastery: Love Me No**

[INSTRUKSI]
Seorang perempuan sedang menggalaui apakah seseorang menyukai dia atau tidak. Ketimbang mencabut kelopak bunga untuk menghitung jika dia suka atau tidak, perempuan tersebut membuat sebuah program.

Function loveMeNot akan menerima satu parameter berupa array yang berisikan boolean.
Apabila jumlah true dalam array lebih besar dari jumlah false, maka function akan mereturn "HE LOVES ME!". Jika tidak, maka return "HE DOES NOT LOVE ME :(".
Jika jumlah true dan false sama, maka function akan me-return "GALAU".
Mudah bukan? :)

```output 
Simpan variabel decisions dengan tipe data boolean
Return 'HE LOVES ME!' jika jumlah true > false
'HE DOES NOT LOVE ME :(' jika jumlah false < true
'GALAU' jika true=false
```


```Javascript
function loveMeNot(decisions) {
  // Code here
  var benar = 0;
  var salah = 0;
  for (var i = 0; i < decisions.length; i++) {
    if (decisions[i] === true) {
      benar++;
    }
    if (decisions[i] === false) {
      salah++;
    }
  } if (benar === salah) {
    return 'GALAU';
  }
  else if (benar > salah) {
    return 'HE LOVES ME!';
  }
  else {
    return 'HE DOES NOT LOVE ME :(';
  }
}

// TEST CASES
console.log(loveMeNot([true, false, false])); // "HE DOES NOT LOVE ME :("
console.log(loveMeNot([true, true, false, false, true])); // "HE LOVES ME!"
console.log(loveMeNot([true, false])); // "GALAU"
console.log(loveMeNot([])); // "GALAU"
console.log(loveMeNot([false])); // "HE DOES NOT LOVE ME :("
```

**Contoh Soal 2 - Array Mastery: Pair Up**

[INSTRUKSI]
Setiap student di HACKTIV8 ditugaskan untuk membuat tim project dengan komposisi tim dua orang.
Kita membutuhkan sebuah program untuk membuat tim-tim tersebut.

Function pairUp akan menerima satu parameter berupa array yang berisi string nama student.
Function ini akan mengelompokkan setiap dua nama menjadi satu kelompok, dan apabila tersisa satu student, student terakhir akan bersama instruktur.
Hasil pengelompokkan adalah sebuah array yang berisi string berupa nama dua orang student sebagai satu tim.
Formatnya adalah <Nama Student 1> dan <Nama Student 2>.

```
output: ['Budi dan Badu', 'Indra dan Indri']

input: ['Budi', 'Badu', 'Indra', 'Indri', 'James']
output: ['Budi dan Badu', 'Indra dan Indri', 'James dan Instruktur']

input: [Simpan variabel Students berupa array dengan tipe data string
Return 2 nama dalam bentuk gabungan array dengan kata hubung 'dan'
Jika tidak habis dibagi 2 maka sisanya students berpasangan dengan Instruktur]
output: []
```
Simpan variabel Students berupa array dengan tipe data string
Return 2 nama dalam bentuk gabungan array dengan kata hubung 'dan'
Jika tidak habis dibagi 2 maka sisanya students berpasangan dengan Instruktur

```Javascript 
function pairUp(students) {
  // Code here
  var i;
  var kelompok;
  var newArr = [];
  for (i = 0; i < students.length-1; i+=2) {
    if (students.length % 2 === 0) {
    kelompok = students[i] + ' dan ' + students[i+1];
    } else if (students.length % 2 !== 0) {
      kelompok = students[i] + ' dan ' + students[i+1];
    } 
    newArr.push(kelompok);
  } 
  return newArr;
}
  
// TEST CASES
console.log(pairUp(['Budi', 'Badu'])); // ['Budi dan Badu']
console.log(pairUp(['Budi', 'Badu', 'Indra', 'Indri'])); // ['Budi dan Badu', 'Indra dan Indri']
console.log(pairUp(['Budi', 'Badu', 'Indra', 'Indri', 'James'])); // ['Budi dan Badu', 'Indra dan Indri', 'James dan Instruktur']
console.log(pairUp([])); // []

```
