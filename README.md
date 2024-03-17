## Commit 1:
Dalam mengerjakan Milestone 1: Single threaded web server, saya mendapatkan pengalaman baru dalam memahami dasar-dasar pembangunan web server dan interaksi jaringan pada level rendah menggunakan Rust. Kode yang saya buat memanfaatkan TcpListener dan TcpStream dari standard library Rust untuk mendengarkan dan menangani koneksi TCP. Proses ini memungkinkan saya untuk lebih dalam memahami bagaimana web server menerima dan memproses request HTTP secara fundamental. 

## Commit 2:
Dalam mengerjakan Milestone 2: Returning HTML, saya mempelajari tentang bagaimana cara mengembangkan fungsi handle_connection pada web server single-threaded saya untuk tidak hanya menerima request HTTP tetapi juga untuk mengembalikan response berupa konten HTML. Dengan menggunakan Rust, saya menambahkan logika untuk membaca file HTML dari sistem file dan mengirimkannya sebagai bagian dari body response HTTP. 

Ini adalah hasilnya:
![Commit 2 screen capture](/assets/images/commit2.jpeg)

## Commit 3:
Dalam mengerjakan Milestone 3: Validating Request and Selectively Responding, saya mempelajari pentingnya memvalidasi permintaan yang masuk ke server dan memberikan respons secara selektif. Saya menyadari bahwa tidak semua permintaan harus dijawab dengan konten yang sama; ada permintaan yang valid dan ada yang tidak. Oleh karena itu, saya mengimplementasikan logika untuk membedakan antara permintaan untuk halaman yang tersedia dengan halaman yang tidak tersedia. Dalam proses ini, saya melakukan refaktor pada kode untuk memastikan bahwa setiap bagian tanggung jawab fungsi lebih jelas dan terpisah, yang memungkinkan untuk perawatan dan pembacaan kode yang lebih baik di masa depan.

Ini adalah hasilnya:
![Commit 3 screen capture](/assets/images/commit3.jpeg)

## Commit 4:
Dalam mengerjakan Milestone 4: Simulation Slow Response, saya mempelajari tentang konsekuensi dari operasi yang memakan waktu di dalam server yang single-threaded. Melalui implementasi rute /sleep yang sengaja memberikan jeda dengan thread::sleep(Duration::from_secs(10)), saya dapat mengamati dampak langsung dari sebuah thread yang diblokir terhadap kemampuan server untuk menangani permintaan lain. Hal ini memberikan pemahaman mengenai pentingnya menggunakan asynchronous programming dan multithreading dalam pengembangan web server agar dapat menangani beban kerja yang tinggi dan tetap memberikan layanan yang responsif.

