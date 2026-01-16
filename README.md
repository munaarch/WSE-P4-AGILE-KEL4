# Praktikum Web Service Engineering - Week 4: Agile Development Methodologies

## 🔗 Repository Kelompok (Source Code Resmi)

Seluruh source code hasil praktikum 4 dikerjakan secara **kolaboratif**
dan disimpan dalam repository kelompok terpisah untuk menjaga
keaslian riwayat commit serta kontribusi masing-masing anggota.

🔗 **Repository Kelompok 4 – Agile Development Methodologies**  
https://github.com/pangeran-kesurupan/AGILE

**Status Kontribusi:**
- Repository ini dikerjakan secara tim (kelompok)
- Penulis README ini tercatat sebagai **Collaborator**
- Riwayat kontribusi dapat dilihat melalui *commit history* dan *contributors*

Catatan:
Repository kelompok tidak disalin ke repository pribadi
untuk menghindari duplikasi dan menjaga integritas version control.

## 👥 Identitas Kelompok 4

| Nama Mahasiswa | NIM | Peran |
| :--- | :--- | :--- |
| **Muhammad Riduwan** | 230104040080 | Project Manager |
| **Muna Rahimatul 'Olya** | **230104040081** | **Anggota** |
| **Siti Alayda Azzahro** | 230104040084 | Anggota |
| **Noor Ahmad Naufal** | 230104040074 | Anggota |

| Informasi Lain | Detail |
| :--- | :--- |
| **Kelas** | TI 23 B |
| **Mata Kuliah** | Web Service Engineering |

---

## 📚 Topik Pembelajaran
Berdasarkan Laporan Praktikum Modul 4, materi yang diimplementasikan meliputi:

1.  **Design-First**: Mendesain kontrak API menggunakan standar **OpenAPI (Swagger)** dan memvalidasinya menggunakan *Spectral* (Linting).
2.  **Mock-First**: Membuat server tiruan (*mock server*) menggunakan **Prism** untuk simulasi endpoint sebelum implementasi backend selesai.
3.  **Test-First (TDD)**: Menulis skenario pengujian (*unit testing*) menggunakan **Jest** terlebih dahulu (fase RED) sebelum menulis kode implementasi (fase GREEN).
4.  **Implementation**: Membangun layanan mikro (*microservices*) untuk **Order Service** dan **Notification Service**.
5.  **Hardening**: Meningkatkan keamanan dan observabilitas sistem dengan:
    * **Security Headers**: Menggunakan library `helmet`.
    * **Logging**: Implementasi logging terstruktur dan *correlation-id*.
    * **Rate Limiting**: Pembatasan jumlah request.

---

## 🚀 Layanan & Endpoint API

Project ini terdiri dari dua layanan utama yang berjalan pada port berbeda:

### 1. Order Service (Port 5002)
| Method | Endpoint | Deskripsi | Status Code |
| :--- | :--- | :--- | :--- |
| `POST` | `/orders` | Membuat pesanan baru | 201 Created / 400 Bad Request |

### 2. Notification Service (Port 5003)
| Method | Endpoint | Deskripsi | Status Code |
| :--- | :--- | :--- | :--- |
| `GET` | `/notifications` | Mengambil data notifikasi | 200 OK |

---

## 🛠️ Tools & Lingkungan Kerja
* **Runtime**: Node.js (v18+)
* **Language**: TypeScript / JavaScript
* **API Spec**: OpenAPI 3.0 (YAML)
* **Testing**: Jest
* **Mock Server**: Prism
* **Linting**: Spectral
* **Security**: Helmet, Rate-Limit

---

## 💻 Cara Menjalankan Project

Ikuti langkah-langkah berikut untuk mereproduksi hasil praktikum:

1.  **Instalasi Dependencies:**
    ```bash
    npm ci
    ```

2.  **Validasi Kontrak API (Linting):**
    ```bash
    npx spectral lint openapi/api.yaml
    ```

3.  **Menjalankan Services (Development Mode):**
    * Jalankan **Order Service** (Terminal 1):
        ```bash
        npm run dev:orders
        ```
    * Jalankan **Notification Service** (Terminal 2):
        ```bash
        npm run dev:notif
        ```

4.  **Menjalankan Pengujian (Test):**
    Untuk menjalankan unit test yang telah dibuat (Jest):
    ```bash
    npm test
    ```

---
*Dibuat untuk memenuhi tugas Praktikum Web Service Engineering - Agile Methodologies.*
