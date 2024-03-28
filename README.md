Kode ini mendefinisikan dua kelas, yaitu MarketingDataETL dan TargetedMarketingETL, yang digunakan untuk melakukan proses ekstraksi, transformasi, dan penyimpanan data pemasaran.

Kelas MarketingDataETL memiliki metode extract() yang digunakan untuk membaca data dari file CSV dan menampilkan data sebelum transformasi. Metode transform() digunakan untuk membersihkan data dengan menghapus baris yang memiliki nilai kosong dalam kolom 'purchase_date' dan mengonversi kolom 'purchase_date' ke dalam format datetime jika memungkinkan.

Kelas TargetedMarketingETL merupakan turunan dari MarketingDataETL. Kelas ini menambahkan metode segment_customers() yang digunakan untuk mengelompokkan pelanggan berdasarkan jumlah yang dihabiskan. Metode transform() di-overide untuk memanggil metode transform() dari kelas induk dan kemudian memanggil metode segment_customers().

Setelah melakukan ekstraksi dan transformasi, data yang telah di-segmentasi disimpan dalam format Excel menggunakan metode store_segmented_data().

Instansiasi objek dari TargetedMarketingETL dilakukan dengan mengekstrak data, melakukan transformasi, dan menyimpan data yang telah di-segmentasi ke dalam file Excel dengan nama "segmented_data_etl.xlsx".
