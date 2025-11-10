PortSwigger Academy — Dokumentasi Kelas

Repositori ini berisi bukti penyelesaian dan ringkasan praktikal dari beberapa lab di PortSwigger Web Security Academy.
Setiap entri menjelaskan apa isi kelasnya dan apa yang dilakukan selama latihan — fokus pada temuan, teknik pengujian, dan rekomendasi mitigasi.

Daftar Kelas
1. API Testing


Isi kelas: Keamanan API modern — autentikasi/otorisasi, kontrol akses objek, parameter tampering, dan ekspos data berlebih.
Yang dilakukan: Menganalisis endpoint dan payload JSON, mengubah parameter (ID/token) untuk mencari IDOR, menguji kontrol akses dengan permintaan ter-manipulasi, dan mendokumentasikan titik lemah beserta rekomendasi perbaikan.

2. Clickjacking


Isi kelas: Teknik clickjacking dan proteksi header (mis. X-Frame-Options, Content-Security-Policy frame-ancestors).
Yang dilakukan: Mencari halaman yang dapat di-embed tanpa proteksi, membuat proof-of-concept halaman overlay untuk demonstrasi, dan merekomendasikan header/policy yang harus diterapkan.

3. Path Traversal


Isi kelas: Cara kerja path traversal (../, encoding) dan teknik bypass filter.
Yang dilakukan: Mengidentifikasi endpoint yang membangun path dari input user, menguji payload traversal untuk baca file sensitif, menganalisis mekanisme sanitasi, dan menyusun mitigasi (canonicalization + whitelist).

4. Server-Side Template Injection (SSTI)


Isi kelas: Risiko injeksi pada template engine (Jinja2, Twig, dll.) — dari info leak sampai RCE.
Yang dilakukan: Menguji input pada rendering template, mendeteksi eksekusi ekspresi template, mengevaluasi potensi eskalasi (RCE), dan rekomendasi mitigasi seperti escaping dan membatasi fitur engine.

5. SQL Injection


Isi kelas: Dasar-dasar SQLi (boolean/time/union/error) dan dampaknya pada integritas data.
Yang dilakukan: Menemukan input yang dipakai pada query, menguji payload injeksi untuk mengakses/mengekstrak data, menilai skop eksfiltrasi, dan merekomendasikan parameterized queries/prepared statements.

6. Web LLM Attacks


Isi kelas: Vektor serangan terhadap aplikasi yang memakai Large Language Models — prompt injection, data exfiltration, dan output-driven actions.
Yang dilakukan: Memetakan aliran data ke/dari model, menguji prompt injection untuk melihat perilaku model, menilai risiko eksekusi otomatis dari output model, dan merekomendasikan sanitasi prompt serta kontrol operasional.

7. WebSockets


Isi kelas: Karakteristik WebSocket, handshake, dan risiko real-time (token leak, replay, message forgery).
Yang dilakukan: Memantau handshake dan pesan WebSocket untuk menemukan kebocoran token/session, memanipulasi pesan untuk menguji validasi server, dan menyusun mitigasi (WSS, validasi server-side setiap event, scoping token).
