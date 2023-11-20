Computer Vision Portofolio

Target Pencapaian
Implementasi pengolahan gambar digital  untuk meningkatkan kualitas gambar dengan menggunakan teknik Pooling dan CLAHE.
Implementasi metode Transfer Learning untuk kasus multi-klasifikasi dengan menggunakan pemodelan Deep Learning-based Computer Vision, seperti ResNet, DenseNet, dan Vision Transformer (ViT).


# Peningkatan Gambar dengan Max Pooling dan CLAHE

## Tujuan
Proyek ini bertujuan untuk mereplikasi algoritma peningkatan gambar yang umum digunakan dalam kamera ponsel pintar, khususnya teknik yang digunakan oleh pemimpin industri seperti Apple dan Samsung. Implementasi melibatkan Max Pooling dan Contrast Limited Adaptive Histogram Equalization (CLAHE).

## Alat dan Pustaka
- Python
- OpenCV
- Scikit-image
- Numpy
- Matplotlib
- PyTorch

## Kumpulan Data
Pastikan bahwa "photo1.jpeg" dan "lena.png" diunggah ke file Google Colab sebelum menjalankan notebook.

## Langkah-langkah

1. **Pemrosesan Gambar Berwarna:**
   - Konversi saluran warna dari BGR ke RGB.
   - Konversi saluran warna dari BGR ke Grayscale.
   - Konversi gambar Grayscale ke Binary.

2. **Analisis Histogram:**
   - Plot histogram dari gambar asli.
   - Plot histogram dari gambar Grayscale.

3. **Max Pooling:**
   - Terapkan Max Pooling menggunakan Scikit-image.
   - Terapkan Max Pooling menggunakan PyTorch dan bandingkan dengan Scikit-image.

4. **Min Pooling dan Average Pooling:**
   - Terapkan operasi Min Pooling dan Average Pooling, dan pahami perbedaannya.

5. **CLAHE (Contrast Limited Adaptive Histogram Equalization):**
   - Implementasikan CLAHE pada gambar RGB.

6. **Simpan Gambar yang Diedit:**
   - Simpan gambar yang ditingkatkan dengan CLAHE dengan nama file yang ditentukan.

## Pertanyaan untuk Diexplorasi:
- Pahami keuntungan Max Pooling PyTorch dibandingkan dengan Scikit-image.
- Bedakan antara operasi Min Pooling dan Average Pooling.
- Telusuri keuntungan menggunakan CLAHE daripada Max Pooling untuk mencerahkan gambar berwarna gelap.

## Kesimpulan:
Membandingkan dan menganalisis hasil Max Pooling dan CLAHE untuk menentukan teknik peningkatan gambar yang paling efektif untuk foto berwarna gelap.

# Transfer Learning menggunakan PyTorch dengan Dataset MNIST

## Gambaran Proyek
Proyek ini melibatkan pembuatan model Computer Vision untuk fasilitas robotik baru di Kalimantan Timur, Indonesia. Tugasnya adalah mengajari robot untuk mengidentifikasi digit tulisan tangan (0-9) dengan benar menggunakan dataset MNIST. Tujuannya adalah menyelesaikan masalah ini secara efisien dalam batas waktu yang ketat menggunakan Transfer Learning.

## Model
Kami bereksperimen dengan tiga model pra-dilatih: ResNet18, DenseNet121, dan Vision Transformer (ViT). Model-model ini awalnya dilatih dengan dataset ImageNet dan diadaptasi untuk tugas MNIST.

## Langkah-langkah

1. **Eksperimen dengan Model DenseNet**
   - Ubah jumlah neuron pada lapisan pertama dan terakhir agar sesuai dengan 10 kelas MNIST.
   - Tentukan hiperparameter dan latih model dengan semua lapisan dapat dilatih.
   - Plot kinerja pelatihan dan validasi.

2. **Pembekuan Lapisan**
   - Bekukan bagian-bagian khusus dari lapisan: (1) "denseblock1," (2) "denseblock1" dan "denseblock2."

3. **Pemelatihan Ulang dengan Lapisan yang Dibekukan**
   - Latih ulang setiap model dengan lapisan yang dibekukan.
   - Plot kinerja dan periksa perbedaannya.

4. **Bonus: Replikasi dengan ResNet dan ViT**
   - Ulangi langkah-langkah di atas dengan model ResNet dan ViT.

## Hasil dan Analisis

### Eksperimen dengan DenseNet
- Meraih akurasi yang baik dalam waktu pelatihan singkat.
- Kerugian berkurang, dan akurasi meningkat selama epoch.

### Transfer Learning dengan Lapisan yang Dibekukan
- Akurasi model lebih rendah ketika lapisan dibekukan.
- Lebih banyak lapisan yang dibekukan menghasilkan akurasi lebih rendah pada epoch awal.

### Waktu Eksekusi
- Membekukan lapisan mengurangi waktu pelatihan-validasi.
- Lebih banyak lapisan yang dibekukan menghasilkan pelatihan-validasi yang lebih cepat.

## Kesimpulan
Transfer Learning efektif untuk pengembangan model yang cepat, tetapi membekukan terlalu banyak lapisan dapat membatasi adaptabilitas terhadap data baru. Perlu dipertimbangkan pertukaran antara waktu pelatihan dan akurasi berdasarkan persyaratan dan kendala spesifik proyek.

## Cara Melakukan Eksperimen Ulang
Untuk mengulangi eksperimen dengan model-model yang berbeda, ubah pemilihan model dalam kode (misalnya, "resnet" atau "vit"). Sesuaikan hiperparameter sesuai kebutuhan.
