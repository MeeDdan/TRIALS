+----------------+       +---------------------+       +------------------+
|    Member      |       | Nomor HP Member     |       |     Mobil        |
+----------------+       +---------------------+       +------------------+
| id_member (PK) |<----->| id_nomor_hp (PK)    |       | id_mobil (PK)    |
| nama_member    |       | nomor_hp            |       | no_polisi        |
| alamat_member  |       | id_member (FK)      |       | merk_jenis_mobil |
+----------------+       +---------------------+       | warna_mobil      |
                         |                         |       | no_rangka_mesin  |
                         |                         |       +------------------+
                         |                         |
                         |                         |
                    +------------+         +-------------------+ 
                    |  Layanan   |         |    Transaksi      |
                    +------------+         +-------------------+
                    | id_layanan (PK) |<--->| id_transaksi (PK) |
                    | jenis_layanan   |     | id_member (FK)    |
                    | tarif_layanan   |     | id_mobil (FK)     |
                    +-----------------+     | id_layanan (FK)   |
                                             | tanggal_cuci      |
                                             | jam_drop_off      |
                                             | jam_pick_up       |
                                             +-------------------+
                                                    |
                                                    |
                                             +------------------+
                                             |  Petugas         |
                                             +------------------+
                                             | id_petugas (PK)  |
                                             | nama_petugas     |
                                             | alamat_petugas   |
                                             | no_hp_petugas    |
                                             +------------------+
                                                    |
                                                    |
                                          +------------------------+
                                          | Penanganan oleh Petugas|
                                          +------------------------+
                                          | id_transaksi (FK)      |
                                          | id_petugas (FK)        |
                                          +------------------------+
