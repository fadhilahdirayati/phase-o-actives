#JavaScript Data Types - Array

**Contoh Soal 1 - A in the Middle

[INSTRUKSI]
function aInTheMiddle adalah sebuah function yang menerima satu parameter yaitu sebuah array yang menampung string.
Function akan mengumpulkan semua string dalam array tersebut yang memiliki karakter di tengah yaitu 'a'. Abaikan kecil besar dari karakter.
Jika string genap, dua huruf di tengah harus 'a'.
Kumpulan string yang memiliki 'a' ditengah akan ditampung dalam array dan di kembalikan oleh function tersebut.


```output 
input: ['asafw', 'test', 'waw']
output: ['asafw', 'waw']

input: ['baon', 'test', 'taqs']
output: []

input: ['graail', 'nAn', 'naAn']
output: ['graail', 'nAn', 'naAn']

input: ['asafw', 'wow', 'o', 'graail', 'nAn']
output: ['asafw', graail', 'nAn']
```


```Javascript
function aInTheMiddle(words) {
  // Code here
  var satuKata = 0;
  var arrWords = [];
  
  for(var i = 0; i < words.length; i ++) {
    //console.log(words[i].length);
    satuKata = Math.floor((words[i].length-1)/2);
    //console.log(satuKata);
    if(words[i].length%2 !== 0) {
      if(words[i][satuKata] === 'a' || words[i][satuKata] === 'A') {
        //console.log(words[i]);
        arrWords.push(words[i]);
      }
    }
    if(words[i].length%2 === 0) {
      if(words[i][satuKata+1] === 'a' || words[i][satuKata+1] === 'A') {
        //console.log(words[i]);
        arrWords.push(words[i]);
      }
    }
  }
  return arrWords;
}

console.log(aInTheMiddle(['asafw', 'test', 'waw'])); // ['asafw', 'waw']
console.log(aInTheMiddle(['baon', 'test', 'taqs'])); // []
console.log(aInTheMiddle(['graail', 'nAn', 'naAn'])); // ['graail', 'nAn', 'naAn']
console.log(aInTheMiddle(['asafw', 'wow', 'o', 'graail', 'nAn'])); // ['asafw', graail', 'nAn']
console.log(aInTheMiddle([])); // []

**Contoh Soal 2 - Two Dimentional Array Generator


[INSTRUKSI]
function twoDimensionalGenerator adalah sebush function yang menerima satu parameter berupa angka.
Function akan mengembalikan sebuah array multidimensi - array yang berisikan array-array yang menampung string.
Array yang dikembalikan memiliki jumlah array di dalamnya sejumlah angka di parameter, dan setiap array di dalamnya akan menampung string 'X' sejumlah angka parameter juga.

WARNING: Harus dalam bentuk array, bukan string! hasil test case dibawah adalah visualisasi bentuk array, dan mungkin bisa sedikit berbeda di setiap console.


```
input: 2
output: [ [ 'X', 'X' ], [ 'X', 'X' ] ]

input: 4
output: [ [ 'X', 'X', 'X', 'X' ], [ 'X', 'X', 'X', 'X' ], [ 'X', 'X', 'X', 'X' ], [ 'X', 'X', 'X', 'X' ] ]

input: 1
output: [ ['X'] ]
```

```Javascript 

function twoDimensionalGenerator(count) {
  // Code here
  var arr = [];
  
  for(var i = 0; i < count; i ++) {
    //console.log (i);
    var arrIsi = [];
    var str = [];
    
    for(var j = 0; j < count; j ++) {
      str = 'X';
      //console.log(j);
      arrIsi.push(str);
    }
    arr.push(arrIsi);
  }
  return arr;
}

