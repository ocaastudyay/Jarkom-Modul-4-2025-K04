# Jarkom-Modul-4-2025-K04

Anggota :
| Nama | NRP |
| -------------------- | ---------- |
| Diva Aulia Rosa | 5027241003 |

## Prefix IP
 `192.213`

## Topologi Awal CPT
<img width="1096" height="740" alt="Topologi Awal Modul 4" src="https://github.com/user-attachments/assets/9125d5c9-f82f-49c6-ab70-b246a9a9f642" />

## Topologi CPT Tahap 1
<img width="1230" height="862" alt="Topologi VLSM Tahap 1" src="https://github.com/user-attachments/assets/622c0294-ba27-472b-874a-915bcc665830" />

## Topologi CPT Penjumlahan Host & Penentuan Prefix
<img width="1230" height="862" alt="paling baru" src="https://github.com/user-attachments/assets/802dd951-9e23-4e8e-a4ef-53ec9554dfc7" />

## Tabel Pembagian Rute
| Nama Subnet | Rute                                                                 | Host + Gateway | Netmask | Jumlah Host |
|-------------|----------------------------------------------------------------------|----------------|---------|-------------|
| A1          | Morgoth > Switch > Erendis > Switch > Elrond                         | 62             | /26     | 61          |
| A2          | Throne > Erebor                                                      | 2              | /30     | 1           |
| A3          | Amorth > Switch > Morgoth > Switch > Throne                          | 4              | /29     | 3           |
| A4          | Anor > Switch > Beacon > Switch > Silmarils                          | 661            | /22     | 660         |
| A5          | Minastir > Amorth                                                    | 2              | /30     | 1           |
| A6          | Minastir > Anor                                                      | 2              | /30     | 1           |
| A7          | Amonsul > Minastir                                                   | 2              | /30     | 1           |
| A8          | Amonsul > Eregion                                                    | 2              | /30     | 1           |
| A9          | Amonsul > Fornost                                                    | 2              | /30     | 1           |
| A10         | Fornost > Switch > Valinor > Switch > Valmar                         | 4              | /29     | 3           |
| A11         | Valinor > Switch > Shadow > Switch > Anarion > Switch > Lindon       | 299            | /23     | 298         |
| A12         | Valmar > Switch > Doriath > Switch > Amor                            | 28             | /27     | 27          |
| A13         | Valmar > Switch > Imrahil > Switch > Utumno > Switch > Gwaith        | 34             | /26     | 33          |
| A14         | Eregion > Switch > Markwood > Switch > Morgul                        | 126            | /25     | 125         |
| A15         | Guldur > Switch > Palantir > Switch > Edhil                          | 120            | /25     | 119         |
| A16         | Guldur > Switch > IronCrwon > Switch > Grond > Switch > Hobbiton     | 14             | /28     | 13          |
| A17         | Numenor > Switch > Arthedain > Switch > Mirdain                      | 875            | /22     | 874         |
| A18         | Mordor > Erain                                                       | 2              | /30     | 1           |
| A19         | Erain > Switch > Melkor > Switch > Khazad                            | 503            | /23     | 502         |
| A20         | Erain > Switch > Balrog > Switch > Gothmog > Switch > Thranduil      | 470            | /23     | 469         |
| A21         | Numenor > Mordor                                                     | 2              | /30     | 1           |
| A22         | Guldur > Numenor                                                     | 2              | /30     | 1           |
| A23         | Eregion > Numenor                                                    | 2              | /30     | 1           |
| **Total**   |                                                                      | **3220**       | **/20** | **3197**    |

Jika menurut Jumlah Host yang dibutuhkan maka IP awal adalah `192.213.0.0/20` tetapi pada data kebutuhan host yang paling besar adalah pada prefix `/22` maka untuk pembagian IP VLSM akan dimulai dari prefix `/22`

## Pembagian IP - VLSM
