# Mengganti MAC Address

Kecepatan internet jadi lambat karena kena block server? Ganti MAC address terus restart WIFI network. Caranya:

```bash
openssl rand -hex 6 | sed 's/\(..\)/\1:/g; s/.$//' | xargs sudo ifconfig en0 ether
```

Command ini akan menghasilkan random hex dan memformatnya dengan format MAC Address (`AA:BB:CC:DD:EE:FF`) dan mengganti en0 (WIFI) dengan MAC address random.

sumber: https://www.howtogeek.com/220462/how-to-find-and-change-your-mac-address-on-os-x/
