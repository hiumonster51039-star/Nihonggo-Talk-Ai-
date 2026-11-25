NIHONGO TALK AI - PROYEK ANDROID

Isi:
- Aplikasi Android WebView (Kotlin)
- Tampilan chat tema navy-biru
- Terhubung ke Cloudflare Worker yang sudah diberikan
- Tombol Belajar N5, Latihan Kaiwa, dan Koreksi Kalimat

CARA MEMBUAT APK:
1. Instal Android Studio di komputer.
2. Ekstrak ZIP ini.
3. Android Studio > Open > pilih folder NihongoTalkAI_Android.
4. Tunggu Gradle Sync selesai.
5. Pilih Build > Build Bundle(s) / APK(s) > Build APK(s).
6. APK hasil build biasanya ada di app/build/outputs/apk/debug/app-debug.apk.

CATATAN PENTING:
- File ini adalah proyek sumber Android, bukan APK yang sudah dikompilasi.
- Worker URL sudah diisi di app/src/main/assets/config.js.
- Worker harus menerima POST JSON { "messages": [...] } dan mengembalikan JSON { "reply": "..." }.
- Jika chat menampilkan masalah koneksi, Worker perlu mengizinkan CORS dari aplikasi Android/WebView (origin null atau origin aplikasi).
- Jangan masukkan API Key OpenAI ke file aplikasi. Simpan API Key hanya sebagai secret di Cloudflare Worker.

BUILD APK DARI HP (GITHUB ACTIONS):
1. Buat repository baru di GitHub dengan nama NihongoTalkAI dan set Public atau Private.
2. Ekstrak ZIP ini, lalu unggah semua ISI folder proyek (termasuk folder .github) ke repository GitHub.
3. Buka tab Actions di repository. Pilih workflow "Build Nihongo Talk AI APK".
4. Tekan Run workflow dan tunggu sampai selesai.
5. Buka hasil run yang hijau, bagian Artifacts, unduh NihongoTalkAI-debug-apk.
6. Ekstrak artifact ZIP dan ambil app-debug.apk.

Penting: GitHub Actions memerlukan akun GitHub dan koneksi internet. Jangan unggah API Key.
