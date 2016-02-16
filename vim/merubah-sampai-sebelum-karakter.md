# Merubah Beberapa Karakter Sampai Sebelum Karakter Tertentu

Di Vim ada shortcut yang sangat sederhana untuk merubah beberapa karakter sampai dengan satu karakter sebelum karakter yang kita tentukan.

`ct<karakter>`

Command ini dapat dijalankan saat berada di normal mode. Misalnya `publishSubscribe`, untuk merubah `publish`, kita cukup menaruh kursor di `p` dan menekan `ctS` untuk merubahnya. Maksud dari command ini adalah `change to <karakter>`. Perbedaanya dengan `cfS` adalah `cf<karakter>` akan mengikutsertakan `S` dalam perubahan tersebut.