console.log(twoDimensionalGenerator(2)); // [ [ 'X', 'X' ], [ 'X', 'X' ] ]
console.log(twoDimensionalGenerator(4)); // [ [ 'X', 'X', 'X', 'X' ], [ 'X', 'X', 'X', 'X' ], [ 'X', 'X', 'X', 'X' ], [ 'X', 'X', 'X', 'X' ] ]
console.log(twoDimensionalGenerator(1)); // [ ['X'] ]
console.log(twoDimensionalGenerator(0)); // []

```
**Contoh Soal 3 - Credential Validator (Anchor with Rocket Score)**


[INSTRUKSI]
DILARANG MENGGUNAKAN Regex dan Match untuk soal ini!


function credentialValidator akan menerima tiga parameter berupa string, yakni username, email, dan password. Buatlah validasi tiga parameter tersebut dengan syarat berikut:

1. [ANCHOR] Username harus memiliki panjang minimal 4 karakter dan maksimal 20 karakter. Username tidak boleh mengandung simbol '*', '@', '#', '$', '%', '^', '&', dan '*'.

2. [ANCHOR] Password harus memiliki panjang minimal 5 karakter, dan harus mengandung kombinasi minimal 1 angka dan 1 huruf.

3. [ROCKET] Email harus memiliki panjang minimal 6 karakter, harus memiliki hanya satu simbol '@' dan memiliki nama email di sisi kiri simbol '@' dan memiliki domain di sisi kanan simbol '@'. Format: [NAMA EMAIL SISI KIRI]@[NAMA EMAIL].[DOMAIN].  domain harus memiliki hanya satu simbol '.' dimana sisi kiri maksimal 4 karakter, dan sisi kanan maksimal 3 karakter.

function akan me-return nilai true jika semua pengecekan terpenuhi, dan false jika minimal satu syarat tidak terpenuhi. Tambahan score bonus rocket apabila sukses melakukan validasi email.



```
input:
  - username: 'adhywiranata'
  - password: 'test123'
  - email: 'adhywiranata@coding.com'
output: true

input: 
  - username: 'adh'
  - password: 'test123'
  - email: 'adhywiranata@coding.com'

output: false, karena username dibawah 4 karakter

input: 
  - username: 'adhy test 123 testing 321 test 123 321 test'
  - password: 'test123'
  - email: 'adhywiranata@coding.com'

output: false, karena username melebihi 20 karakter

input: erwin@nice.com
input: 
  - username: 'erwin'
  - password: 'testing'
  - email: 'erwin@nice.com'

output: false, karena password tidak mengandung 1 angka sama sekali


```

```Javascript 

ffunction credentialValidator(username, password, email) {
  // Code here
  //cek username
  var arrSimbol = '*@#$%^&*';
  if (username.length >= 4 && username.length <= 20) {
    var cekSimbol = [];
    var simbol;
    for (var i = 0; i < username.length; i++) {
      simbol = arrSimbol.indexOf(username[i]);
      cekSimbol.push(simbol);
      cekSimbol.sort(function(a, b) {
        return b - a;
      });
    }
    if (cekSimbol[0] === -1) {
      //cek password
      var arrAngka = '1234567890';
      var cekAngka = [];
      var angka;
      for (var j = 0; j < password.length; j++) {
        angka = arrAngka.indexOf(password[j]);
        cekAngka.push(angka);
        cekAngka.sort(function(a, b) {
          return b - a;
        });
      }
      if (cekAngka[0] === -1) {
        return false + ', karena password tidak mengandung 1 angka sama sekali';
      } else {
        return true;
      }
      return true;
    } else {
      return (
        false +
        ", karena username mengandung simbol '*', '@', '#', '$', '%', '^', '&', dan '*'"
      );
    }
  } else {
    return false + ', karena username melebihi 20 karakter';
  }
}

console.log(
  credentialValidator('adhywiranata', 'test123', 'adhywiranata@coding.com')
);
console.log(
  credentialValidator(
    'adhy test 123 testing 321 test 123 321 test',
    'test123',
    'adhywiranata@coding.com'
  )
);
console.log(credentialValidator('erwin', 'testing', 'erwin@nice.com'));
...

