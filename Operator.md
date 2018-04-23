## Operator

Operator adalah karakter yang merepresentasikan sebuah tindakan. Kita sering menemukan operator seperti + (tambah),
 x (kali), dan lain-lain. Namun, di dunia programming, operasi kali kita gantikan dengan simbol * (asterisk) dan operasi bagi dengan simbol / (slash)

Operator dibagi menjadi beberapa tipe:

**Arithmetic Operator**
Arithmetic operator adalah operator yang melibatkan operasi matematika, seperti penambahan, pengurangan, perkalian, dan lain-lain.

- Tambah (+)
- Kurang (-)
- Kali (\*)
- Bagi (/)
- Modulus (%)

Bagi kamu yang baru kali ini mendengar tentang modulus, modulus adalah sisa bagi. Misalkan kita membagi 7 dengan 2. Hasil bagi nya adalah 3, namun sisa dari hasil baginya adalah 1. Bilangan yang memang habis dibagi, sisa hasil baginya adalah 0.

Contoh sederhana penggunaan modulus:

```javascript
> 4 % 2 // 4 modulus 2
> 0 // bilangan 4 habis dibagi 2, sehingga 4 modulus 2 menghasilkan nilai 0
> 5 % 2 // 5 modulus 2
> 1 // bilangan 5 habis tidak habis dibagi 2, sehingga 5 modulus 2 menghasilkan nilai 1, sisa dari hasil pembagian
```

**Assignment Operator**
Assignment operator adalah operator yang meng-"assign", atau memberikan nilai. Biasanya, assignment operator digunakan untuk memberikan nilai kepada sebuah variable.

```javascript
var bilangan;
bilangan = 5; // Contoh assignment value 5 ke sebuah variable
```

**Comparison Operator**
Comparison operator adalah operator yang membandingkan satu nilai dengan nilai lainnya. Hasil operasi yang melibatkan comparison operator adalah antara 'true' atau 'false'.

- Equal operator (==)

```javascript
var angka = 8;
console.log(angka == 8); // true
console.log(angka == 1); // false
```

- Not Equal operator (!=)

```javascript
var angka = 8;
console.log(angka != 7); // true
console.log(angka != 8); // false
```

- Strict Equal operator (===)

Sedikit berbeda dengan equal operator, strict operator `===` mewajibkan nilai yang dibandingkan sama dan tipe data nya pun harus sama. Sedangkan pada `==`, `8` dan `"8"` akan dianggap sama, karena itu menghasilkan nilai `true`.

```javascript
var angkaBeda = "8";
console.log(angkaBeda == 8); // true
console.log(angkaBeda === 8); // false
console.log(angkaBeda === "8"); // true
```

- Strict Not Equal operator (!==)

Sedikit berbeda dengan not equal operator, strict not equal operator `!==` mewajibkan nilai yang dibandingkan tidak sama dan tipe data nya pun harus sama. Sedangkan pada `!=`, `8` dan `"8"` akan dianggap sama, karena itu menghasilkan nilai `false`.

```javascript
var angkaBeda = "8";
console.log(angkaBeda != 7); // true
console.log(angkaBeda !== 7); // true
console.log(angkaBeda !== 8); // true
console.log(angkaBeda !== "8"); // false
```

- Less Than (<) / Greater Than (>)

operator selanjutnya adalah `<`, yaitu kurang dari sekian, dan `>`, yaitu lebih dari sekian.

```javascript
var angka = 8;
console.log(angka > 7); // true
console.log(angka < 6); // false
console.log(angka <= 8); // true
```

**Conditional Operator**
Conditional operator adalah operator yang akan mengevaluasi kebenaran dari nilai yang dikomputasi.

- OR (||): akan menghasilkan nilai `true` jika salah satu premis mengandung `true`

```javascript
console.log(true || true); // true
console.log(true || false); // true
console.log(true || false || false); // true
console.log(false || false); // false
```

- AND (&&): akan menghasilkan nilai `true` jika kedua premis `true`.

```javascript
console.log(true && true); // true
console.log(true && false); // false
console.log(false && false); // false
console.log(false && true && true); // false
console.log(true && true && true); // true
```
