# Login
## Deskripsi Soal
yok login yok... ( btw ini natip natip anget ehe )

---

## Solution
- strcmp() php vuln
- Fungsi strcmp() membandingkan dua string, perlu diperhatikan bahwa fungsi strcmp() peka huruf besar-kecil.
- contoh sintax nya seperti ini
```php
  strcmp("HackThePlanet!","HackThePlanet!")
```
- strcmp() akan memberikan return 0 jika kedua nilai var sama, <0 jika var1 lebih kecil, >0 jika var2 lebih kecil. 
- Namun ada masalah pada strcmp(). function ini akan selalu memberikan return 0 jika kedua variable dimasukkan type array.
- secara normal, kita harus memasukkan password melalui POST untuk mendapatkan return value 0. Seperti berikut:
- http://localhost:8000?password=a
- Namun autentikasi ini bisa dibypass dengan mengirimkan password dalam bentuk array. seperti berikut.
- http://localhost:8000?password[]=b
- lebih mudah ny bisa pake di postman bro
## FLAG
```bash
  LKS{MeNyAlAa_AbAnGkUhHhH}
```