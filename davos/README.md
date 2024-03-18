
# DAVOS
## Concept
WebDAV-enabled application with public and private (password-protected) endpoint.

## Solution
- Terdapat sebuah web server yang menyediakan flag dalam bentuk iframe
- Ketika kita cek file health_check.php dalam Inspect Element, terlihat bahwa program dijalankan dalam localhost:8888. Ketika kita coba akses web tadi dengan port 8888, ternyata kita dapat mengakses file lokal dalam web server.
- Isi folder public sama dengan web server tadi, tetapi kita bisa mendapatkan file php tadi secara utuh, jadi kita bisa melihat isi dari health_check.php
- jadi akses web dengan port 8888 lalu tambahkan /health_check.php ( sesuai yang didapat dalam inspect yang pertama ) dan langsung terdownload
- di dalam health_check.php kita bisa lihat ada username dan password

```php
      $settings = array(
        'baseUri' => 'http://davos/restricted/',
        'userName' => 'user',
        'password' => 'bdChWzznlMlVOEBXmIkjiuJJIE9htIav',
        'proxy' => '',
    );
```
- Untuk mengakses folder restricted, kita perlu username dan password
- Kita bisa login dengan kredensial yang sudah kita dapatkan di health_check.php, lalu kita bisa baca file flag.txt
- 
```bash
  LKS{ther3s_so_much_tech_gotta_c4tch_dav_all_10101030}
```