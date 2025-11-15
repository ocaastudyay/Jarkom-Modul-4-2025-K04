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
<img width="1328" height="770" alt="puwaling baru" src="https://github.com/user-attachments/assets/3454fa85-2262-47e4-9621-e124477e4526" />


## Tabel Pembagian Rute
| Nama Subnet | Rute                                                            | Host + Gateway | Netmask | Jumlah Host |
|-------------|------------------------------------------------------------------|----------------|---------|-------------|
| A1          | Morgoth > Switch > Erendis > Switch > Elrond                    | 62             | /26     | 61          |
| A2          | Throne > Erebor                                                 | 3              | /30     | 2           |
| A3          | Amorth > Switch > Morgoth > Switch > Throne                     | 4              | /29     | 3           |
| A4          | Anor > Switch > Beacon > Switch > Silmarils                     | 661            | /22     | 660         |
| A5          | Minastir > Amorth                                               | 2              | /30     | 1           |
| A6          | Minastir > Anor                                                 | 2              | /30     | 1           |
| A7          | Amonsul > Minastir                                              | 2              | /30     | 1           |
| A8          | Amonsul > Eregion                                               | 2              | /30     | 1           |
| A9          | Amonsul > Fornost                                               | 2              | /30     | 1           |
| A10         | Fornost > Switch > Valinor > Switch > Valmar                    | 4              | /29     | 3           |
| A11         | Valinor > Switch > Shadow > Switch > Anarion > Switch > Lindon  | 299            | /23     | 298         |
| A12         | Valmar > Switch > Doriath > Switch > Amor                       | 28             | /27     | 27          |
| A13         | Valmar > Switch > Imrahil > Switch > Utumno > Switch > Gwaith   | 34             | /26     | 33          |
| A14         | Eregion > Switch > Markwood > Switch > Morgul                   | 126            | /25     | 125         |
| A15         | Guldur > Switch > Palantir > Switch > Edhil                     | 120            | /25     | 119         |
| A16         | Guldur > Switch > IronCrwon > Switch > Grond > Switch > Hobbiton| 14             | /28     | 13          |
| A17         | Numenor > Switch > Arthedain > Switch > Mirdain                 | 875            | /22     | 874         |
| A18         | Mordor > Erain                                                  | 2              | /30     | 1           |
| A19         | Erain > Switch > Melkor > Switch > Khazad                       | 503            | /23     | 502         |
| A20         | Erain > Switch > Balrog > Switch > Gothmog > Switch > Thranduil | 470            | /23     | 469         |
| A21         | Numenor > Mordor                                                | 2              | /30     | 1           |
| A22         | Guldur > Numenor                                                | 2              | /30     | 1           |
| A23         | Eregion > Numenor                                               | 2              | /30     | 1           |
| **Total**   |                                                                  | **3221**       | **/20** | **3198**    |

Jika menurut Jumlah Host yang dibutuhkan maka IP awal adalah `192.213.0.0/20` tetapi pada data kebutuhan host yang paling besar adalah pada prefix `/22` maka untuk pembagian IP VLSM akan dimulai dari prefix `/22`

## Pembagian IP - VLSM
Tabel Pembagian VLSM setelah diurutkan dengan acuan kebutuhan host yang paling banyak
| Subnet | Network ID     | Netmask           | Broadcast        | Range Blok                         |
|--------|----------------|-------------------|------------------|-------------------------------------|
| A17    | 192.213.0.0    | 255.255.252.0     | 192.213.3.255    | 192.213.0.0 - 192.213.3.255         |
| A4     | 192.213.4.0    | 255.255.252.0     | 192.213.7.255    | 192.213.4.0 - 192.213.7.255         |
| A19    | 192.213.8.0    | 255.255.254.0     | 192.213.9.255    | 192.213.8.0 - 192.213.9.255         |
| A20    | 192.213.10.0   | 255.255.254.0     | 192.213.11.255   | 192.213.10.0 - 192.213.11.255       |
| A11    | 192.213.12.0   | 255.255.254.0     | 192.213.13.255   | 192.213.12.0 - 192.213.13.255       |
| A14    | 192.213.14.0   | 255.255.255.128   | 192.213.14.127   | 192.213.14.0 - 192.213.14.127       |
| A15    | 192.213.14.128 | 255.255.255.128   | 192.213.14.255   | 192.213.14.128 - 192.213.14.255     |
| A1     | 192.213.15.0   | 255.255.255.192   | 192.213.15.63    | 192.213.15.0 - 192.213.15.63        |
| A13    | 192.213.15.64  | 255.255.255.192   | 192.213.15.127   | 192.213.15.64 - 192.213.15.127      |
| A12    | 192.213.15.128 | 255.255.255.224   | 192.213.15.159   | 192.213.15.128 - 192.213.15.159     |
| A16    | 192.213.15.160 | 255.255.255.240   | 192.213.15.175   | 192.213.15.160 - 192.213.15.175     |
| A3     | 192.213.15.176 | 255.255.255.248   | 192.213.15.183   | 192.213.15.176 - 192.213.15.183     |
| A10    | 192.213.15.184 | 255.255.255.248   | 192.213.15.191   | 192.213.15.184 - 192.213.15.191     |
| A2     | 192.213.15.192 | 255.255.255.252   | 192.213.15.195   | 192.213.15.192 - 192.213.15.195     |
| A5     | 192.213.15.196 | 255.255.255.252   | 192.213.15.199   | 192.213.15.196 - 192.213.15.199     |
| A6     | 192.213.15.200 | 255.255.255.252   | 192.213.15.203   | 192.213.15.200 - 192.213.15.203     |
| A7     | 192.213.15.204 | 255.255.255.252   | 192.213.15.207   | 192.213.15.204 - 192.213.15.207     |
| A8     | 192.213.15.208 | 255.255.255.252   | 192.213.15.211   | 192.213.15.208 - 192.213.15.211     |
| A9     | 192.213.15.212 | 255.255.255.252   | 192.213.15.215   | 192.213.15.212 - 192.213.15.215     |
| A18    | 192.213.15.216 | 255.255.255.252   | 192.213.15.219   | 192.213.15.216 - 192.213.15.219     |
| A21    | 192.213.15.220 | 255.255.255.252   | 192.213.15.223   | 192.213.15.220 - 192.213.15.223     |
| A22    | 192.213.15.224 | 255.255.255.252   | 192.213.15.227   | 192.213.15.224 - 192.213.15.227     |
| A23    | 192.213.15.228 | 255.255.255.252   | 192.213.15.231   | 192.213.15.228 - 192.213.15.231     |

