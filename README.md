## Implementation-of-NoSQL-Solutions-on-Warehouse-Data-using-MongoDB-and-Cassandra

Dalam proses pengolahan data berbasis NoSQL, penting untuk memahami bahwa sistem seperti MongoDB dan Cassandra tidak dirancang untuk melakukan operasi join antar tabel seperti halnya sistem basis data  relasional (SQL). Hal ini disebabkan oleh prinsip dasar NoSQL yang mengutamakan kecepatan dan efisiensi dalam penyimpanan serta pengambilan data dalam skala besar. Cassandra, misalnya, sepenuhnya mengandalkan desain berbasis query, sehingga tidak menyediakan kemampuan join antar tabel. Sementara MongoDB hanya menyediakan fitur terbatas seperti $lookup, yang hanya bisa digunakan dalam konteks agregasi dan masih memiliki banyak batasan dibanding join pada SQL. Karena itulah, ketika diperlukan analisis data dari beberapa tabel yang berbeda, proses penggabungan (join) data dilakukan di luar database, yaitu menggunakan Python dan library seperti Pandas dalam Jupyter Notebook. Pendekatan ini disebut sebagai integrasi data secara desentralisasi, karena proses penyatuan dan pemrosesan dilakukan di luar sistem database. Oleh karena itu, alasan penggunaan Python sebagai alat bantu integrasi data dalam praktikum ini adalah keputusan yang tepat dan sesuai dengan karakteristik serta keterbatasan dari sistem NoSQL yang digunakan. Selain itu, proses preprocessing atau pembersihan dan penyesuaian data juga dilakukan sebelum analisis. Penjelasan lebih lengkap mengenai tahapan preprocessing tersebut dapat diakses melalui tautan berikut: Penjelasan Preprocessing Data Warehouse Retails. Laporan ini akan berisi 10 query utama, masing-masing disertai hasil dan penjelasannya. Lima query dibuat langsung dari MongoDB, dan lima lainnya dibuat dari hasil penggabungan data di Python. Setiap query akan dianalisis dan divisualisasikan agar lebih mudah dipahami.

# Download Tools:
Install Java SE Development Kit (JDK) versi 1.8.0_202
https://www.oracle.com/id/java/technologies/javase/javase8-archive-downloads.html

Install MongoDB (Community Edition)
https://www.mongodb.com/try/download/community

Install Apache Cassandra
https://cassandra.apache.org/download/
