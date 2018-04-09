# ARRAY

# Contoh Soal - Array Mastery: Circular Operation

[INSTRUKSI]
Akan dijalankan sebuah operasi matematika dengan urutan kali (+) dan kurang (-).

Function circularOperation akan menerima satu parameter berupa array angka, dan memproses satu per satu angka tersebut.
Proses yang dilakukan adalah mengoperasikan setiap bilangan didalamnya, menggunakan simbol +, dan - berturut-turut.
Simbol akan berotasi kembali ke + jika operasi - sudah dilakukan, sampai semua angka selesai di proses.

Gambaran Proses:
0 + angka pertama - angka kedua + angka ketiga - angka keempat + angka kelima - angka keenam + ... (dan seterusnya)


Function akan mereturn hasil kalkulasi dari operasi tersebut.
Jika tidak ada angka yang diberikan, function akan me-return 0.

Aturan: proses operasi satu per satu, dan TIDAK ADA aturan matematika yang harus memproses * sebelum + / !


```Output
input: [1, 2, 3, 4, 5]
proses: 0 + 1 - 2 + 3 - 4 + 5
output: 3

input: [5, 4, 3, 2, 1, 2]
proses: 0 + 5 - 4 + 3 - 2 + 1 - 2
output: 1

input: [1, 1, 1, 1]
proses: 0 + 1 - 1 + 1 - 1
output: 0

input: []
```
Simpan variabel number bentuk array tipe data angka
Return hasil operasi + dan - secara bergantian dari variabel tersebut


```Javascript
function circularOperation(numbers) {
  // Code here
  var hasil = 0;
  
  for (var i = 0; i < numbers.length; i++) {
    if(i%2 === 0) {
      hasil += numbers[i];
    }
    else{
      hasil -= numbers[i];  
    }
  }
  return hasil;
}
  
// TEST CASES
console.log(circularOperation([1, 2, 3, 4, 5])); // 3
console.log(circularOperation([5, 4, 3, 2, 1, 2])); // 1
console.log(circularOperation([1, 1, 1, 1])); // 0
console.log(circularOperation([0, 10, 2, 5, 7])); // -6
console.log(circularOperation([])); // 0
```

# Contoh Soal 2 - Array Mastery: Group Odd Evens

[INSTRUKSI]
Function groupOddEven akan menerima satu parameter berupa array yang berisi number.
Function akan mengelompokkan setiap number yang ganjil (odd) dan setiap number yang genap (even),
dan akan mereturn sebuah string dengan format berikut:

"ODDS: <OddNum1>,<OddNum2>,<OddNum3> EVENS: <EvenNum1>,<EvenNum2>,<EvenNum3>"

aturan:
  - Apabila tidak ada angka ganjil, hanya tampilkan:
  "EVENS: <EvenNum1>, <EvenNum2>"
  - Apabila tidak ada angka genap, hanya tampilkan:
  "ODDS: <OddNum1>, <OddNum2>"
  - Apabila tidak ada angka sama sekali, tampilkan string kosong!
  - Angka tidak perlu diurutkan!
  
```Output
input: [1, 5, 8, 2, 3]
output: "ODDS: 1, 5, 3 EVENS: 8, 2"

input: [1, 1, 1]
output: "ODDS: 1, 1, 1"

input: [2, 8, 10]
output: "EVENS: 2, 8, 10"
```
Simpan variabel students dalam bentuk array tipe data angka
Return angka ganjil masuk ke ODDS dan angka genap masuk ke EVENS


```Javascript
function groupOddEven(students) {
  // Code here
  var odds = [];
  var evens = [];
  var hasil1 = '';
  var hasil2 = '';
  
  if(students.length === 0) {
    return '""';
  }
  else {
    for(var i = 0; i < students.length; i ++) {
      if(students[i]%2 === 0) {
        evens.push(students[i]);
        hasil1 = 'EVENS : ' + evens +'"';
      } 
      else if(evens.length === 0) {
        hasil1 = '"';
      }
      else{
        hasil1 = ' EVENS : ' + evens +'"';
      }
      if(students[i]%2 !== 0) {
        odds.push(students[i]);
        hasil2 = '"ODDS : ' + odds;
      }
      else if(odds.length === 0){
        hasil2 = '"';
      }
    }
    return hasil2 + hasil1;
  }
}
  
// TEST CASES
console.log(groupOddEven([1, 5, 8, 2, 3])); // "ODDS: 1, 5, 3 EVENS: 8, 2"
console.log(groupOddEven([1, 1, 1])); // "ODDS: 1, 1, 1"
console.log(groupOddEven([2, 8, 10])); // "EVENS: 2, 8, 10"
console.log(groupOddEven([2, 111])); // "ODDS: 111 EVENS: 2"
console.log(groupOddEven([])); // ""
```

