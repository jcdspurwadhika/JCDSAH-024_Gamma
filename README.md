# JCDSAH-024_Gamma

# JCDSAH-024_Gamma

# Prediksi Customer Churn pada Perusahaan Telekomunikasi

## Latar Belakang

Customer churn merupakan salah satu tantangan utama dalam industri telekomunikasi. Ketika pelanggan berhenti menggunakan layanan, perusahaan tidak hanya kehilangan pendapatan yang berulang tetapi juga harus mengeluarkan biaya tambahan untuk mendapatkan pelanggan baru.

Proyek ini bertujuan untuk membangun model machine learning yang dapat memprediksi kemungkinan pelanggan berhenti berlangganan (churn) berdasarkan data historis pelanggan. Dengan mengetahui pelanggan yang berisiko churn lebih awal, perusahaan dapat melakukan strategi retensi seperti memberikan promosi, meningkatkan kualitas layanan, atau menawarkan paket yang lebih sesuai dengan kebutuhan pelanggan.

Dataset yang digunakan dalam proyek ini berisi informasi mengenai demografi pelanggan, layanan yang digunakan, metode pembayaran, serta lama berlangganan.

---

# Metodologi

Tahapan yang dilakukan dalam proyek ini meliputi:

## 1. Business Understanding

- Memahami kegiatan bisnis perusahaan Telco: Perusahaan Telco adalah perusahaan yang menyediakan layanan khusus untuk jaringan telepon dan internet, serta perusahaan juga menyediakan layanan tambahan seperti Keamanan jaringan internet, penyimpanan data, perlindungan perangkat, streaming TV dan movies.

- Tantangan dan problem yang sedang ingin pihak manajemen selesaikan: Saat ini Perusahaan sedang menghadapi tantangan utama yaitu pelanggan yang berhenti menggunakan layanan yang disediakan dan berpindah ke competitor (Churn) yang mengakibatkan berkurangnya pendapatan perusahaan. Pihak manajemen sudah mengupayakan strategi program retensi seperti promo diskon, bonus kuota, upgrade paket dan strategi lainnya, namun pihak manajemen masih merasa program retensinya kurang memuaskan karena biaya yang telah dikeluarkan untuk program retensi dibandingan penurunan churn rate yang tidak begitu signifikan.

- Tujuan: Sehingga dengan dilakukannya analisis ini, perusahaan bertujuan untuk benar-benar memahami bahwa faktor apa saja yang mendorong pelanggan berhenti berlangganan (Churn). Dengan memahami sepenuhnya apa saja faktor-faktor yang mendorong churn, diharapkan perusahaan dapat lebih efisien dalam menggunakan anggaran biaya retensi, mendeteksi secara efektif dan tepat customer mana saja yang memiliki risiko churn tinggi supaya dapat mencegah customer untuk berpindah ke kompetitor dengan tepat waktu.

Maka dari itu perusahaan dapat meningkatkan revenue dengan biaya program retensi yang efisien.

## 2. Data Understanding

Dataset yang digunakan adalah Telco Customer Churn Dataset yang berisi informasi mengenai:

- Demografi pelanggan (CustomerID, Gender, SeniorCitizen, Partner, Dependents)
- Jenis layanan yang digunakan (PhoneService, MultipleLines, InternetService, OnlineSecurity, OnlineBackup, DeviceProtection, StreamingTV, StreamingMovies)
- Jenis Kontrak (Contract)
- Metode pembayaran (PaymentMethod)
- Lama berlangganan (Tenure)
- Biaya layanan bulanan dan total (MonthlyCharges)
- Status churn pelanggan (Churn): Target variabel dalam proyek ini adalah Churn, yang menunjukkan apakah pelanggan berhenti berlangganan atau tidak

## 3. Data Cleaning

Membersihkan, memperbaiki tipe data dan menangani nilai yang hilang (missing values) supaya data siap digunakan untuk analisis.

## 4. Data Preprocessing

Sebelum melakukan pelatihan model, dilakukan pembagian variabel independen dan variabel dependent (target), dilakukan encoding variabel kategorikal serta pembagian proporsi antara data training dan data test.

## 5. Modeling

Melakukan proses percobaan untuk menemukan model terbaik yang dapat digunakan untuk dataset Telco.

## 6. Model Evaluation

Memilih model yang akan di deploy dengan mengevaluasi performa model menggunakan metrik seperti Precision, Recall dan Confusion Matrix.

---

# Insight Utama

Beberapa faktor yang berhubungan dengan churn pelanggan antara lain:

- Pelanggan dengan kontrak bulanan (month-to-month) memiliki tingkat churn lebih tinggi
- Pengguna internet fiber optic cenderung lebih sering churn dibanding DSL
- Pelanggan tanpa layanan tambahan seperti Streaming Movies dan Streaming TV lebih berisiko churn
- Metode pembayaran electronic check memiliki tingkat churn yang relatif lebih tinggi

---

# Kesimpulan

Penelitian ini bertujuan untuk membangun model machine learning yang mampu memprediksi kemungkinan pelanggan berhenti menggunakan layanan (customer churn) sehingga perusahaan dapat melakukan tindakan retensi secara lebih proaktif.

Berdasarkan proses eksplorasi data, pemodelan, serta evaluasi model yang dilakukan, model Logistic Regression dipilih sebagai model akhir karena mampu memberikan performa yang baik serta memiliki tingkat interpretabilitas yang tinggi. Model ini memungkinkan perusahaan untuk memahami faktor-faktor yang paling berpengaruh terhadap keputusan pelanggan untuk churn.

Dengan menggunakan pendekatan penanganan data imbalance serta optimasi threshold berbasis biaya, model mampu mencapai nilai **Recall yang sangat tinggi pada kelas churn**, yang berarti model berhasil mengidentifikasi sebagian besar pelanggan yang berpotensi berhenti menggunakan layanan. Hal ini penting dari perspektif bisnis karena kegagalan dalam mengidentifikasi pelanggan yang akan churn dapat menyebabkan kehilangan pendapatan yang lebih besar.

Hasil interpretasi model menunjukkan bahwa beberapa faktor utama yang berkontribusi terhadap churn pelanggan antara lain penggunaan layanan **fiber optic**, tipe kontrak **month-to-month**, serta beberapa layanan tambahan seperti streaming services. Selain itu, analisis prioritas pelanggan menunjukkan bahwa terdapat kelompok pelanggan dengan kontribusi pendapatan tinggi yang juga memiliki risiko churn yang signifikan.

Dengan memanfaatkan model prediksi churn ini, perusahaan dapat mengidentifikasi pelanggan yang berisiko lebih awal serta memprioritaskan tindakan retensi secara lebih efektif.

---

# How to Run Local
cd telco_churn_app
Run this code
streamlit run app.py
Streamlit Link : https://jessicatanu-beep-telco-churn-app-app-z3vfvh.streamlit.app/
