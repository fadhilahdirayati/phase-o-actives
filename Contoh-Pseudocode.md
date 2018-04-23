# Pseudocode Challenge

Soal ini terdiri dari 4 nomor!

## 1. Newton Second Law

Bunyi hukum II Newton adalah:

```
Percepatan sebuah benda akan sebanding dengan gaya yang diberikan pada benda dan berbanding terbalik dengan massa benda. Arah percepatan benda sama dengan arah gaya total yang diberikan pada benda.

```

Secara matematis hukum II Newton dirumuskan sebagai berikut:
ΣF = m x a

ΣF = resultan gaya (Newton)

m = massa benda (kg)

a = percepatan benda (m/s2)

Berdasarkan keterangan di atas, buatlah sebuah algoritma / pseudocode untuk menghitung resultan gaya pada sebuah mobil yang memiliki massa benda 600 kg dan ketika didorong oleh tiga orang percepatannya adalah 2 m/s2!

```Pseudocode 
  STORE "resultan" without any values
  STORE "m" with 600
  STORE "a" with 2
  CALCULATE "resultan" AS m*a
  DISPLAY "resultan"
```

## 2. Tahun Kabisat

Apa yang kamu ketahui tentang tanggal 29 Februari? Kamu pasti tahu jika suatu tahun memiliki tanggal 29 Februari berarti tahun tersebut merupakan tahun kabisat.

Dalam kalender Gregorian, tahun kabisat memiliki beberapa kriteria yaitu antara lain:
 - Jika tahun habis di bagi 4 dan tidak habis di bagi 100, dan
 - Jika tahun habis di bagi 4, habis di bagi 100 dan habis di bagi 400

Buatlah algoritma/pseudocode untuk menentukan apakah suatu tahun merupakan tahun kabisat atau bukan!

```Pseudocode 
STORE year with any value
IF year module 4 is 0 THEN
    IF year module 100 is 0 THEN
        DISPLAY "`year is leap year"
    ELSE IF year module 400 is 0 THEN
        DISPLAY "year is leap year"
    ELSE
        DISPLAY "year is not leap year"
ENDIF
```

## 3. Laundry Day

Foxie akan mencuci pakaiannya menggunakan mesin cuci. Pakaian yang akan dicuci oleh Foxie sebanyak 20 dan akan dimasukkan ke mesin cuci.
Mesin cuci akan dinyalakan jika semua pakaian Foxie sudah masuk ke mesin cuci.

Bantulah Foxie untuk menghitung jumlah pakaian yang akan dimasukkan ke mesin cuci menggunakan algoritma / pseudocode perulangan!

```Pseudocode 
STORE "clothes" with 0

WHILE "clothes" < 20
  ADD "clothes" by 1

DISPLAY "washing machine on !"
```


## 4. Periksa Kuku

Seorang guru akan memeriksa kuku siswa-siswinya yang sebanyak 40 orang dengan cara berkeliling kelas. Jika guru menemukan siswa/siswi yang memiliki kuku yang panjang maka guru akan menghukum siswa/siswi tersebut, jika tidak guru akan memuji siswa/siswi tersebut.

Buatlah algoritma/pseudocode untuk permasalahan diatas.

```Pseudocode 
STORE "students" with 40

IF nails long THEN
    DISPLAY "get punishment"
 ELSE
    DISPLAY "get compliment"
END IF

```


## 5. Buatlah sebuah algoritma/pseudocode untuk kasus berikut:

Seorang anak akan dibelikan mainan jika nilai sekolahnya bagus. List mainan yang
akan dibelikan oleh orang tuanya tergantung dengan nilai-nya.

* Range Nilai 90 - 100 akan mendapatkan hadiah `RASTAR-MOTORCYCLE BMW RED`
* Range Nilai 70 - 89 akan mendapatkan hadiah `HALO ROBOTICS-SPHERO STAR WARS`
* Range Nilai 50 - 69 akan mendapatkan hadiah `Die Cast`
* Range 50 ke bawah tidak akan mendapatkan apapun

NOTE:
Range nilai hanya dari 0 - 100, jika nilai kurang dari itu atau lebih maka tampilkan 'Invalid Score'

```Pseudocode 
STORE nilai with any value
STORE Hadiah without value

IF nilai >= 90 AND nilai <=100 THEN
     DISPLAY `RASTAR-MOTORCYCLE BMW RED` to 'hadiah'
  ElSE IF nilai >=70 AND nilai <=89 THEN
     DISPLAY `HALO ROBOTICS-SPHERO STAR WAR` to 'hadiah'
  ElSE IF nilai >=50 AND nilai <=69 THEN   
    DISPLAY `Die Cast` to 'hadiah'
  ELSE nilai <0 OR nilai >100 THEN 
    DISPLAY 'Invalid Score'
END IF 
```

## 6. Buatlah sebuah algoritma untuk kasus berikut:

Sebuah game memiliki hero dan hero tersebut memiliki atribut level dan damage.
Damage dari hero tergantung dari levelnya, perhitungan damage akan mengikuti aturan berikut:
- Damage Hero Level 1-15: level dikalikan 2
- Damage Hero Level 16-20: (level dikalikan 2) + 5
- Damage Hero Level 21-25: (level dikalikan 2) + 10
- Selain level yang disebutkan di atas, tampilkan "Invalid level" dan hentikan program

Lalu tampilkan damage hero berdasarkan levelnya sekarang

```Pseudocode 
STORE level with anyvalue
STORE DamageHero without anyvalue
STORE Damage without anyvalue

IF level >=1 AND  <=15 THEN
    DISPLAY Damage Her
    DamageHero = Damage times 2
 ELSE IF level >=16 AND <=20 THEN
    DamageHero = 

```
