# Forward SSH key untuk remote server

Hari ini saya menemui masalah, remote server yang saya gunakan tidak bisa melakukan git clone. Hal ini disebabkan karena tidak memiliki ssh key untuk git clone ke github.

Berikut ini cara mem-forward SSH key dari komputer kita ke remote server.

```bash
ssh-add -L # untuk melihat apakah key yang dibutuhkan sudah ditambahkan
ssh-add ~/.ssh/id_rsa
ssh username@alamat-ip-server.com
```
