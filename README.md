# Portfolio — Muhammad Ali Akbar Al-Qahri · Data Analyst

Portfolio website satu halaman yang menonjolkan pekerjaan sebagai **Data Analyst di PT Cerebrum Edukanesia Nusantara**, dengan fokus pada program **Power BI end-to-end**: dari banyak database terpisah → ETL ke data warehouse → **star schema** (fact + dimension) → dashboard Power BI yang terhubung langsung ke MySQL.

**Live demo:** _(isi setelah deploy ke Vercel, mis. https://ali-akbar.vercel.app)_

---

## Isi situs

- **Hero** — ringkasan peran + tombol Download CV.
- **About & Skills** — latar Data Science Telkom University + tech stack.
- **Architecture** — pipeline multi-database → star schema → Power BI, lengkap dengan **diagram star schema interaktif** (1 fact table dikelilingi dimensi).
- **Dashboards** — 4 dashboard Power BI produksi (Revenue, User, Package, Activity) dengan lightbox zoom.
- **Track record** — rekap nyata 120 task magang (Feb–Jun 2026) dari tracker internal: jenis pekerjaan, sumber permintaan, divisi yang dilayani.
- **Projects, Experience, Contact** — proyek pendukung, timeline karier, dan tautan kontak.

Fitur: dark/light theme, 5 pilihan warna aksen, dan toggle bahasa **ID / EN**.

## Struktur file

```
.
├── index.html                              # seluruh situs (HTML + CSS + JS, single file)
├── dashboard-revenue.png                   # screenshot Power BI
├── dashboard-user.png
├── dashboard-package.png
├── dashboard-activity.png
├── Muhammad_Ali_Akbar_Al-Qahri_Resume.pdf  # CV (tombol download)
├── Tracker DB.xlsx                          # tracker pekerjaan (tombol download)
├── vercel.json
├── .gitignore
└── README.md
```

## Menjalankan secara lokal

Situs ini statis — cukup buka `index.html` di browser, atau jalankan server lokal:

```bash
python -m http.server 8000
# lalu buka http://localhost:8000
```

## Deploy ke GitHub + Vercel

### 1. Push ke GitHub

```bash
git init
git add .
git commit -m "Initial commit: data analyst portfolio"
git branch -M main
git remote add origin https://github.com/<username>/<nama-repo>.git
git push -u origin main
```

### 2. Deploy lewat Vercel

1. Buka [vercel.com](https://vercel.com) dan login dengan akun GitHub.
2. **Add New… → Project**, lalu pilih repo ini.
3. Framework Preset: **Other** (situs statis, tanpa build step).
4. Build Command & Output: biarkan kosong / default.
5. Klik **Deploy**. Selesai — situs langsung online di `https://<nama-repo>.vercel.app`.

Setiap `git push` berikutnya akan otomatis men-deploy ulang.

> Catatan: nama file `Tracker DB.xlsx` mengandung spasi. Tautan download di situs sudah disesuaikan, tetapi jika ingin URL lebih bersih, rename menjadi `Tracker_DB.xlsx` dan perbarui `href` di `index.html`.

---

© 2026 Muhammad Ali Akbar Al-Qahri
