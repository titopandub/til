# Menggabungkan Beberapa Command dalam Command Mode Vim

Dalam Vim kita diberikan sebuah mode untuk menulis command, misalnya `:e <nama file>` untuk membuat atau membuka file ke dalam buffer. Ada cara untuk menggabungkan beberapa command tersebut (chaining) sekaligus.

`:vsp | :A`

Command di atas akan membuka vertical split dan akan membuka file spec / test dari file yang sedang terbuka (jika menggunakan vim-rails).
