# Crack_me
## Deskripsi Soal
crack me using IDA or something else.......... ( decompile maybe ehe )

---

## Solution
- Diberikan sebuah executable binary crack_me yang menerima user input berupa kata sandi.
- Analisis lebih lanjut pada kode hasil dekompilasi menunjukkan bahwa terdapat fungsi validate_code() yang mendeklarasikan beberapa constraints dari setiap char yang dimasukkan.
- Selain itu terdapat fungsi validate_pin() yang mana mendeklarasikan beberapa constraint pengecekan pin.
- Untuk mempermudah proses pengerjaan, cukup masukkan list constraint yang ada menggunakan python-z3.
## FLAG
```bash
  LKS2021{simpl3_p4sscrack_us1ng_z3}
```