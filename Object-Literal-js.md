# JavaScript Object Literal

## Objectives

- ▢ Memahami pembuatan object sebagai pair key: value tanpa menggunakan class

### Object

JavaScript merupakan bahasa pemrograman yang berbasis simple-object (Objek sederhana). Objek adalah kumpulan tidak berurut yang merangkai beberapa property dan property memiliki nama/key dan value (key-value pairs).

Objek dalam JavaScript, sama seperti banyak bahasa pemrograman lainnya, bisa dibandingkan dengan objek dalam kehidupan nyata.

Untuk membuat sebuah object literal bisa dengan cara menuliskan kurung kurawal (curly braces) kemudian menuliskan nama property yang harus memiliki keyName dan value.

```javascript
var myObj = {
  myKey: 'myValue'
};
```


Value dalam object literal selain string bisa juga dengan memasukkan value array bahkan value object literal lainnya.

Kita bisa coba dengan kode berikut:

```javascript
var supermanObj = {
  id: "1a2b3c",
  name: "Superman",
  age: 200,
  favorites: [
    "coding",
    "reading",
    {
      sports: ["parkour", "hill climbing"]
    }
  ],
  address: {
    street: "Planet Krypton",
    zipCode: 54213
  }
};

console.log(supermanObj.name); // "Superman"
console.log(supermanObj.age); // 200
console.log(supermanObj.favorites[0]); // "coding"
console.log(supermanObj.favorites[2].sports); // ["parkour", "hill climbing"]
console.log(supermanObj.favorites[2].sports[0]); // "parkour"
console.log(supermanObj.address); // {street: "Planet Krypton", zipCode: 54213}
console.log(supermanObj.address.zipCode); //54213
```
contoh lain :


#### PASSWORD GENERATOR

#### `[INSTRUCTIONS]`

passGen adalah sebuah function yang menerima tiga parameter berupa firstName, email, dan age.
Function akan mengambil bagian-bagian dari ketiga parameter menjadi satu kesatuan string baru,
dengan ketentuan:

output: [3 huruf pertama dari firstName][Semua huruf sebelum simbol @ di email][age]

Jika firstName dibawah 3 huruf, hentikan function dan kembalikan string berupa 'NAME IS INVALID!'

#### `[CONSTRAINTS]`
Dilarang menggunakan sintaks .split(), .slice(), .splice(), .join(), .push(), dan .concat().
Soal ini hanya membutuhkan operasi string (mengakses index dari string tentunya diperbolehkan)!
Dilarang menggunakan segala bentuk regex (match, test, dan lain-lain)


#### `[EXAMPLE]`
passGen('john', 'hello@john.com', 25)

proses:

- 3 huruf pertama dari firstName: 'joh'
- semua huruf sebelum simbol @ di email: 'hello'
- age: 25

output: 'johhello25'

EXPLAIN YOUR LOGIC BELOW! (Required) 
Tidak harus formal pseudocode, tapi bagaimana step by step logikanya
Nilai tidak valid (0) jika logic dan code berbeda!


````Javascript

function passGen(firstName, email, age) {
 var tampung = ''// penampung 3 karakter pertama pada nama + nama email yang sudah dipotong
 var tampungEmail ='';
 var tampungSampah = '';
 
 for(i=0;i<=2;i++){// mencari 3 karakter awal nama pindahkan ke tampung
 	tampung+=firstName[i];
 }
 for(j=0;j<email.length;j++){//mencari nama awal di email
 	tampungEmail+'.' // tambahkan titik untuk clearing
 	if(email[j] === '@' ){ // menambahkan nama ke dalam tampung
 		tampung+=tampungEmail
 		tampungEmail = ''
 	} else if(email[j] === '.'){ // if clearing
 		tampungEmail = ''
 	} else {
 		tampungEmail+=email[j] // if penambahan hurup email
 	}
 }
if(firstName.length<=3){// jika nama dibawah 3 karakter
	return 'NAME IS INVALID!'
}
return tampung+age // 
}

console.log(passGen('john', 'hello@gmail.com', 15)); // 'johhello15' 
console.log(passGen('mickey', 'mike@gmail.com', 1)); // 'micmike1'
console.log(passGen('a', 'hello@gmail.com', 15)); // 'NAME IS INVALID!'
console.log(passGen('rudy', 'rud@rudy.co.id', 22)); // 'rudrud22'
console.log(passGen('bejo', 'zetta@bejo.gov', 50)); // 'bejzetta50'
````

