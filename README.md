# ingatin_telur

Landing page statis (HTML/CSS/JS, tanpa backend) untuk Ingatin Telur.

## Update harga harian

Harga produk diambil dari `prices.json` dan dirender otomatis ke halaman utama.

1. Buka `admin.html` (link tersedia di footer situs, bagian "Admin").
2. Login dengan password admin (dibuat sendiri saat pertama kali membuka halaman ini — tersimpan hanya di browser tersebut).
3. Ubah harga produk, lalu klik **Unduh prices.json**.
4. Ganti file `prices.json` di folder proyek ini dengan file yang baru diunduh.
5. Commit & push (atau unggah ke hosting) seperti biasa — situs otomatis memakai harga baru, tidak perlu ubah kode lain.

Catatan: karena situs ini statis tanpa server/database, `admin.html` tidak punya autentikasi sungguhan — password hanya tersimpan di browser perangkat masing-masing sebagai penghalang ringan. Jangan sebarkan link `admin.html` secara publik. `prices.json` juga perlu diakses lewat server (mis. `python3 -m http.server` saat development, atau hosting seperti GitHub Pages) — membuka `index.html`/`admin.html` langsung sebagai file lokal (`file://`) tidak bisa memuat harga karena browser memblokir `fetch` pada skema tersebut.
