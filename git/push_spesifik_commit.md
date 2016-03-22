# Push Spesifik Commit

Suatu ketika, saat sedang bekerja, ada laporan bug yang datang. Padahal ada beberapa commit yang belum di push. Ada solusi untuk push hanya commit untuk fixing bug.

```
$ git rebase -i HEAD~3 #ganti 3 dengan jumlah commit yang akan di-edit

# di dalam rebase interactive, pindahkan commit yang akan di push ke baris teratas, lalu keluar dari editor

$ git pull --rebase    # jika dibutuhkan
$ git push <remote_name> <commit_SHA>:<local_branch> # git push origin 8974859:master
```

Selesai.
