### PROJEK OS-NABIL
LANGKAH 1 BUAT STRUKTUR DIREKTORI
Berikut contoh membuat direktori 
projek_file_manajement:
[deskripsi gambar]
https://drive.google.com/file/d/1Px1iOpNXnyp40YB_DF0_6kuQ0VfqqdUd/view?usp=drivesdk

#ubuntu@nabilbouato:~ mkdir projek_file_manajement


Berikut contoh perintah berpindah direktori ke 
projek_file_manajement dan membuat folder document images archives logs:
[deskripsi gambar]
https://drive.google.com/file/d/1I7W4isoNWqbh7NFwPbj5Q8Pc3aOoRPWf/view?usp=drivesdk


cd projec_file_manajement
mkdir document images archives logs


BERIKUT CONTOH PERINTAH MEMBUAT 20 FILE

[Deskripsi gambar]
https://drive.google.com/file/d/1x98pJD2OnIbO7E-i3i9-VxSVjmGal1ph/view?usp=drivesdk


touch file{1..10}.txt file{11..15}.jpg


BERIKUT CONTOH PERINTAH MEMASUKAN SEBUAH TEKS KE MASING MASING FILE YANG BERDEDA:

[Deskripsi gambar]
https://drive.google.com/file/d/1j7PDK17HdS4ol7QtJ-kaG5wINMZDHJXz/view?usp=drivesdk

echo "ini adalah dokumen comtoh" > file.txt
echo "data gambar" > file11.jpg
echo "log sistem contoh" > file20.log

Penjelasan
• mkdir → membuat folder baru
• touch → membuat  file kosong dengan cepat
• echo → menulis teks kedalam file

LANGKAH 2 SKRIP FILE ORGANISASI
Buat Script Organisasi File di dalam direktori proyek:
nano organisasi_file.sh
Naskah ISI
[Deskripsi gambar]

( https://drive.google.com/file/d/1DwRIHzH-5jURXFBeDsO0hdLD_nOSd8ix/view?usp=sharing )

#!/bin/bash
# Script untuk mengorganisasi file berdasarkan ekstensi

# Pastikan berada di direktori proyek
cd ~/project_file_management

# Pindahkan file sesuai ekstensi
find . -maxdepth 1 -type f -name "*.txt" -exec mv {} documents/ \;
find . -maxdepth 1 -type f -name "*.jpg" -exec mv {} images/ \;
find . -maxdepth 1 -type f -name "*.pdf" -exec mv {} archives/ \;
find . -maxdepth 1 -type f -name "*.log" -exec mv {} logs/ \;

# Konfirmasi hasil
echo "File berhasil dipindahkan ke folder sesuai ekstensi!"
ls documents images archives logs
Beri Hak Eksekusi:
chmod +x organisasi_file.sh
Eksekusi Naskah Yang Telah Dibuat:
./organisasi_file.sh
Penjelasan:

menemukan . -max depth 1 -type f -name "*.ext" → mencari file berdasarkan ekstensi di direktori saat ini.

-exec mv {} folder/ ; → memindahkan file hasil pencarian ke folder yang sesuai.

chmod +x → memberi izin eksekusi ke skrip.

LANGKAH 3 FUNGSI PENCARIAN
Karena saya sudah punya script pencarian file yang bisa mencari berdasarkan nama, ukuran, dan isi konten. Jadi Saya Langsung Buat Fungsi pencariannya.

Buat file Search_file.sh
nano search_file.sh
[Deskripsi gambar] ( https://drive.google.com/file/d/11KP1W8-jfZsyK_wDd6aTQVj5xc_NzJAD/view?usp=sharing )

 #!/bin/bash
# Script: search_files.sh
# Fungsi: Mencari file berdasarkan nama, ukuran, atau konten

cd ~/project_file_management

echo "=== PENCARIAN FILE ==="
echo "1. Cari berdasarkan nama"
echo "2. Cari berdasarkan ukuran"
echo "3. Cari berdasarkan isi konten"
read -p "Pilih opsi (1/2/3): " opsi

case $opsi in
  1)
    read -p "Masukkan nama atau pola file (contoh: *.txt): " nama
    echo "Hasil pencarian:"
    find . -type f -name "$nama"
    ;;
  2)
    read -p "Masukkan batas ukuran (contoh: +1M untuk lebih dari 1MB, -500k untuk kurang dari 500KB): " ukuran
    echo "Hasil pencarian:"
    find . -type f -size "$ukuran"
    ;;
  3)
    read -p "Masukkan kata kunci yang ingin dicari dalam file: " keyword
    echo "Hasil pencarian:"
    grep -r "$keyword" .
    ;;
  *)
    echo "Opsi tidak valid."
    ;;
esa
