# 🚀 Helium Challenge - PT JobPortal
Laporan khusus untuk kompetisi pengujian penetrasi pada aplikasi web **PT JobPortal**.

## 🎯 Target
- **URL:** `https://jobportal.vulnapp.id`
- **Scope:** Seluruh fitur user, perusahaan, dan admin.

## 🔍 Temuan Utama
| Vulnerability | Impact | Mitigation |
| :--- | :--- | :--- |
| **Critical IDOR** | Akses password plaintext user lain via `userID`. | Implementasikan *Session-based Access Control*. |
| **SQL Injection** | Dump database pelamar dan kredensial admin. | Gunakan *Prepared Statements*. |
| **Stored XSS** | Pencurian session cookie melalui form lamaran. | Sanitasi input HTML dan implementasi CSP. |
| **IDOR Chaining** | Manipulasi status lamaran perusahaan lain. | Validasi kepemilikan objek pada setiap request. |

## 📊 Hasil Akhir
Berhasil mengidentifikasi lebih dari 10 celah keamanan dengan total dampak kritikal pada kerahasiaan data pengguna.
