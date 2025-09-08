# Catatan Perintah Linux Dasar

## Navigasi Direktori
| Perintah | Fungsi |
|----------|--------|
| `pwd` | Menampilkan lokasi direktori saat ini (Print Working Directory). |
| `ls` | Menampilkan isi folder di direktori aktif. |
| `ls -l` | Menampilkan isi folder dengan detail (izin akses, ukuran file, tanggal). |
| `ls -a` | Menampilkan semua file termasuk file tersembunyi (diawali dengan titik `.`). |
| `ls -lh` | Menampilkan isi folder dengan detail dan ukuran file dalam format mudah dibaca (KB/MB/GB). |
| `cd [nama_folder]` | Masuk ke folder tertentu. |
| `cd ..` | Kembali ke folder induk. |
| `cd ~` | Pindah ke direktori home user. |
| `cd /` | Pindah ke root direktori sistem. |

---

## Manajemen File & Folder
| Perintah | Fungsi |
|----------|--------|
| `touch [nama_file]` | Membuat file kosong baru. |
| `mkdir [nama_folder]` | Membuat folder baru. |
| `mkdir -p a/b/c` | Membuat folder beserta subfolder secara langsung. |
| `cp [sumber] [tujuan]` | Menyalin file. |
| `cp -r [folder] [tujuan]` | Menyalin folder beserta isinya. |
| `mv [sumber] [tujuan]` | Memindahkan file/folder atau mengganti namanya. |
| `rm [nama_file]` | Menghapus file. |
| `rm -r [nama_folder]` | Menghapus folder beserta isinya. |
| `rm -rf [nama_folder]` | Menghapus paksa folder beserta isinya tanpa konfirmasi. |

---

## Melihat & Membaca Isi File
| Perintah | Fungsi |
|----------|--------|
| `cat [file]` | Menampilkan isi file langsung di terminal. |
| `tac [file]` | Menampilkan isi file terbalik (dari bawah ke atas). |
| `less [file]` | Menampilkan isi file per halaman (scroll dengan spasi/↑/↓). |
| `more [file]` | Menampilkan isi file per halaman (mirip `less` tapi lebih sederhana). |
| `head [file]` | Menampilkan 10 baris pertama dari file. |
| `head -n 20 [file]` | Menampilkan 20 baris pertama dari file. |
| `tail [file]` | Menampilkan 10 baris terakhir dari file. |
| `tail -f [file]` | Menampilkan isi file secara real-time (berguna untuk log). |

---

## Informasi Sistem & Monitoring
| Perintah | Fungsi |
|----------|--------|
| `whoami` | Menampilkan nama user yang sedang login. |
| `id` | Menampilkan UID, GID, dan grup user. |
| `uname -a` | Menampilkan informasi kernel & sistem. |
| `hostname` | Menampilkan nama host (komputer). |
| `uptime` | Menampilkan berapa lama sistem sudah berjalan. |
| `df -h` | Menampilkan penggunaan disk dalam format mudah dibaca. |
| `du -sh [folder]` | Menampilkan ukuran total folder. |
| `free -h` | Menampilkan penggunaan RAM. |
| `top` | Menampilkan proses yang sedang berjalan secara interaktif. |
| `htop` | Versi lebih interaktif dari `top` (harus diinstal terlebih dahulu). |
| `ps aux` | Menampilkan daftar proses yang sedang berjalan. |
| `kill [pid]` | Menghentikan proses dengan PID tertentu. |
| `shutdown -h now` | Mematikan komputer langsung. |
| `reboot` | Merestart sistem. |

---

## Pencarian File & Teks
| Perintah | Fungsi |
|----------|--------|
| `find [folder] -name [nama_file]` | Mencari file berdasarkan nama. |
| `locate [nama_file]` | Mencari file (lebih cepat, tapi perlu database `updatedb`). |
| `grep "teks" [file]` | Mencari teks dalam file. |
| `grep -r "teks" [folder]` | Mencari teks dalam semua file di folder. |

---

## Manajemen Package (Debian/Ubuntu)
| Perintah | Fungsi |
|----------|--------|
| `sudo apt update` | Memperbarui daftar paket. |
| `sudo apt upgrade` | Memperbarui semua paket terinstal. |
| `sudo apt install [nama_paket]` | Menginstal paket baru. |
| `sudo apt remove [nama_paket]` | Menghapus paket. |
| `sudo apt autoremove` | Menghapus paket yang tidak terpakai. |

---

## Hak Akses & Permission
| Perintah | Fungsi |
|----------|--------|
| `ls -l` | Menampilkan izin file/folder. |
| `chmod 755 [file]` | Mengubah izin file (contoh: pemilik full, orang lain hanya baca & eksekusi). |
| `chmod +x [file]` | Memberikan izin eksekusi pada file. |
| `chown user:group [file]` | Mengubah pemilik dan grup file. |

---

## Jaringan
| Perintah | Fungsi |
|----------|--------|
| `ping [alamat]` | Mengecek koneksi ke alamat/domain tertentu. |
| `curl [url]` | Mengambil data dari URL. |
| `wget [url]` | Mengunduh file dari URL. |
| `ifconfig` | Menampilkan konfigurasi jaringan (butuh paket `net-tools`). |
| `ip addr` | Menampilkan informasi IP (alternatif modern). |
| `netstat -tulnp` | Menampilkan daftar port yang terbuka (butuh paket `net-tools`). |
| `ss -tulnp` | Menampilkan port terbuka (alternatif modern). |

---

## Trik Tambahan
| Perintah | Fungsi |
|----------|--------|
| `history` | Menampilkan riwayat perintah. |
| `!!` | Menjalankan ulang perintah terakhir. |
| `!n` | Menjalankan ulang perintah ke-n dari history. |
| `alias ll="ls -lh"` | Membuat alias perintah cepat. |
| `nano [file]` | Membuka file dengan editor teks Nano. |
| `vim [file]` | Membuka file dengan editor teks Vim. |

---
