# Submission 1: Diabetes Prediction
Nama: Shefiyyah Aurellia Wahyudi

Username dicoding: shefiyyah-aurellia-w

| | Deskripsi |
| ----------- | ----------- |
| Dataset | [Diabetes prediction dataset](https://www.kaggle.com/datasets/iammustafatz/diabetes-prediction-dataset)<br> Dataset prediksi Diabetes adalah kumpulan data medis dan demografis dari pasien, bersama dengan status diabetes mereka (positif atau negatif). Data ini mencakup fitur-fitur seperti usia, jenis kelamin, indeks massa tubuh (BMI), hipertensi, penyakit jantung, riwayat merokok, kadar HbA1c, dan kadar glukosa darah. |
| Masalah | Penyakit diabetes adalah kondisi di mana kadar gula darah seseorang menjadi terlalu tinggi. Diabetes dapat mengakibatkan komplikasi serius seperti kerusakan organ, masalah jantung, stroke, dan masalah mata. Beberapa gejala diabetes meliputi sering buang air kecil, haus berlebihan, penurunan berat badan tanpa sebab, kelelahan, dan luka yang sulit sembuh. Diabetes dapat dikendalikan melalui pola makan sehat, olahraga teratur, dan penggunaan obat-obatan yang diresepkan oleh dokter. |
| Solusi machine learning | Dengan memprediksi Diabetes, sistem perawatan kesehatan dapat mengalokasikan sumber daya dengan lebih efisien, memprioritaskan mereka yang membutuhkan perawatan yang lebih intensif. |
| Metode pengolahan | Deskripsi metode pengolahan data yang digunakan |
| Arsitektur model | Model ini memiliki beberapa input layer tergantung pada jumlah fitur kategorikal dan numerikal yang digunakan. Setiap fitur kategorikal diubah menjadi one-hot encoding dan dijadikan sebagai input layer dengan dimensi yang sesuai. Sedangkan fitur numerikal dijadikan sebagai input layer dengan dimensi 1.
Setelah input layer, output dari semua input layer digabungkan menggunakan layer concatenate. Pada arsitektur ini, terdapat tiga lapisan Dense dengan masing-masing memiliki 256, 64, dan 16 neuron. Aktivasi yang digunakan pada setiap lapisan adalah ReLU. Aktivasi yang digunakan adalah sigmoid, yang menghasilkan probabilitas prediksi diabetes. Nilai output yang mendekati 1 menunjukkan probabilitas tinggi untuk diabetes, sedangkan nilai yang mendekati 0 menunjukkan probabilitas rendah. : Setelah definisi arsitektur model, model dikompilasi menggunakan optimizer Adam dengan learning rate 0.001. Loss function yang digunakan adalah binary crossentropy, yang cocok untuk tugas klasifikasi biner seperti prediksi diabetes. Metric yang digunakan untuk evaluasi model adalah binary accuracy. |
| Metrik evaluasi | Metric yang digunakan pada model yaitu AUC, Precision, Recall, BinaryAccuracy, ExampleCount untuk mengevaluasi performa model sebuah klasifikasi dengan threshold lower bound = 0.5 ddan change threshold absolute = 0.0001|
| Performa model |Model yang dibuat menghasilkan performa yang cukup baik dalam memberikan sebuah prediksi dan dari pelatihan yang dilakukan menghasilkan binary_accuracy sebesar 97.15%, val_binary_acuracy sebesar 97.18%, dan loss sebesar 0.08. Hasil seperti ini sudah cukup baik untuk sebuah memprediksi |
| Opsi deployment | Proyek machine learning ini dideploy menggunakan salah satu platfrom as a service yaitu railway  yang menyediakan layanan gratis untuk mendeploy sebuah proyek.|
| Web app |  [diabetes-model](https://diabetes-prediction-production.up.railway.app/v1/models/diabetes-model/metadata)|
| Monitoring | Monitoring pada sistem ini dilakukan menggunakan prometheus dan grafana. Disini hanya dilakukan proses monitoring untuk menampilkan request yang masuk pada sistem yang akan menamplkan status pada tiap request yang dilakukan, pada sistem ini menampilkan yaitu apabila proses request berhasil ditandakan dengan ok |

