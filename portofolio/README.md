# Portofolio + CMS (GitHub Pages)

Situs statis yang membaca isinya dari `content/site.json`. Konten diedit lewat CMS di `/admin`, setiap simpan menjadi commit ke repo.

## Deploy
1. Buat repo GitHub (mis. `portofolio`), lalu upload seluruh isi folder ini.
2. Buka **Settings > Pages**, pilih branch `main` dan folder `/ (root)`. Situs aktif di `https://USERNAME.github.io/portofolio/`.
3. Edit `admin/config.yml`: ganti `repo: USERNAME/NAMA-REPO` dengan repo kamu.

## Login CMS (tanpa server tambahan)
1. Di GitHub: **Settings > Developer settings > Personal access tokens > Fine-grained tokens > Generate new token**.
2. Pilih hanya repo portofolio ini, beri izin **Contents: Read and write**.
3. Buka `https://USERNAME.github.io/portofolio/admin/`, pilih **Sign in with token**, tempel token tadi.
4. Edit isi, klik Save. Tunggu 1 sampai 2 menit sampai GitHub Pages memperbarui situs.

Simpan token dengan aman dan jangan pernah dimasukkan ke repo.

## Catatan
- Preview lokal: jalankan `python -m http.server` lalu buka `http://localhost:8000`.
- Ingin memakai Decap CMS resmi? Ganti script di `admin/index.html` ke Decap dan tambahkan `base_url` OAuth proxy di `config.yml`.
- Foto yang diunggah lewat CMS tersimpan di `assets/uploads/`.