Kamu dapat mencoba kode di atas [di sini](http://jsbin.com/diruxiq/edit?js,console)

<!-- ### BONUS: JSON

JSON adalah format pertukaran data (data-interchange) yang ringan (lightweight), mudah bagi manusia untuk membaca dan menulisnya, mudah juga bagi mesin/komputer untuk mengurai (parse) dan hasilkan (generate). Win win! :star2:

JSON dibasiskan sebagai subset dari JavaScript.
Walaupun berhubungan, JSON adalah format teks yang independen tapi menggunakan konvensi atau aturan yang familiar untuk programmer dari bahasa keluarga C seperti C++, C#, Java, JavaScript, Perl, Python, dan banyak lainnya. Jadi kita bisa gunakan JSON tanpa JavaScript.
Properti ini menjadikan JSON bahasa pertukaran data yang ideal, mampu untuk menyimpan maupun mentransfer/mengirim data ke mana saja. Keren! :sunglasses:

Mari kita ulang sebentar. Seperti object JavaScript, JSON dibuat dengan dua struktur yang mirip:

- Kumpulan/koleksi pasangan nama kunci dan nilai. Dalam beberapa bahasa, ini dibuat sebagai object, record, struct, dictionary, hash table, keyed list, atau associative array. Maka dari itu ada berbagai cara untuk membuat JSON, selain di JavaScript.
- Deretan nilai yang berurutan. Dalam kebanyakan bahasa, bisa dibuat sebagai array, vector, list, atau sequence.

JSON juga merupakan objek biasa yang berisi dua fungsi utama:

- `parse()`: parse atau translate, untuk menerjemahkan atau menganalisis JSON dalam hal in terms of aturan tata bahasa, mengidentifikasi bagian perkataan, hubungan secara sintaks, dll.
- `stringify()`: membuat teks JSON.

Dalam JSON, kita bisa gunakan tipe data apapun juga. Kombinasikan String, Number, Array, dan lainnya. Buatlah nama kunci sebaiknya sebagai String.

```javascript
{
  "animals": [
    {
      "species": "lion",
      "rank": 1,
      "alive": true
    },
    {
      "species": "tiger",
      "rank": 2,
      "alive": true
    },
    {
      "species": "jaguar",
      "rank": 3,
      "alive": false
    },
    {
      "species": "leopard",
      "rank":null,
      "alive":null
    }
  ]
}
```
contoh lain:

#### PASSWORD GENERATOR

#### `[INSTRUCTIONS]`

passGen adalah sebuah function yang menerima tiga parameter berupa firstName, email, dan age.
Function akan mengambil bagian-bagian dari ketiga parameter menjadi satu kesatuan string baru,
dengan ketentuan:

output: [3 huruf pertama dari firstName][Semua huruf sebelum simbol @ di email][age]

Jika firstName dibawah 3 huruf, hentikan function dan kembalikan string berupa 'NAME IS INVALID!'

#### `[CONSTRAINTS]`
Dilarang menggunakan sintaks .split(), .slice(), .splice(), .join(), .push(), dan .concat().
Soal ini hanya membutuhkan operasi string (mengakses index dari string tentunya diperbolehkan)!
Dilarang menggunakan segala bentuk regex (match, test, dan lain-lain)


#### `[EXAMPLE]`
passGen('john', 'hello@john.com', 25)

proses:

- 3 huruf pertama dari firstName: 'joh'
- semua huruf sebelum simbol @ di email: 'hello'
- age: 25

output: 'johhello25'

EXPLAIN YOUR LOGIC BELOW! (Required) 
Tidak harus formal pseudocode, tapi bagaimana step by step logikanya
Nilai tidak valid (0) jika logic dan code berbeda!


````Javascript

function passGen(firstName, email, age) {
 var tampung = ''// penampung 3 karakter pertama pada nama + nama email yang sudah dipotong
 var tampungEmail ='';
 var tampungSampah = '';
 
 for(i=0;i<=2;i++){// mencari 3 karakter awal nama pindahkan ke tampung
 	tampung+=firstName[i];
 }
 for(j=0;j<email.length;j++){//mencari nama awal di email
 	tampungEmail+'.' // tambahkan titik untuk clearing
 	if(email[j] === '@' ){ // menambahkan nama ke dalam tampung
 		tampung+=tampungEmail
 		tampungEmail = ''
 	} else if(email[j] === '.'){ // if clearing
 		tampungEmail = ''
 	} else {
 		tampungEmail+=email[j] // if penambahan hurup email
 	}
 }
if(firstName.length<=3){// jika nama dibawah 3 karakter
	return 'NAME IS INVALID!'
}
return tampung+age // 
}

console.log(passGen('john', 'hello@gmail.com', 15)); // 'johhello15' 
console.log(passGen('mickey', 'mike@gmail.com', 1)); // 'micmike1'
console.log(passGen('a', 'hello@gmail.com', 15)); // 'NAME IS INVALID!'
console.log(passGen('rudy', 'rud@rudy.co.id', 22)); // 'rudrud22'
console.log(passGen('bejo', 'zetta@bejo.gov', 50)); // 'bejzetta50'
````

contoh lain:

```javascript
{
  "id": "1a2b3c",
  "name": "Superman",
  "age": 200,
  "favorites": [
    "coding",
    "reading",
    {
      "sports": ["parkour", "hill climbing"]
    }
  ],
  "address":{}
}
``` -->



### References

- [JavaScript Objects on W3Schools](http://www.w3schools.com/js/js_objects.asp)
- [Working with objects, on MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Working_with_Objects)
<!-- - [JSON.org](http://json.org)
- [JSON Parser Online](http://json.parser.online.fr) -->

