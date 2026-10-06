### Aturan Bisnis

- Satu resep memiliki satu kategori dan dimiliki oleh satu pengguna.
- Langkah memasak diurutkan berdasarkan step_number.
- Takaran bahan disimpan di tabel pivot ingredient_recipe karena jumlahnya berbeda untuk setiap resep.
- Pengguna hanya dapat melihat dan mengubah meal planner serta daftar belanjanya sendiri.
- Daftar belanja dibuat dari seluruh meal_plan_items pada sebuah meal plan.
- Jumlah bahan dihitung dari quantity bahan pada resep dikali rasio servings rencana terhadap servings resep.
- Bahan yang sama dengan satuan yang sama dari beberapa resep digabung menjadi satu baris shopping_list_items.

## Teknologi

- PHP 8.3+ dan Laravel
- Blade templates
- Tailwind CSS (via Vite)
- MySQL

## Cara Menjalankan

# Clone repository
git clone https://github.com/nazwaaa0805/laravel5d
cd laravel5d

# Pindah ke branch P01
git checkout feature/p01-database-design

# Install dependensi
composer install
npm install

# Konfigurasi environment
cp .env.example .env
php artisan key:generate

# Atur koneksi database di file .env, lalu jalankan migration dan seeder
php artisan migrate --seed

# Jalankan server pengembangan
npm run dev
php artisan serve
Kemudian buka <http://localhost:8000>.

## Struktur Project

app/Models/        Model Eloquent dan relasinya
database/
  migrations/      Definisi tabel
  seeders/         Data awal (kategori, bahan, contoh resep)
resources/views/   Template Blade
docs/
  erd.png          Gambar ERD
## Roadmap

- [x] P01 — Perancangan database (ERD)
- [ ] P01 — Migration, model + relasi, dan seeder
- [ ] Autentikasi dan hak akses (admin / user)
- [ ] CRUD kategori, bahan, dan resep
- [ ] Favorit resep
- [ ] Meal planner
- [ ] Daftar belanja otomatis

## Penulis

Nazwa Aulia Rizka — NPM 2410010338 — Kelas 5D TI Reguler Banjarbaru

## Lisensi

Dirilis di bawah [MIT License](https://opensource.org/licenses/MIT).