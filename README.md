# Reflection

Wahyu Hidayat - 2206081894 - Advanced Programming B

1. ***What are the key differences between unary, server streaming, and bi-directional streaming RPC (Remote Procedure Call) methods, and in what scenarios would each be most suitable?***

    - **Unary RPC** memungkinkan komunikasi satu kali antara client dan server, cocok untuk query yang memerlukan respons tunggal, seperti cek status. 
    - **Server Streaming RPC** efektif untuk situasi di mana data harus terus menerus dikirimkan ke client, misalnya untuk real-time updates. 
    - **Bi-directional Streaming RPC** berguna dalam kasus yang memerlukan komunikasi dua arah dengan respons cepat, seperti aplikasi chatting atau gaming.

2. ***What are the potential security considerations involved in implementing a gRPC service in Rust, particularly regarding authentication, authorization, and data encryption?***

   Saat mengimplementasikan gRPC di Rust, memastikan **authentication** menggunakan teknik seperti JWT untuk keamanan akses, **authorization** untuk pengaturan akses berdasarkan peran pengguna, dan **data encryption** dengan TLS/SSL penting untuk melindungi data dan menjaga kerahasiaan transaksi.

3. ***What are the potential challenges or issues that may arise when handling bidirectional streaming in Rust gRPC, especially in scenarios like chat applications?***

   Dalam **bidirectional streaming** di Rust untuk aplikasi chat, tantangannya meliputi mengelola state secara efisien, menangani kesalahan jaringan, dan memastikan stabilitas dengan latency yang rendah.

4. ***What are the advantages and disadvantages of using the tokio_stream::wrappers::ReceiverStream for streaming responses in Rust gRPC services?***

   **Tokio_stream::wrappers::ReceiverStream** memfasilitasi konversi antara channels dan streams di Tokio, yang mendukung operasi asynchronous. Namun, hal ini mungkin tidak mengatur backpressure yang bisa mempengaruhi penggunaan sumber daya.

5. ***In what ways could the Rust gRPC code be structured to facilitate code reuse and modularity, promoting maintainability and extensibility over time?***

   Untuk mendukung **code reuse dan modularity** dalam Rust gRPC, penting untuk mengorganisir code dalam modul-modul terpisah, menggunakan trait untuk fungsi umum, dan menerapkan dependency injection untuk memudahkan pengujian dan pemeliharaan.

6. ***In the MyPaymentService implementation, what additional steps might be necessary to handle more complex payment processing logic?***

    Untuk pengolahan pembayaran yang lebih kompleks, langkah tambahan mencakup **validasi informasi pembayaran**, **pemeriksaan ketersediaan dana**, **proses melalui payment gateway**, **penanganan error**, dan **pengiriman notifikasi** tentang hasil transaksi. 

7. ***What impact does the adoption of gRPC as a communication protocol have on the overall architecture and design of distributed systems, particularly in terms of interoperability with other technologies and platforms?***

   Penggunaan gRPC mempengaruhi arsitektur sistem terdistribusi, meningkatkan interoperabilitas melalui **Protocol Buffers** dan mendukung komunikasi yang efisien dan konsisten antar layanan dengan memanfaatkan HTTP/2.

8. ***What are the advantages and disadvantages of using HTTP/2, the underlying protocol for gRPC, compared to HTTP/1.1 or HTTP/1.1 with WebSocket for REST APIs?***

    HTTP/2 menawarkan keuntungan dalam mengirim banyak pesan sekaligus, mengurangi latency dan memperbaiki kinerja dibandingkan HTTP/1.1. Namun, untuk aplikasi yang membutuhkan koneksi terbuka yang lama, WebSocket mungkin lebih sesuai.

9. ***How does the request-response model of REST APIs contrast with the bidirectional streaming capabilities of gRPC in terms of real-time communication and responsiveness?***

   Dibandingkan dengan model request-response dari REST API, **bidirectional streaming** gRPC menawarkan kemampuan komunikasi real-time yang lebih baik, mengurangi latency dan meningkatkan responsivitas untuk aplikasi interaktif.

10. ***What are the implications of the schema-based approach of gRPC, using Protocol Buffers, compared to the more flexible, schema-less nature of JSON in REST API payloads?***

    Pendekatan berbasis skema gRPC dengan **Protocol Buffers** menawarkan kepastian struktur data yang meningkatkan efisiensi dan mengurangi error, berbeda dengan pendekatan fleksibel namun kurang terstruktur dari JSON dalam REST API yang lebih rentan terhadap kesalahan runtime.
