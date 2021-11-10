# [Challenge 1116](https://ctflearn.com/challenge/1116)

Kita disuguhkan web seperti ini 

![](/ctflearn/web/assets/1116.png)

Di website itu terdapat banyak sekali clue, salah satunya adalah **Gobustme**. 

_note: gobuster adalah tool yang di pakai untuk mencari direktori yang ada di website._

lalu kita cari flag tersebut dengan menggunakan gobuster menggunakan payload yang sudah saya buat.

```
gobuster dir -e -u https://gobustme.ctflearn.com/ -w /usr/share/wordlists/dirb/common.txt -s 200 -b 404 -o ctflearn.txt
```

dir     : directory/file enumeration mode

-e      : enumerate directories

-u      : target url

-w      : wordlist

-s      : status code

-b      : negative status code

-o      : output file

lalu cek outputnya

![gambar](/ctflearn/web/assets/1116_2.png)

buka website tersebut satu satu dan lihat apakah flagnya ada di dalamnya.

![gambar](/ctflearn/web/assets/1116_3.png)