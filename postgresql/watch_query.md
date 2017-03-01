Kita dapat melihat suatu query dijalankan terus menerus dalam satu satuan waktu (detik) dengan command `\watch`

```
postgres=>select count(1) from users;
 count 
-------
 24875
(1 row)

postgres=>\watch
Watch every 5s  Tue May 26 17:42:00 2015
 count 
-------
 24875
(1 row)

Watch every 5s  Tue May 26 17:42:05 2015
 count 
-------
 24890
(1 row)
```

source: http://www.fishscript.com/?d=1684
