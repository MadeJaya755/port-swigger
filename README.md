Dokumentasi Kelas PortSwigger
1. API Testing (api tasting.jpg)

Isi kelas:

Konsep keamanan API: otorisasi, autentikasi, access control, dan parameter handling.

Tipe celah umum pada API: IDOR, broken object-level authorization, excessive data exposure, dan insecure direct object references.

Cara kerja endpoint, header, dan response JSON.

Kegiatan di kelas:

Menganalisis request/response API untuk menemukan parameter sensitif.

Menguji perubahan nilai parameter (ID, token) untuk mendeteksi IDOR.

Memeriksa kontrol akses dengan permintaan yang dimodifikasi (mis. meminta resource user lain).

Mencatat kesalahan konfigurasi dan rekomendasi mitigasi.



2. Clickjacking (clickjacking.jpg)

Isi kelas:

Prinsip clickjacking: memanipulasi UI dengan frame tersembunyi untuk membuat pengguna melakukan tindakan tanpa sadar.

Header dan kebijakan proteksi: X-Frame-Options dan Content-Security-Policy (frame-ancestors).

Kegiatan di kelas:

Mencari target yang bisa di-embed tanpa header proteksi.

Membuat demonstrasi proof-of-concept halaman yang meng-overlay elemen target.

Menguji efek interaksi user pada elemen tersembunyi.

Merekomendasikan perbaikan konfigurasi header.



3. Path Traversal (path tranversal.jpg)

Isi kelas:

Mekanisme path traversal: penggunaan ../ atau encoding untuk mengakses file di luar direktori yang diizinkan.

Teknik bypass filter sederhana dengan encoding atau variasi path.

Kegiatan di kelas:

Mengidentifikasi endpoint yang menerima path/file dari input user.

Mencoba payload traversal untuk membaca file sensitif (mis. konfigurasi, credential).

Menganalisis sanitasi input server dan bagaimana ia gagal.

Menyusun saran mitigasi (whitelisting path, canonicalization).



4. Server-Side Template Injection (SSTI) (server-side.jpg)

Isi kelas:

Konsep SSTI: input user disuntikkan langsung ke engine template server (Jinja2, Twig, dll).

Dampak: dari disclosure data hingga remote code execution tergantung engine.

Kegiatan di kelas:

Mendeteksi apakah input diproses oleh template engine (payload tes sederhana).

Menilai output yang dihasilkan untuk melihat eksekusi template.

Mengeksplorasi tingkat kerentanan (informasi leak vs RCE).

Merekomendasikan pencegahan (escape output, disable eval di template).



5. SQL Injection (sql injaction.jpg)

Isi kelas:

Dasar-dasar SQLi: bagaimana input user bisa memodifikasi query database.

Variasi SQLi: boolean-based, time-based, union-based, error-based.

Kegiatan di kelas:

Menemukan input yang dipakai langsung dalam query SQL.

Menguji payload injeksi untuk melihat perubahan hasil respons.

Menilai tingkat akses yang bisa diperoleh (baca data, bypass auth).

Menyarankan mitigasi (prepared statements, parameterized queries).



6. Web LLM Attacks (web LLM attacks.jpg)

Isi kelas:

Risiko integrasi LLM: prompt injection, data exfiltration, dan output-driven actions.

Vektor serangan pada aplikasi yang mem-forward input ke model.

Kegiatan di kelas:

Memahami jalur data dari user → server → model → aplikasi.

Menyusun contoh prompt injection untuk melihat bagaimana model merespon instruksi berbahaya.

Menilai kontrol yang kurang (mis. tidak memfilter prompt, langsung mengeksekusi output).

Merekomendasikan mitigasi (sanitasi prompt, rate limiting, human-in-the-loop).



7. WebSockets (web sockets.jpg)

Isi kelas:

Karakteristik WebSocket: koneksi persistent, pesan event-driven, handshake spesifik.

Risiko: autentikasi lemah, replay/forgery, dan ekspos data real-time.

Kegiatan di kelas:

Memantau handshake dan pesan WebSocket untuk menemukan token/session yang bocor.

Menguji manipulasi pesan untuk memicu aksi tak diinginkan di server.

Mengecek apakah server memvalidasi setiap event dan sumbernya.

Menyusun rekomendasi (validasi sisi server, penggunaan WSS, token scoping).
