Kita dapat men-disable index dalam postgres untuk sementara dengan cara

```
update pg_index set indisvalid = false where indexrelid = 'nama_index_di_table'::regclass
```

dan untuk men-enable kembali dengan cara

```
update pg_index set indisvalid = true where indexrelid = 'nama_index_di_table'::regclass
```
