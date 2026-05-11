# 🌾 JagoanSiber Platform Assessment
Dokumentasi pengujian penetrasi pada platform *bertani.my.id* dan *pegawai.my.id*. Laporan teknis lengkap tersedia dalam format PDF di dalam folder ini.

## 📑 Ringkasan Temuan Teknis

| Jenis Kerentanan | Fitur / Aset Terpengaruh | Dampak Utama |
| :--- | :--- | :--- |
| **Remote Code Execution** | Avatar Upload, Knowledge Posts, Admin File Mgmt | Kendali penuh atas server (Web Shell). |
| **SQL Injection** | Search & Filter Parameters | Ekstraksi basis data secara ilegal. |
| **Privilege Escalation** | Registration (Role Manipulation) | Mendapatkan akses Administrator. |
| **Stored XSS** | Update Settings, Admin Dashboard, SVG Upload | Pencurian session cookie & Defacement. |
| **Information Disclosure** | `.env` File & Laravel Debug Mode | Kebocoran API Keys & Kredensial DB. |
| **Broken Access Control** | Transaction Dashboard, Hidden Profile Page | Akses data finansial tanpa izin. |
| **Business Logic Bypass** | Attendance (GPS) & Leave Requests | Pemalsuan data kehadiran & perizinan. |

## 📝 Metodologi
1. **Reconnaissance:** Pemetaan *endpoint* dan *directory brute-forcing*.
2. **Analysis:** Identifikasi celah logika bisnis dan validasi input.
3. **Exploitation:** Verifikasi dampak melalui Proof of Concept (PoC).
4. **Reporting:** Penyusunan rekomendasi mitigasi teknis.
