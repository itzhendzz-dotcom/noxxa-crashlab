# JPatch Render Lite

Config siap dipakai oleh JPatch yang sudah terpasang. Ini preset statis, bukan plugin baru atau adaptive limiter. Tidak membutuhkan compile.

Basis: net.rusjj.jpatch.ini milik pengguna, upload 11 September 2026. Semua 251 key dipertahankan; tepat dua nilai berubah.

| Setting [Visual] | Awal | Preset | Tujuan dan trade-off |
|---|---:|---:|---|
| DetailedWaterDrawDistance | 48 | 32 | Memperpendek cakupan air detail; transisi kualitas air dapat terlihat lebih dekat. |
| FxDistanceMult | 1.0 | 0.8 | Mengurangi pengali jarak FX yang ditangani JPatch; efek jauh dapat menghilang lebih cepat. |

Angka tersebut adalah pilihan preset konservatif, bukan hasil benchmark atau nilai optimum yang telah dibuktikan. Pengurangan beban yang diharapkan bergantung pada scene dan apakah versi JPatch aktif menerapkan kedua setting. Tidak semua shader/efek SA_DOX mengikuti pengali FX ini. Tidak ada klaim persentase kenaikan FPS, jaminan 120 FPS, pengurangan stutter universal, atau peningkatan pada scene tanpa beban terkait.

## Pasang

1. Download file `net.rusjj.jpatch.ini` dari folder ini. Pada halaman file GitHub, gunakan Download raw file; bila browser membuka teks, simpan dengan nama persis tersebut, bukan .txt.
2. Tutup game dan backup config JPatch aktif saat ini.
3. Ganti file `net.rusjj.jpatch.ini` di lokasi config JPatch yang memang dibaca APK kamu. Gunakan lokasi file lama, termasuk pada APK Unprotected; tidak perlu membuat path baru.
4. Jalankan game kembali.

Butuh libJPatch.so yang kompatibel dan sudah berfungsi. File INI ini tidak bekerja sendiri sebagai plugin AML dan tidak perlu mengganti libGTASA.so. Jika config aktif kamu lebih baru atau berbeda dari basis September 11, cukup pindahkan dua nilai pada tabel ke bagian [Visual] config aktif agar setting lain tidak tertimpa.

## Verifikasi dan rollback

Struktur dicek: 251 key, tanpa duplikat, tanpa penambahan/penghapusan key, tepat dua perubahan. File tersimpan melalui GitHub. Belum diuji di perangkat, belum diukur FPS, dan versi binary JPatch saat ini belum diperiksa.

Bandingkan rute yang sama dekat perairan serta scene dengan FX jauh, menggunakan preset grafis, cap FPS, dan kondisi awal perangkat yang sama. Jika tampilan menjadi terlalu terpotong atau tidak ada manfaat, pulihkan backup. Untuk membalik hanya preset ini, kembalikan dua angka menjadi 48 dan 1.000000.

## Alasan cakupan perubahan kecil

Basis config sudah mengaktifkan OptimiseTextureSearching, FixFXLeak, SP_StreamingMemoryBug, serta mematikan tambahan refleksi/mirror/shadow berat. Mengaktifkan ulang setting yang sama tidak memberikan optimasi tambahan. Pengaturan RAM/streaming tidak dinaikkan tanpa bukti bottleneck. Kepadatan kendaraan dan pejalan kaki tetap mengikuti config basis.

Referensi fitur JPatch: https://github.com/AndroidModLoader/JPatch
