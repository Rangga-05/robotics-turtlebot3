# Laporan Praktikum Modul 1: Dockerized ROS 2 Development Environment

## Langkah yang Dikerjakan
1. Memastikan WSL 2 Ubuntu 22.04 dan Docker Engine/Desktop terinstal dan terhubung dengan baik.
2. Membuat repositori lokal `robotics-turtlebot3` dan mengonfigurasi package ROS 2 `my_first_robot_package`.
3. Memodifikasi `docker/Dockerfile` untuk menambahkan instalasi sistem operasi dan mengeksekusi otomatis `colcon build`.
4. Mengonfigurasi `docker/compose.yaml` untuk menjalankan service `talker` dan `listener` secara bersamaan dan terhubung di network host.
5. Mengeksekusi `docker compose build` dan `docker compose up`, serta memverifikasi node yang berjalan dengan `ros2 node list`.
6. Menyimpan seluruh perubahan dan melakukan push ke repositori GitHub.

## Masalah yang Ditemui dan Solusi
1. **Kendala Git Push (Authentication Failed):** Saat melakukan `git push` via HTTPS, autentikasi menggunakan password akun GitHub ditolak.
   * **Solusi:** Membuat Personal Access Token (PAT) tipe Classic dengan akses `repo` di GitHub Developer Settings, kemudian menggunakannya sebagai password saat autentikasi di terminal.
2. **Kendala Docker Not Found:** Saat membuka ulang terminal WSL, perintah `docker compose build` tidak terbaca.
   * **Solusi:** Memastikan aplikasi Docker Desktop di Windows berjalan dan opsi "WSL Integration" untuk Ubuntu-22.04 dihidupkan di pengaturan Docker.
